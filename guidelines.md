Please follow this template when creating the migration guides: e.g. from MongoDB to Couchbase Server.

These should be developer focused and must not target one platform only. For example, we can't afford to write a MongoDB to Couchbase Server guide targeted only at Python developers.

# Format

## Sections

Each migration guide should have the following headings:
 * Key differences between tool X and Couchbase Server
  * Keep it factual
 * Data model
 * Query
  * We should emphasise N1QL
    * explain indexing
  * However, views and key-value are still very much part of Couchbase and we should use them where they're the better solution
 * Development model
  * What are the biggest differences in how someone develops against Couchbase Server compared to the origin DBMS?
   * How do our SDKs differ to whatever was available for the origin DBMS?
   * What tooling do we have that offers a replacement for what they use now? (e.g. Ottoman for Mongoose)
   * What tooling will they lose or gain?
   * Show how to perform common operations in Couchbase Server and how they differ
 * Architecture considerations
  * What optimisations might they be making now that are no longer necessary?
 * Tools to help the migration
  * ETL etc
 * Things to look out for
   * Common mistakes/gotchas
 * Example
   * Take everything we've covered and turn it into a full example of moving from the origin DBMS to Couchbase Server

# Example data

We'll use a simple ecommerce data model for each guide. Each guide should bring the reader to a place where they have the following document types in Couchbase Server:

 * customer
 * customer_history (includes order history, products viewed)
 * customer_address (each customer can have multiple addresses and each can be billing, delivery or both)
 * product
 * product_reviews
 * order

#Style

These guides will be published on the blog initially but they form part of our developer documentation. As such, they should be written more like documentation than blog posts. That doesn't mean they need to be dry but you should avoid too informal terminology, referring to yourself and so on.

##Screenshots and code

Screenshots and code samples will help us to make the guide easier to follow and more compelling. 

##Maintenance
We'll write these in Markdown and host them on [GitHub](https://github.com/couchbaselabs/migration-guides).

Each author will be responsible for updating their guide when there is a change in the origin DBMS or Couchbase.