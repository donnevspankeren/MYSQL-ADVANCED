# Antwoorden Eindopdracht

1. 
Copy paste je gemaakte SQL query hieronder
SELECT races.name AS Name_Race, circuits.name AS Name_Circuits FROM races
LEFT JOIN circuits ON races.circuitId = circuits.circuitId
WHERE year=2018;

2. Copy paste je gemaakte SQL query hieronder
SELECT races.name AS Race, drivers.driverRef AS Driver, points FROM driver_standing
LEFT JOIN races ON driver_standing.raceId = races.raceId
LEFT JOIN drivers ON driver_standing.driverId = drivers.driverId
WHERE races.year='2017' AND points='10';

3. Copy paste je gemaakte SQL query hieronder
   SELECT drivers.forename AS Voornaam, drivers.surname AS Achternaam, duration FROM pitstops 
LEFT JOIN drivers ON pitstops.driverId = drivers.driverId 
WHERE duration<25

4. Copy paste je gemaakte SQL query hieronder
SELECT constructors.constructorRef AS constructor, races.name AS GrandPrix FROM  
LEFT JOIN constructors ON constructor_standing.constructorId = constructors.constructorId
LEFT JOIN races ON constructor_standing.raceId = races.raceId
WHERE constructors.constructorRef = 'McLaren' OR races.year = '2018';

5. Copy paste je gemaakte SQL query hieronder
SELECT circuits.name AS "circuit",  circuits.country AS "Land", races.name AS "Grand Prix", drivers.surname AS 'Achternaam' FROM races
LEFT JOIN circuits ON races.circuitId = circuits.circuitId
LEFT JOIN drivers ON drivers.driverId = drivers.driverId
WHERE races.year = "1950"
AND drivers.surname LIKE "F%";