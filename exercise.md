# Øvelse: Tilføj Courses og enrollments til StudentAdministration Projektet

Tidligere arbejde vi med ["StudentAdministration"](https://github.com/dat17v1/StudentAdministration)

I skal nu tilføje funktionalitet så der kan arbejdes med Courses og Enrollments

* I skal have to nye tabeller i jeres database så den kommer til at indeholde følgenede tabeller. 
  * Students
  * Courses
  * Enrollments
  
Enrollments burde egentligt hedde students_courses og er altså den tabel man bliver nød til at have når vi skal lave en mange til mange forbindelse.
Så Students kan altså være tilmeldt mange kurser og et kursus kan have mange studerende (så vi har en mange til mange forbidelse).

Når i har lavet tabellerne skal i lave en 
* CourseController og en 
* EnrollmentsController

Til disse skal i have CRUD html sider
* index.html
* create.html
* delete.html
* update.html

Det kunne også være godt at gøre det muligt på Students Details Siden at tilmelde en studerende til forskellige kurser (klasser). Lidt ala dette: 

<img src="https://github.com/dat17v1/2_18_mange_til_mange_forbindelser/blob/master/img/Screen%20Shot%202017-10-23%20at%2023.13.53.png" width="400px" />
<img src="https://github.com/dat17v1/2_18_mange_til_mange_forbindelser/blob/master/img/Screen%20Shot%202017-10-23%20at%2023.13.53.png" width="400px" />


I skal desuden huske at lave repositories til både *Course* og *Enrollment*    
I disse repositories skal forbindelsen til databasen håndteres.


