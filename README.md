# MongoDb-Cheatsheet
### MongoD version v6.0.3


## MongoDb command for Database:

#### 1) view all database :
```mongosh
show dbs;
```
#### 2)create a new or switch database
```mongosh
use DBName;

```
#### 3) View current Database
```mongosh
db;
```
#### 4) Delete database
```mongosh
db.dropDatabase()
```


# MongoDb command for Collections:

#### 5) view Database collections :
```mongosh
show collections;
```
#### 6) Create a new Collections :
```mongosh
db.createCollection('suvu');
```
#### 7)Delete Collections :
```mongosh
db.<COLLECTIONS_NAME>.drop();
```
#### 8) Insert One-Row in Collections:
```mongosh
db.content.insert({
	'name':'Suvendu',
	'pl':'c,c++',
	'Age':20
});

db.content.insertOne({ 'name': 'Supratim', 'pl': 'Java', 'Age': 20 });

db.content.insertOne({ 'name': 'Supratim Majumder', 'pl': 'Java', 'Age': 20 ,'date':new Date()});

```

#### 9)Insert many-row in Collections:

```mongosh
db.content.insertMany([
{ 'name': 'Bristi', 'pl': 'Python', 'Age': 19 },
{ 'name': 'Sayan', 'pl': 'Java,Dsa', 'Age': 20 },
{ 'name': 'Prasanta', 'pl': 'Js', 'Age': 20 },
{ 'name': 'Avas', 'pl': 'Kichu Pari na ami', 'Age': 22 }

]);
```

#### 10) show all collections rows values:

```mongosh
db.content.find();
```

#### 11)Search in MongoDb Databse:

```mongosh
db.content.find({pl:'Java'});
```
#### 12) Limit the number of rows in output :

```mongosh
db.content.find({pl:'Java'}).limit(2);
```
#### 13)Count the number of rows in outut :

```mongosh
db.content.find().count();
db.content.find({name:'Suvendu'}).count();
db.content.findOne({name:'Suvendu'});
```
#### 14) sort the number of rows in output :
##### i) Sort the value with descending order-

```mongosh
db.content.find().sort({name:-1});
```
##### ii) Sort the value with Asecending order-
```mongosh
db.content.find().sort({name:1});
```

#### 15) Remove row :
```mongosh
db.content.remove({name:'Supratim'});
```
