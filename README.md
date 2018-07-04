# Laravel---Docker-
Develop your laravel application using docker instead of MAMP and other virtual environments


This file contains a version of Laravel, laradock and docker.  Make sure you are using php 7.0 and better for this environment.  For php >7.0 rollback the version of Laravel in this file.  

Prequisite (need to know): 
1. Docker installed on your device
2. This image was made on a Mac.  For window in environments, it should still work the same. 



Instructions: 
1. Run "docker-compose down" to ensure all docker processes are not running. 
2. In terminal run "lsof -i | grep LISTEN" to ensure the local host ports are not being used. 
2.1 If a localhost port is being used, end it by getting the PID number by entering "lsof -i : port number
", locate the listed PID number and then enter "kill -9 PIDNUMBERHERE" to end it with fire!
3. cd laradock
3.1 Then enter "docker-compose up -d nginx mysql phpmyadmin redis workspace".  Go get coffee.  If you get an error, enter each command individually such as "docker-compose up -d nginx" docker-compose up -d  mysql" docker-compose up -d phpmyadmin" etc. 
go to the following URL: http://localhost.  You can see that our Laravel 5.6 is running on that local server
4. We can access the phpMyAdmin at 8080 port on the browser. http://localhost:8080.  If you get any error, please verify your mysql server, database name, username, and password.  Create the database, whichever the name, you have written inside the .env file.



