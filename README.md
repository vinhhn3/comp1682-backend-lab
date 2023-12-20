# COMP1682 Backend Lab: Building a .NET API for Simultaneous Connection to SQL Server Express and MongoDB

Welcome to the COMP1682 Backend Lab, where you'll embark on a practical journey to develop a .NET API that seamlessly connects to both SQL Server Express and MongoDB. This hands-on tutorial integrates the power of ChatGPT with software development skills, enabling you to build a robust system that enhances performance.

## Objectives:

1. **Practice with .NET API:**

   - Gain hands-on experience in developing a .NET API.
   - Strengthen your understanding of API development principles.

2. **Utilize ChatGPT for System Development:**

   - Leverage ChatGPT's capabilities to guide you through the development process.
   - Learn how to combine ChatGPT and software knowledge effectively.

3. **Simultaneous Connection to SQL Server Express and MongoDB:**
   - Explore the intricacies of connecting a .NET API to both SQL Server Express and MongoDB concurrently.
   - Understand the importance of dual-database integration for improved system performance.

## Lab Overview:

Throughout this lab, you'll follow step-by-step instructions provided by ChatGPT to create a .NET API that seamlessly interacts with SQL Server Express and MongoDB. This practical approach ensures a comprehensive understanding of the development process, combining theoretical knowledge with hands-on implementation.

## Key Takeaways:

By the end of this lab, you will:

- Have practical experience in developing a .NET API.
- Understand the collaborative potential of ChatGPT and software development.
- Grasp the significance of integrating multiple databases for enhanced system performance.

Get ready to dive into the world of backend development, where you'll harness the power of .NET, ChatGPT, and dual-database connectivity to create a resilient and high-performing API. Let's begin!

## Startup Prompt

Start with this prompt to setup

```bash
I want you to act as a Teacher in Software. I will provide some specific information about software requirements.
It will be your job to come up with a tutorial to meet the requirements with C# and .NET and Visual Studio

I will give you information and instructions to follow.

Answer YES if understand
```

Then, input the Database design

```bash
I want you to develop an .NET API connect to MongoDB and SQL Server Express at the same time.

Following is the design of 2 database.

SQL Server:

Users:
- Id (PK)
- Username:
- Password

Addresses:
- Id (PK)
- Name
- UserId (FK)

MongoDB

Products
- Id (PK)
- Name
- Price

Orders
- ID
- UserID
- Items: [
	{ProductId: 1, Quantity: 2},
	{ProductId: 2, Quantity: 3},
	...
]

Answer Yes if you read and understand all above
```

## Connect to SQL Server

```bash
Now, start with the SQL Server first.

First, show me how to create the project with Visual Studio
```

```bash
Indicate what packages need to be installed
```

```bash
Create models.
- Do not forget to create DbContext, setup the ConnectionString, run Migration and Update-Database
```

```
Now, Create full CRUD functions UsersController
- I want when perform the endpoint GET /user/:id, it stores the UserId in the cookie for the response.
```

```bash
Now, create the AddressesController for SQL server
```

**Note:** sometimes, ChatGPT will forget the Database Design, you will have to remind it sometimes.

## MongoDB

```bash
First, Setup MongoDB:
- Create a new MongoDB database on MongoAtlas and collections corresponding to models.
```

```bash
Then, Install MongoDB Driver:
- Install the MongoDB driver for .NET with Visual Studio
```

```bash
Create MongoDB Models:
- Define models for MongoDB entities (Products and Orders).
```

```bash
Configure MongoDB Connection:
- Set up the connection string for MongoDB in  application settings.
```

```bash
Create MongoDB Context:
- Implement a context class that derives from IMongoDatabase to handle interactions with MongoDB.
```

```bash
Implement CRUD Operations:
- Create API controllers with actions for CRUD operations on MongoDB entities.
- Make sure to use the UserId from cookie when perform POST in Orders.
```
