#### write commands for following mongodb opertaions

1. create a database named `sports`
   // Answer here ..
   use sports

2. list all databases present in local mongod server.
   // Answer here..
   show dbs

3. create 3 collections named `cricket`, `football`, `TT` in sports database.
   // Answer...

```
db.createCollection('cricket')
db.createCollection('football')
db.createCollection('TT')

```

4. add 3 players in each of above collections which should have fields like `name`, `age`, `email`, state and auction_price.

```
TT
db.TT.insert({name:"",age:"",email:"",state:"",auction_price:""})
db.cricket.insert({name:"",age:"",email:"",state:"",auction_price:""})
db.football.insert({name:"",age:"",email:"",state:"",auction_price:""})

```

5. list all collections in sports database.

6. rename `TT` collection to `tennis`.

7. create a capped collection called `khokho` which should have max 3 documents.
   Try inserting more than 3 and output the result here ?

8. check whether a collection is capped or not?

9. remove all documents from `football` collection.

10. delete cricket collection completely.

11. rename database sports to games

12. delete sports database.
