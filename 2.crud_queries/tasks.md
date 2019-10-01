1. Create a database named `blog`.

```
use blog
```

2. Create a collection called 'articles'.

```
db.createCollection('articles');
```

3. Insert multiple documents(at least 3) into articles. It should have fields

```
db.articles.insertMany([{name: 'Abhinav', title: 'javascript', tag: ['web', 'dev'], age: '23'}, {name: 'Shivam', title: 'node', tag: ['web', 'dev'], age: '23'}, {name: 'Swastik', title: 'react', tag: ['web', 'dev'], age: '20'}]);
```

4. Find all the articles using `db.COLLECTION_NAME.find()`

```
db.articles.find();
```

5. Find a document using \_id field.

```
db.articles.find({ "_id" : ObjectId("5d5ab239209af49d864119b9")});
```

6. Find documents using title and author's name field.

```
db.articles.find({name: 'Abhinav', title: 'javascript'});
```

7. Find document using a specific tag.

```
db.articles.find({"tag" : {$all : ['web']}});
```

8. Update title of a document using its \_id field.

```
db.articles.update({_id: ObjectId("5d5abeead9d39d6e5d4f99af")}, {$set: {title: 'javascript'}});
```

9. Update a author's name using article's title.

```

```

10. rename details field to description from articles collection.

```

```

11. Add additional tag in a specific document.

```

```

12. Update an article's tags using $set and without $set.

```

```

- Write the differences here ?

```

```

13. Increment an auhtor's age by 5.

```
db.articles.update({name: "Abhinav"}, {$inc: {age: 25}});
```

14. Delete a document using \_id field with `db.COLLECTION_NAME.remove()`.

```
db.articles.remove({_id: ObjectId("5d5ad0436efa7fabe76dd86e")});
```

Use sample.js data for below queries.

```

```

1. Find all males who play cricket.

```
db.users.find({gender: "Male", sports: {$all: ['football']}});
```

2. Update user with extra golf field in sports array whose name is "Steve Ortega".

```
db.users.update({name: "Steve Ortega"}, {$push: {sports: "golf"}});
```

3. Find all users who play either 'football' or 'cricket'.

```
db.users.find({sports: {$in: ['football', 'cricket']}});
```

4. Find all users whose name includes 'ri' in their name.

```
db.users.find({name: /ri/i});
```
