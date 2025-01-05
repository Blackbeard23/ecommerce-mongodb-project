# Student MongoDB Project: E-Commerce Data Analysis

This project is designed to demonstrate understanding of MongoDB concepts, including CRUD operations, aggregation, indexing, $lookup, schema design, and more. Working with a sample dataset to model, query, and analyze data. The project mirrors real-world scenarios to help consolidate knowledge.

## Project Overview

Tasked with building a MongoDB database for an e-commerce platform and using it to answer analytical questions. The project involves:

- Creating collections and designing a schema.
- Importing sample data.
- Applying advanced queries and aggregation pipelines.
- Answering key analytical questions.

## Schema Design

- `Customers` collection uses an embedded schema for its `address` field. This is because the address details (street, city, state) are tightly coupled with the customer and are likely to always be accessed together.

- The `Products` collection does not reference other collections directly in this design. It represents standalone data about products.

- The `Orders` collection references the customers collection through the `customer_id` field. The orders collection references the customers collection through the customer_id field.

- The `Order_items` collection references both the `Orders` collection through the `order_id` field and the `Products` collection through the `product_id` field.
