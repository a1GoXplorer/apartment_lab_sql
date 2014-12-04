ANSWERS FOR APARTMENT_SQL LAB

1) \dt - list all tables in the currrent DB
2) \du - list users
3) SELECT * FROM OWNERS; - list the owners table
4) SELECT name FROM owners; - show all the names of the owners
5) SELECT age FROM owners ORDER BY age ASC; - lists owners' names ascending
6) SELECT * FROM owners WHERE name = 'Donald'; - Search for 'Donald' in owners
7) SELECT * FROM owners WHERE age > 30; - list for owners over the age of 30
8) SELECT * FROM owners WHERE name LIKE 'E%'; - list for owners with a name starting with 'E'
9) INSERT INTO owners (name, age) VALUES ('John', 33); - We add John as and owner, he's 33
10)INSET INTO owners (name, age) VALUES ('Jane', 30); - We add Jane as an owner, she's 43
11) UPDATE owners SET age = 30 WHERE name = 'Jane'; - Jane becomes 30.
12) UPDATE owners SET name = 'Janet' WHERE name = 'Jane'; - Jane changes her name to Janet
13) INSERT INTO properties (name, units, owner_id) VALUES ('Archstone', 20, 1); - added a 20 unit property
14) DELETE FROM owners name = 'Jane'; delete the owner named 'Jane'
15) SELECT * FROM properties WHERE name <> 'Archstone' AND property_id NOT IN (3,5) ORDER BY name ASC; - Show the properties that aren't in the 3 or 5 key and aren't called 'Archstone'...in ascending order
16) SELECT COUNT (*) FROM properties; - Shows the count of rows from properties
17) SELECT MAX(age) FROM owners; - Shows who's the oldest owner
18) SELECT * FROM owners LIMIT 3; - shows the first 3 owners
19) ALTER TABLE properties ADD CONSTRAINT owner_fk FOREIGN KEY (owner_id) REFERENCES owners (owner_id) ON DELETE NO ACTION; - creates a foreign key that refers to the owners table and creates the ON DELETE NO ACTION constraint
20) SELECT owners.name, properties.name FROM owners JOIN properties ON owners.owner_id = properties.owner_id; - Show the owners' properties.
