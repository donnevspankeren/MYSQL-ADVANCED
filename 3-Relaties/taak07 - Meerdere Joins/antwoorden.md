1:
SELECT game.name, platform.platform, genre.genre FROM game
LEFT JOIN platform ON game.platform_id = platform.id
LEFT JOIN genre ON game.genre_id = genre.id
WHERE game.name LIKE "b%";

2:
SELECT game.name, platform.platform, publisher.publisher, year FROM game
LEFT JOIN platform ON game.platform_id = platform.id
LEFT JOIN publisher ON game.publisher_id = publisher.id
WHERE `year` = "2013"; 

3:
SELECT game.name, platform.platform, publisher.publisher, year FROM game
LEFT JOIN platform ON game.platform_id = platform.id
LEFT JOIN publisher ON game.publisher_id = publisher.id
WHERE `year` = "2013"; 

4:
SELECT platform.platform, year, genre.genre, publisher.publisher, jp_sales FROM game
LEFT JOIN platform ON game.platform_id = platform.id
LEFT JOIN genre ON game.genre_id = genre.id
LEFT JOIN publisher ON game.publisher_id = publisher.id
WHERE game.name LIKE 'Mario%';

5:
SELECT game.name, genre.genre, publisher.publisher, year FROM game
RIGHT JOIN platform ON game.platform_id = platform.id
LEFT JOIN genre ON game.genre_id = genre.id
LEFT JOIN publisher ON game.publisher_id = publisher.id
WHERE platform = 'PC';