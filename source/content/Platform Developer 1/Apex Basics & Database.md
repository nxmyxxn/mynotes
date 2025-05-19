
# 1. Get Started with Apex
## What is Apex?

Java-like syntax  
Acts like database stored procedures  
Enables developers to add business logic to system events(button clicks, updates of related records)

### 1) Apex Language Highlights

##### Unlike other OOP languages, Apex supports:
- Cloud development 
- Trigger (ex. when Contact record is created, automatically update Account)
- Database statements that allow you to make direct database calls and query languages to query and search data.
- Transaction and rollbacks
- The global access modifier (more permissive than the public modifier and allow access across namespaces and applications.)
- Versioning of custom code

### 2) Data Types Overview

- A **primitive**
- An **sObject**, either as a generic sObject or as a specific sObject(Account, Contact, MyCustomObject__c)
- A collection, including:
  A ==list== of primitives, sObjects, user defined objects, objects created from Apex classes, or collections  
  A ==set== of primitives, sObjects, user defined objects, objects created from Apex classes, or collections  
  A ==map== from a primitive to a primitive, sObject, or collection
- A typed list of values, also know as an enum
- User-defined Apex classes
- System-supplied Apex classes

### 3) Apex Collection: List

Lists hold an <span style="color:rgb(0, 112, 192)">ordered collection</span> of data of the <span style="color:rgb(0, 112, 192)">same type</span>.



# 2. Use sObjects

## What is sObjects

==Every record== in Salesforce is natively represented as an ==sObject== in Apex.
Common sObject types names in Apex used for standard objects:  
Account, Contact, Lead, Opportunity    
(At first, I confused sObjects as custom objects)

## Work with the Generic sObject Data Type
When you don't know the type of sObject your method is handling, you can use the ==**generic sObject**== data type.


# 3. Manipulate Records with DML



# 4. Write SOQL Queries

# 5. Write SOSL Queries

*permissive 관대한*