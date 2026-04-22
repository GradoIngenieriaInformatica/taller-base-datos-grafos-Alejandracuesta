MATCH (p1:Persona)-[:TRABAJA_CON]->(p2:Persona)
WHERE id(p1) < id(p2)
RETURN 
  p1.nombre AS persona1,
  p2.nombre AS persona2;