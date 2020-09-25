Simple web API for the student course registration process using Laravel framework.

Endpoints:

API must have an endpoint to create a student.
route:http://127.0.0.1:8000/api/student/   (method= POST)

API must have an endpoint to view all students.
route:http://127.0.0.1:8000/api/student/   (method= GET)

API must have an endpoint to update a student.
route:http://127.0.0.1:8000/api/student/2 (method=PATCH)

API must have an endpoint to create a course.
route:http://127.0.0.1:8000/api/course/ (method=POST)

API must have an endpoint to view all courses.
route:http://127.0.0.1:8000/api/course/ (method=GET)

API must have an endpoint to register a course.
route:http://127.0.0.1:8000/api/enrollment/ (method=POST)

API must have an endpoint to drop a course.
route:http://127.0.0.1:8000/api/enrollment/1 (method=DELETE)

API must have an endpoint to view taken courses of a specific student.
route:http://127.0.0.1:8000/api/enrollment/1 (method=GET)

Routes:

+--------+-----------+-----------------------------+--------------------+---------------------------------------------------+------------+
| Domain | Method    | URI                         | Name               | Action                                            | Middleware |
+--------+-----------+-----------------------------+--------------------+---------------------------------------------------+------------+
|        | GET|HEAD  | /                           |                    | Closure                                           | web        |
|        | GET|HEAD  | api/course                  | course.index       | App\Http\Controllers\CourseController@index       | api        |
|        | POST      | api/course                  | course.store       | App\Http\Controllers\CourseController@store       | api        |
|        | DELETE    | api/course/{course}         | course.destroy     | App\Http\Controllers\CourseController@destroy     | api        |
|        | PUT|PATCH | api/course/{course}         | course.update      | App\Http\Controllers\CourseController@update      | api        |
|        | GET|HEAD  | api/course/{course}         | course.show        | App\Http\Controllers\CourseController@show        | api        |
|        | POST      | api/enrollment              | enrollment.store   | App\Http\Controllers\EnrollmentController@store   | api        |
|        | GET|HEAD  | api/enrollment              | enrollment.index   | App\Http\Controllers\EnrollmentController@index   | api        |
|        | GET|HEAD  | api/enrollment/{enrollment} | enrollment.show    | App\Http\Controllers\EnrollmentController@show    | api        |
|        | PUT|PATCH | api/enrollment/{enrollment} | enrollment.update  | App\Http\Controllers\EnrollmentController@update  | api        |
|        | DELETE    | api/enrollment/{enrollment} | enrollment.destroy | App\Http\Controllers\EnrollmentController@destroy | api        |
|        | GET|HEAD  | api/student                 | student.index      | App\Http\Controllers\StudentController@index      | api        |
|        | POST      | api/student                 | student.store      | App\Http\Controllers\StudentController@store      | api        |
|        | DELETE    | api/student/{student}       | student.destroy    | App\Http\Controllers\StudentController@destroy    | api        |
|        | PUT|PATCH | api/student/{student}       | student.update     | App\Http\Controllers\StudentController@update     | api        |
|        | GET|HEAD  | api/student/{student}       | student.show       | App\Http\Controllers\StudentController@show       | api        |
|        | GET|HEAD  | api/user                    |                    | Closure                                           | api        |
|        |           |                             |                    |                                                   | auth:api   |
+--------+-----------+-----------------------------+--------------------+---------------------------------------------------+------------+


