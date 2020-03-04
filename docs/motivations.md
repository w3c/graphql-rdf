This document lists the group's motivations and goals.
This data has been gathered based on the [call for introductions in the group's mailinglist](https://lists.w3.org/Archives/Public/public-graphql-rdf/2020Feb/0000.html).


**Motivations:**

* Developers don't want to learn the classic Semantic Web technology stack, or have difficulties with it.

**Concrete goals:**

* GraphQL-over-RDF
    * List, document and compare the various GraphQL-over-RDF approaches + understanding how different use cases have led to the design of these different approaches
    * Define relationship to JSON-LD, SHACL, ShEX, OWL, ...
    * Formal foundation of GraphQL-over-RDF
    * Defining best practices for using GraphQL-over-RDF (possibly even define one or more standard approaches?)
* Mappings between GraphQL (schemas) and other schema languages (SHACL, ShEx): https://github.com/w3c/EasierRDF/issues/64
    * RDF validation using GraphQL schemas

**Meta-goals:**

* Making Semantic Web technology stack accessible to developers to know GraphQL
* Lowering difficulties for writing queries by using GraphQL instead of SPARQL.
* Figuring out if "GraphQL can bring Semantic Web to the Web"
* GraphQL-over-RDF as a solution to federated data access
* GraphQL-over-RDF as a replacement/extension to Ontology Based Data Access
* Provide idiomatic ways to fix GraphQL shortcomings:
    1. To make a subclass, you need to make two things: a type and an interface
    2. No multiple types
    3. Covariance of object types (data) but not input types (operations)
    4. If a mandatory field is missing, the whole object is supposed to bomb out. Then recursively upward...
    5. Prop characteristics can vary per object, which complicates jsonld output.
    6. If a filter var is unset, that can easily break the query.
    7. If object id's (IRIs) are missing in a query, one cannot output them, which is bad for jsonld.