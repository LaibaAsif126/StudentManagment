# Debug Log – Lecture 7 Assignment

## Bug 1: NullReferenceException in Student Details
-  What went wrong: When accessing a student's CourseTitle, the app crashed with a NullReferenceException.
-  How I found it: Used Visual Studio debugger to step through the code and saw that student.Course was null.
-  How I fixed it: I added a null check in the Razor view using `@student.CourseTitle ?? "N/A"`.

## Bug 2: Bad ID Fetch Caused 404
-  What went wrong: API call to fetch a student with a non-existent ID returned a 404, breaking the view.
-  How I found it: Tested API using Postman and saw the 404. Also used Chrome DevTools to inspect response.
-  How I fixed it: I added a null check for the student object and returned NotFound() if it was null.

## Result
-  All bugs fixed
-  Pushed to GitHub
