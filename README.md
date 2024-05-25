# E-commerce Project

Microservice e-commerce project that consist of 5 services written in Java and Scala.

![image](https://github.com/Js111l/Ecommerce_Project/assets/95163990/4ee7f196-2b42-41e7-abdd-3b9ad4692e83)


## Table of contents

* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)

## General info
Project is currently in development.

The system is built based on a microservices architecture and consists of five services: ProductService, PriceService, FinancialTransactionsService, InventoryService, and CheckoutService. 
CheckoutService is responsible for handling products in the shopping cart. The service implements typical CRUD functionality related to individual products in the cart and communicates with PriceService to retrieve current prices for the given products.
PriceService also implements CRUD functionality related to prices and promotions for specific products or categories of products. The service includes an appropriate algorithm for calculating the price for each active product. 
The algorithm retrieves all active promotions for the given day for a specific product and then selects the promotion that offers the greatest price reduction for the product.

ProductService is responsible for CRUD functionality related to products in the system. Additionally, an appropriate mechanism using the Spring Batch module has been configured to load product data from a CSV file and save it to the database.

FinancialTransactionsService is a service written in Scala, responsible for managing payments and saving payment documents. The Stripe library is used to handle payments, leveraging its API for payment processing. Currently, the system supports credit card payments and bank transfers. Upon receiving a payment initiation request, the service communicates with the Stripe API to process the payment. 

InventoryService is also a service written in Scala and is responsible for managing the product inventory. It provides CRUD functionality related with products inventory and 
specific scheduled tasks that sends specific notifications when the appriopate inventory related event happens (e.g., when the quantity of an unavailable product increases, the user receives a notification that the product is available again)).

## All technologies

* Java 17
* Spring Boot 
* Spring Data JPA (Hibernate)
* Spring Batch
* MapStruct
* Lombok
* Scala 2.13
* Akka HTTP
* Akka Actor
* Slick
* Guice
* Stripe
* Docker
* MySQL
* Postgres

##### Libraries:

* Guava
* Lombok

## Product Service: 
https://github.com/Js111l/ProductService

## Financial Transactions Service:
https://github.com/Js111l/FinancialTransactionService

## Checkout Service:
https://github.com/Js111l/CheckoutService

## Price Service:
https://github.com/Js111l/PriceService

## Inventory Service:
https://github.com/Js111l/InventoryService
