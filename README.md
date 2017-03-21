# final-project
The Pokemon recommendation engine for Kanto Pokemon. Final Project for DB

Link to Neo4j: http://54.68.75.194:7474/browser/
Username: neo4j
Password: tails1992
Query to match Pokemon:
MATCH (s1:name{name:'Bulbasaur'})-[*]->(n)<-[*]-(s2:name)
RETURN s2.name AS Name,collect(n.name) as in_common, count(*)as power ORDER BY power DESC

Feel free to try any other Pokemon from the Kanto region, but make sure to Camelcase the Pokemon's name. (i.e. Charmander not CHARMANDER or charmander)
