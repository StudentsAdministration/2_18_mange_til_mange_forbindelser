# Dag 18 Mange til mange forbindelser
Agenda dag 18 d. 24-10-2017    

*Databasen vi arbejdede med sidste gang og bruger i dag kan i finde [her](https://github.com/dat17v1/2_18_mange_til_mange_forbindelser/blob/master/shop.sql)*

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

### INNER JOIN
Skal vi bruge SQL til at spørge i databasen kunne det se sådan ud:

````
  SELECT * FROM relationsshop.order
  INNER JOIN relationsshop.order_product ON relationsshop.order.order_id = relationsshop.order_product.fk_order
  INNER JOIN relationsshop.products ON relationsshop.products.product_id = relationsshop.order_product.fk_product
  INNER JOIN relationsshop.customers ON relationsshop.order.fk_customer_id = relationsshop.customers.customer_id
````

## [Øvelse: Tilføj Courses og Enrollment til Studentsadministration]()

# Literatur
<a href="https://www.lynda.com/Programming-Foundations-tutorials/Joining-tables/412845/438446-4.html?autoplay=true"><img src="https://github.com/dat17v1/2_18_mange_til_mange_forbindelser/blob/master/img/Screen%20Shot%202017-10-23%20at%2015.56.16.png" width="300px"  />   </a>  


