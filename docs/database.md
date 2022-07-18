This application uses Amazon DynamoDB for the database, it is a fully managed NoSQL database.  NoSQL databases are optimized to query for items by a known key, so it's important to plan your application's data access patterns and design your tables around them.

The data modeling exercise is slightly more complicated.  To start, you create an entity relationship diagram to help you understand the different types of data in your application and their relationship to one another.

![xuml](/out/docs/plantuml/rdbms-physical-data-model.png)

The design of the schema is based on the access patterns that are required.   For the product price and availability data, the important access patterns are:

| Access Pattern |
|:---:|
| Look up latest price and inventory for all products by store |
| Get latest price and inventory for a given product at all stores |
| Get latest price and inventory for a given product at all stores with specified zip code |
| Find stores with the lowest price for a given product |
| Find stores with the lowest price for a given product at all stores with specified zip code |
| Get price history of a given product within a given date range |
| Get price history of a given product at a retailer within a given date range |

Example AWS CLI command to create DynamoDB table from JSON file.

```
aws dynamodb create-table --cli-input-json file://create-table-materials.json --region us-east-1
```

https://emshea.com/post/part-1-dynamodb-single-table-design

