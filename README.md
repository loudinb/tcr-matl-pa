# Material Price & Availability

This is a custom application developed for True Craft Renovations (West Chester, OH).  There are three componenents to the material price and availability application.
* A web scraper which extracts material price and availability data from the websites of major big box retailers located in areas where True Craft Renovations operate. (Selenium and Python)
* A database to store the scraped data. (Amazon DynamoDB)
* A REST API for reading data from the database. (Node.js)

The application is deployed to AWS using a serverless framework, the components used are:
* [AWS Lambda](https://aws.amazon.com/lambda/)
* [Amazon API Gateway](https://aws.amazon.com/api-gateway/)
* [Amazon DynamoDB](https://aws.amazon.com/dynamodb/)

### AWS Credentials and Configuration

You must run `aws config` to set up your AWS CLI, for more information see [Quick configuration with aws confgiure](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html#cli-configure-quickstart-config).

