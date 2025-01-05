>> Data that is accessed together is stored together.

# CLI
```bash
mongosh
```

```javascript
show dbs
use shop
db.help()
db.products.insertOne({name: "Book", price: 12.99})
db.products.find()
db.products.find().pretty()
```