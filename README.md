## AI Ontology OWL File to Neo4j Graph Database

# Installation

- This requires [Neo4j Desktop](https://neo4j.com/download-center/#desktop) to run.

- Install the python dependencies

```sh
pip install neo4j
pip install owlready2
```

- We will use Neo4j Desktop to create a local DBMS and transport owl file to it.
- Install and open Neo4j Desktop

![](https://github.com/dikshant293/dikshant_repo/raw/master/pics/p1.PNG)

- Click on New -> Add -> Local
- Put any Name and Password (here testdbms and 12345 respectively)

![](https://github.com/dikshant293/dikshant_repo/raw/master/pics/p2.png)

- Click on the three dots beside the DBMS name to open Settings file
- Paste the following line in the file and apply changes
```sh
apoc.export.file.enabled=true
apoc.import.file.use_neo4j_config=false
```
![](https://github.com/dikshant293/dikshant_repo/raw/master/pics/p3.png)

- Paste the following line in the file and apply changes
```sh
apoc.export.file.enabled=true
apoc.import.file.use_neo4j_config=false
```
![](https://github.com/dikshant293/dikshant_repo/raw/master/pics/p4.png)

- Open up plugins and install APOC, this is required to export database

![](https://github.com/dikshant293/dikshant_repo/raw/master/pics/p8.png)

- Start the DBMS by clicking on start
- Click on the "testdbms" to bring up the details
- Copy the Bolt Port. This will be used to connect to the local database via python 
- 
![](https://github.com/dikshant293/dikshant_repo/raw/master/pics/p5.png)

- Open up owl-to-neo3j-DB.py in any text editor
- Paste Bolt port in URL
- Username is neo4j by default (no change necessary if above steps followed)
- Enter password (here 12345)

![](https://github.com/dikshant293/dikshant_repo/raw/master/pics/p6.png)

Run the python script
If no error, whole owl database will be converted to JSON and cypher query file.
Files will be located in drive root.

## Result

- Use Neo4j Browser from Ne04j Desktop to access graph by basic Cypher queries 

![](https://github.com/dikshant293/dikshant_repo/raw/master/pics/p9.png)
