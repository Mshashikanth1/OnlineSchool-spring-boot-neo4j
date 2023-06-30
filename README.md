# OnlineSchool-spring-boot-neo4j
Demo Project for Learning Neo4j Graph Database and cypher query Langauage
# To run Project
```./mvnw clean install```
```./mvnw spring-boot:run```

# Cipher Basics
cipher is the  simple query language similar sql for relational databases but cipher is for neo4j
# create a node
```create (n:Course {id:8,name:'Biology',teacher:'rajesh'})```


# get all nodes
```match (n) return n```

# get only nodes of type user and of limit
```MATCH (n:User) RETURN n LIMIT 25;```

# create a relations (or ) edges 
```
match 
(n:User),(c:Course) 
where n.name='shashi kanth' 
and  c.name='Science 101'  
create (n)-[r:REGISTERED]->(c) 
return type(r);
```
```
MATCH
  (a:User),
  (b:User)
WHERE a.handle = 'ssh3' AND b.handle = 'johndoe123'
CREATE (b)-[r:sister]->(a)
RETURN type(r)
```