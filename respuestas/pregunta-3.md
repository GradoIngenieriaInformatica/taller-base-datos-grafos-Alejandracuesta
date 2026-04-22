MATCH (p:Persona)-[:VIVE_EN]->(c:Ciudad)
WITH 
  c,
  count(p) AS numero_personas
WHERE numero_personas > 2
RETURN 
  c.nombre AS ciudad,
  numero_personas;