OpenAPI 3.0
June, 2018
Mike Ralphson - Mermade Software

---

Mike Ralphson
Independent Software Consultant
Mermade Software
Member, OpenAPI Initiative Technical Steering Committee

---

Introduction - What is the OpenAPI Specification

“[The] OpenAPI specification defines a standard, programming language-agnostic interface description for REST APIs, which allows both humans and computers to discover and understand the capabilities of a service without requiring access to source code, additional documentation, or inspection of network traffic. When properly defined via OpenAPI, a consumer can understand and interact with the remote service with a minimal amount of implementation logic. Similar to what interface descriptions have done for lower-level programming, the OpenAPI Specification removes guesswork in calling a service.”
OpenAPI specification defines a standard, programming language-agnostic interface description for REST APIs, which allows both humans and computers to discover and understand the capabilities of a service without requiring access to source code, additional documentation, or inspection of network traffic. When properly defined via OpenAPI, a consumer can understand and interact with the remote service with a minimal amount of implementation logic. Similar to what interface descriptions have done for lower-level programming, the OpenAPI Specification removes guesswork in calling a service.

---

# What does that mean?

OpenAPI documents describe the public surface area of a RESTful API

* Provides machine-readable interface documentation
* Formerly known as the Swagger specification
* Like WSDL for SOAP / web-services, but can be easily hand-generated
* Supports HTTP(S), websockets, webhooks
* Does not support async (MQ)  / gRPC / GraphQL APIs
* See AsyncAPI
* Not ‘true’ REST / Hypermedia - Richardson Maturity Model 2+

---

Describing the surface area of your API

Metadata
Name
Version
Server(s)
Description
License/Terms
External documentation
Security
Paths/Operations
Templated paths
HTTP methods
Parameters
Request Bodies
Responses
Callbacks (new)
Links (new)

Schemas
Define the shape of objects sent and received as part of the API contract.
OpenAPI documents are written in JSON or YAML format using JSON schema but schemas may map to any media-type (including XML).
List of paths or routes for the API, within that, operations or the HTTP methods used to call the operations, within that, parameters, the request body (if any) which is sent, and a list of responses expected.

---

# What does one look like?

*Schema for the comic object, with properties and types. Can be as complex as you want. JSON schema permitting.*

---

# Why would we do this?

Because human (only)-readable documentation sucks.

*It’s verbose, out of date, incomplete etc.*

---

Interactive documentation.

API consoles / testing tools, such as swagger-ui or postman

Static documentation, such as widdershins, swagger2slate etc

Client and server SDK generation (CLI / programmatic / API versions of these tools also exist - Swagger codegen). Support more languages than you can manually.

Editors for design-first development

Mocking / testing

---

# What’s new in OpenAPI 3.0.x

* Server variables - dynamic hosts

* Better JSON schema (Draft 5) support (oneOf, anyOf, not)

* Callbacks - allowing webhooks to be defined
Defined in exactly the same way: path -> operations -> parameters etc

* Links - a step towards hypermedia. Identify potential links in responses, how to map parameters, and specify which operations they map to

---

# Design first or code-first?

## Design-first:

* Generate client and server code from API definition
* Dynamic or static one-time only generation?
* How to keep code in sync with API changes?

## Code-first:

* Generate API definition from annotations
* Definition always agrees with implementation
* More definition churn?

---

# Discoverability - Schema.org WebAPI type

---

# Documentation - how not to do it

> please ignore the API documentation below, it's nonsense! please go to https://www.avatarapi.com/ and scroll down to the "XML API"

---

# One standard to /bring them all, and in the darkness {bind} them

## Alternatives

* RAML (modelling / reuse focus)
* API Blueprint (markdown based)
* Mashery IODocs (dead?)
* Google Discovery format (proprietary)
* WADL (why WADL when you can Swagger?)

---

# Collections and integrations

* APIs.guru - 1,600+ definitions 
* SwaggerHub - edit / mock / SDKs
* DataFire - like IFTTT
* AnyAPI - docs / consoles
* RestFul API Modelling Language, Web API Description Language.

---

# Get involved

* https://github.com/OAI/OpenAPI-Specification
* It’s just markdown - issue a Pull Request
* https://github.com/APIs-guru/awesome-openapi3
* Find and promote OpenAPI implementations
* https://github.com/APIs-guru/openapi-directory 
* Find and promote API definitions

---

# STICKERS ARE COOL!

*I don’t know who you need to … impress to become an OpenAPI ambassador.*

*I guess it’s one of these guys.*

---

It was the Dawn of the Third Age of Mankind, ten years after the Swagger-RAML War. The OpenAPI Project was a dream given form.

---

Questions?
