# Dag 18 Mange til mange forbindelser
Agenda dag 18 d. 24-10-2017

## En til Mange forbidelser
Sidste gang arbejde vi med "En til Mange" forbidelser i databasen 

<img src="https://github.com/dat17v1/2_18_mange_til_mange_forbindelser/blob/master/img/en-mange.png" width="300px" />
<img src="https://github.com/dat17v1/2_18_mange_til_mange_forbindelser/blob/master/img/en-mange-tabeller.png" width="300px" />    

### Inner Join
Vi brugte også SQL til at lave forespøgelser i tabellerne.

````   
  SELECT * FROM order INNER JOIN rcustomers ON order.fk_customer_id = customers.customer_id;
````   
Og med WHERE i Stamentet for at vælge mere præcist   

````   
  SELECT * FROM order INNER JOIN customers ON order.fk_customer_id = customers.customer_id WHERE customers.Customer_id = 1;
````  

## Mange til Mange Forbidelser
I dag skal vi arbejde med den anden type: en Mange til Mange forbidelse.    
Hvor en Customer kan have mange ordre, men hvor en enkelt Order kun kan have en customer tilknyttet.    
En order derimod kan indeholde mange produkter, og et produkt kan også være med i mange ordre.    

<img src="https://github.com/dat17v1/2_18_mange_til_mange_forbindelser/blob/master/img/mange-mange-2.png" width="500px" />    


Eller som i vil se i dag kan det faktisk ikke lade sig gøre, så derfor kommer ER-Diagrammet til at se sådan ud:    

<img src="https://github.com/dat17v1/2_18_mange_til_mange_forbindelser/blob/master/img/Mange-mange_2.png"  />    



## [Øvelse: Tilføj Courses og Enrollment til Studentsadministration]()
