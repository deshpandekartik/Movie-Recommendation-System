Team Members :
Mohit Kumar Joshi (B00698010) - mjoshi7
Kartik Ranjit Deshpande (B00692326) - kdeshpa3
Vaibhav Chauhan (B00677602) - vchauha2

Our project has three parts -:

1. Procedural paradgim ( C ) - Written to initially populate database with movies and ratings from a txt file.
    gcc -o procedural $(mysql_config --cflags) procedural.c $(mysql_config --libs)
    ./procedural
    Add to crontab -e "./procedural"

   
   To set delete status to Y for deleting movies which is done by upper script
   gcc -o procedural2 $(mysql_config --cflags) procedural_set_stat_y.c $(mysql_config --libs)
   ./procedural2
   Add to crontab -e "./procedural2"

2. Object oriented paradgim ( java ) - Web application of the module is written in java. This includes registration, login of the user.It provides a user interface where user can give ratings and get recommendations.

Web application to be deployed over apache tomcat 7.
Starting url = http://localhost:8080/movies/pages/login.jsp

3. Functional paradgim ( scala ) - The recommendation engine to pull out recommendations for a user based on his previos choices is written in scala.
It is initiated by web application, bash initiates the execution.

4. Database
Our database is a mysql database set up using phpmyadmin
Tables
- movie_rating
	Populated by c program from input file , used to delete marked entries.
- movie_recommendation_scala
	Populated when scala runs in background to provide movie reommendations to user
- user_login
	Populated when user register's.
- user_movie_rating
	Populated when user gives rating to a movie.


References :
https://alvinalexander.com
https://www.tutorialspoint.com
http://www.brunton-spall.co.uk
http://allaboutscala.com
https://www.youtube.com/watch?v=Wm6CUkswsNw&t=1955s
