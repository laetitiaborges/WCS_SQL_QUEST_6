SELECT t.`name`, COUNT(p.id) AS count_nbplayers
FROM player p
INNER JOIN team t
  ON p.team_id = t.id
GROUP BY t.`name`
ORDER BY count_nbplayers DESC;


SELECT t.name, COUNT(p.role) as nb_players
FROM player p
INNER JOIN team t
  ON p.team_id = t.id
GROUP BY t.name
HAVING nb_players >= 14
ORDER BY t.name


SELECT *
FROM player
WHERE DAYOFWEEK(enrollment_date) = 2
ORDER BY enrollment_date;
