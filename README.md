## dmongo
- A python library for communicating and Querying mongodb

### how to use 

1. Install package
 
```
pip install dmongo
 
```
2. import the package 
 
```
from dmongo.dmongo import mongoQuery

```
3. initializing dmongo 
- To initialize dmongo, create a MONGO_URI, you either create the Database or dmongo will automatically creates it, if it doesn"t exist.


```
Query=mongoQuery(MONGO_URI="localhost:27017",Database="geof",collections="movies")

```
4. creating a record
- To create a new record, send in a data in this Dictionary format, where the key pair is the record name and the value pair is the value to be stored.
```
 Query.create({"name":"JohnDoe","email":"jdoe@gmail.com","username":"JohnD"})

```

4. get all record
- Returns all the record available in the defined collection of the specified Database
```
Query.getAll()

```

5. get one record 
- Returns a particular record from the defined collection of the specified database base on it's ID. which is unique across the collection.

```
Query.getOne(ID="620843809255d268ce967245")

```

6. updating a record
- replaces the existing value of the specified key pair with a new value of the specified value pair according to the ID specified.
```
Query.update(ID="620843809255d268ce967245",data={"name":"JamesDoe"})

```
7. filtering of record 
- Returns all the record with the same value as specified
```
Query.filterBy(data={"name":"JamesDoe"})

```
8. deleting a record
- Deletes a record according to the ID specified.
```
Query.delete(ID="620843809255d268ce967245")

```

