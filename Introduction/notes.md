# Notes

> Data that is accessed together is stored together.
>> A single document in a collection (including all embedded documents it might have) must be **<= 16MB**. Additionally, you may only have 100 levels of embedded documents.

## CLI

```javascript
mongosh
show dbs
use shop
db.help()
db.products.insertOne({name: "Book", price: 12.99})
db.products.find()
db.products.find().pretty()
db.products.deleteOne({name: "Book"})
db.products.drop()
db.dropDatabase()
mongod --help
```

## Numbers

- **NumberInt** creates a **int32** value = `NumberInt(55)`
- **NumberLong** creates a **int64** value = `NumberLong(7489729384792)`

If you just use a number, it will get added as a **normal double** into the database. The reason for this is that the shell is based on JS which only knows float/double values and doesn't differ between integers and floats.

- **NumberDecimal** creates a high-precision double value = `NumberDecimal("12.99")` = This can be helpful for cases where you need (many) exact decimal places for calculations.

## Important links

- <https://www.mongodb.com/docs/manual/core/schema-validation/>
- <https://www.mongodb.com/docs/manual/reference/limits/>
