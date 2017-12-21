/* SELECT * FROM Invoice i
JOIN invoiceLine il ON il.invoiceId = i.invoiceId
WHERE il.UnitPrice > 0.99;
 */
/*  SELECT i.InvoiceDate, c.FirstName, c.LastName, i.total
 FROM Invoice i 
 JOIN Customer c ON i.CustomerId = c.CustomerId;
  */
  
/*   SELECT c.FirstName, c.LastName, e.FirstName, e.LastName
  from Employee e 
  JOIN Customer c ON c.SupportRepId = e.EmployeeId
  */
/*   
  SELECT al.title, ar.name 
  from album al
  JOIN Artist ar ON al.ArtistId = ar.ArtistId;
   */
   
/*  SELECT tr.TrackId
 FROM PlaylistTrack tr
 JOIN Playlist p ON p.PlaylistId = tr.PlaylistId
 WHERE P.Name = 'Music'; */
 
/*  SELECT t.Name
 FROM Track t
 JOIN PlaylistTrack p ON p.TrackId = t.TrackId
 WHERE p.PlaylistId = 5; */
 
 
/*  SELECT t.name, p.name
 FROM Track t 
 JOIN PlaylistTrack pt ON t.TrackId = pt.TrackId
 JOIN Playlist p ON pt.PlaylistId = p.playlistId;
  */
  
/*  SELECT t.Name, al.Title
 FROM TRACK t
 JOIN Album al ON t.AlbumId = al.AlbumId
 JOIN Genre g ON g.GenreId = t.GenreId
 WHERE g.Name = "Alternative";
 
 */
 
/*  SELECT * FROM Invoice i
 WHERE InvoiceId IN (SELECT invoiceId FROM InvoiceLine WHERE UnitPrice > 0.99)
  */
 
/* SELECT * 
FROM PlaylistTrack
WHERE PlaylistId = ( SELECT PlaylistId FROM Playlist p WHERE Name = "Music");
 
  */
  
/*  SELECT t.Name
 from Track t
 join PlaylistTrack pt ON pt.TrackId = t.TrackId
 Where pt.PlaylistId = 5;
  */
  
/*   SELECT * 
  From Track t
  where GenreId In ( SELECT GenreId from Genre where Name = "Comedy");

 */
/*  SELECT * 
 from Track t
 where AlbumId IN (SELECT AlbumId from Album where name = "Fireball"); */
 
 
/*  SELECT *
FROM Track
WHERE AlbumId IN ( 
  SELECT AlbumId FROM Album WHERE ArtistId IN ( 
    SELECT ArtistId FROM Artist WHERE Name = "Queen" 
  )
);  */
 
 
 
/*  UPDATE Customer
 set Fax = null
 where Fax IS NOT NULL; */
 
/*  UPDATE Customer
 set Company = "self"
 where company is null; */
 
/*  UPDATE Customer
 set LastName = "Thompson"
 where LastName = "Barnett"; */
 
 
/* UPDATE Customer
SET SupportRepId = 4
WHERE Email = "luisrojas@yahoo.cl"; */
 
 
/*  UPDATE Track 
 set Composer = "The darkness around us"
 where GenreId = ( SELECT GenreId from Genre Where Name = "Metal");
  */
 
/* SELECT Count(*), g.Name
from Track t
join Genre g ON t.GenreId = g.GenreId
group by g.Name;
  */
  
/* SELECT Count(*), g.Name
from Track t
Join Genre g ON t.GenreId = g.GenreId
where g.Name = "Pop" OR g.Name = "Rock"
group by g.Name; */


/*  SELECT Count(*)
 FROM Artist ar 
 -- join is linking up artistId from artist and from Album
 join Album al On ar.ArtistId = al.ArtistId
 group by al.ArtistId; */
 
/*  SELECT DISTINCT Composer
 from Track
  */
  
/* SELECT DISTINCT BillingPostalCode
from Invoice */

/* SELECT DISTINCT Company
from Customer */

/* DROP TABLE IF EXISTS practice_delete;
CREATE TABLE practice_delete ( Name string, Type string, Value integer );
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "bronze", 50);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "bronze", 50);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "bronze", 50);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "silver", 100);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "silver", 100);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "gold", 150);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "gold", 150);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "gold", 150);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "gold", 150);

 */
/* DELETE FROM practice_delete where Type = "bronze"; */

/* DELETE FROM practice_delete WHERE TYPE = "silver"; */

/* DELETE FROM practice_delete WHERE Value = 150; */

/* SELECT * FROM practice_delete; */

DROP TABLE IF EXISTS users;
DROP TABLE IF EXISTS products;
DROP TABLE IF EXISTS orders;


CREATE TABLE users (
Name STRING,
email VARCHAR(40)
);

INSERT INTO users
(Name, email)
VALUES
("Ryan Stupey", "ryan.stupey@gmail.com"),
("Sarah Mongomery", "sh@montague.com"),
("jim Beam", "JackDaniels@ILikeWhiskey.com");

/* SELECT * from users */

CREATE TABLE products (
product_id integer PRIMARY KEY,
name STRING,
price FLOAT
);

INSERT INTO products 
(name, price)
VALUES 
("Tilde", 13.70),
("belt", 3.50),
("T-rex", 12.77),
("apples", 2.00),
("truck", 1.70),
("book", 20.00),
("yoyo", 100.00);


CREATE TABLE orders (
product_id INTEGER PRIMARY KEY

);

INSERT INTO orders 
(product_id)
VALUES
(1),
(4),
(9),
(5),
(3);

SELECT * FROM orders






 
 