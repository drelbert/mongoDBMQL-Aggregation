## Set of Terms for Reference with MQL and the Aggregation Pipeline

#### MongoDB Query Language (MQL)
- MQL: a MongoDB specific language structure for interacting with data stored in a database collection as documents.  Allows for query (CRUD) operations.

- CRUD: a common operations set for creating, reading, updating and deleting documents.

- Create Operations: inserts or creates a new document in a collection.  
    - common methods

      `db.collection.insertOne()`
      `db.collection.insertMany()`

    - simple implementation

      `db.student.insertOne(
          {
              name: "Toni",
              role: "data scientist",
              modulesCompleted: 3
          }
      )`

- Read Operations: a set of operators to retrieve or query a collection for documents.
    - method

      `db.collection.find()`

    - simple implementation

       `db.student.find(
           {
               name: "Toni"
               }
       )`
       

#### Aggregation Framework

- Aggregation Framework: Opinionated, MongoDb domain specific language.  Also known as the Aggregation Language, providing for data analytic workflows, in the form of a pipeline and stages.

- Aggregation Pipeline: built with one or more stages that operate on a collection of documents.  

- Stages: Built of operators that process documents based on a use case such as totals or averages.  
    - example stage 

      `$match`
    
    - simple implementation 

       `db.learners.aggregate([
           {$match: {modulesCompleted: 4}}
       ])`


<p>Please note this is only to illustrate this asset for the context of defining the differences between MQL and the Aggregation Pipeline.  For production, this list would be built out to include all terms that would be used in the module.</p>