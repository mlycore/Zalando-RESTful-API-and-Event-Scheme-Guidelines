# Zalando-RESTful-API-and-Event-Scheme-Guidelines
Translation of Zalando RESTful API and Event Scheme Guidelines (https://opensource.zalando.com/restful-api-guidelines/)
---

# Table of Contents
## 1. Introduction

Conventions Used in These Guidelines
Zalando specific information

## 2. Principles

API Design Principles
API as a Product
API First

## 3. General Guidelines

Must: Follow API First Principle
Must: Provide API Specification using OpenAPI
Must: only use Durable and Immutable Remote References
Should: Provide API User Manual
Must: Write APIs in U.S. English

## 4. Meta Information

Must: Contain API Meta Information
Must: Use Semantic Versioning
Must: Provide API Identifiers
Must: Provide API Audience

## 5. Security

Must: Secure Endpoints with OAuth 2.0
Must: Define and Assign Permissions (Scopes)
Must: Follow Naming Convention for Permissions (Scopes)

## 6. Compatibility

Must: Don’t Break Backward Compatibility
Should: Prefer Compatible Extensions
Must: Prepare Clients To Not Crash On Compatible API Extensions
Should: Design APIs Conservatively
Must: Always Return JSON Objects As Top-Level Data Structures To Support Extensibility
Must: Treat Open API Definitions As Open For Extension By Default
Should: Used Open-Ended List of Values (x-extensible-enum) Instead of Enumerations
Should: Avoid Versioning
Must: Use Media Type Versioning
Must: Do Not Use URI Versioning

## 7. Deprecation

Must: Obtain Approval of Clients
Must: External Partners Must Agree on Deprecation Timespan
Must: Reflect Deprecation in API Definition
Must: Monitor Usage of Deprecated APIs
Should: Add a Warning Header to Responses
Should: Add Monitoring for Warning Header
Must: Not Start Using Deprecated APIs

## 8. JSON Guidelines

Must: Property names must be ASCII snake_case (and never camelCase): ^[a-z_][a-z_0-9]*$
Should: Define Maps Using additionalProperties
Should: Array names should be pluralized
Must: Boolean property values must not be null
Must: Use same semantics for null and absent properties
Should: Empty array values should not be null
Should: Enumerations should be represented as Strings
Should: Name date/time properties using the _at suffix
Should: Date property values should conform to RFC 3339
Should: Time durations and intervals could conform to ISO 8601

## 9. Data Formats

Must: Use JSON to Encode Structured Data
May: Use non JSON Media Types for Binary Data or Alternative Content Representations
Should: Prefer standard Media type name application/json
Should: Use standardized property formats
Must: Use Standard Date and Time Formats
Should: Use Standards for Country, Language and Currency Codes
Must: Define Format for Type Number and Integer

## 10. Common Data Types

Must: Use a Common Money Object
Must: Use common field names and semantics

## 11. API Naming

Must/Should: Use Functional Naming Schema
Must: Follow Naming Convention for Hostnames
Must: Use lowercase separate words with hyphens for Path Segments
Must: Use snake_case (never camelCase) for Query Parameters
Should: Prefer Hyphenated-Pascal-Case for HTTP header Fields
Must: Pluralize Resource Names
Should: Not Use /api as Base Path
Must: Avoid Trailing Slashes
Must: Stick to Conventional Query Parameters

## 12. Resources

Must: Avoid Actions — Think About Resources
Should: Model complete business processes
Should: Define useful resources
Must: Keep URLs Verb-Free
Must: Use Domain-Specific Resource Names
Must: Use URL-friendly Resource Identifiers: [a-zA-Z0-9:._-]*
Must: Identify resources and Sub-Resources via Path Segments
Should: Only Use UUIDs If Necessary
May: Consider Using (Non-) Nested URLs
Should: Limit number of Resource types
Should: Limit number of Sub-Resource Levels

## 13. HTTP Requests

Must: Use HTTP Methods Correctly
Must: Fulfill Common Method Properties
Should: Consider To Design POST and PATCH Idempotent
Should: Use Secondary Key for Idempotent POST Design
Must: Define Collection Format of Header and Query Parameters
Should: Design simple query languages using query parameters
Should: Design complex query languages using JSON
Must: Document Implicit Filtering

## 14. HTTP Status Codes And Errors

Must: Specify Success and Error Responses
Must: Use Standard HTTP Status Codes
Must: Use Most Specific HTTP Status Codes
Must: Use Code 207 for Batch or Bulk Requests
Must: Use Code 429 with Headers for Rate Limits
Must: Use Problem JSON
Must: Do not expose Stack Traces

## 15. Performance

Should: Reduce Bandwidth Needs and Improve Responsiveness
Should: Use gzip Compression
Should: Support Partial Responses via Filtering
Should: Allow Optional Embedding of Sub-Resources
Must: Document Cachable GET, HEAD, and POST Endpoints

## 16. Pagination

Must: Support Pagination
Should: Prefer Cursor-Based Pagination, Avoid Offset-Based Pagination
Should: Use Pagination Links Where Applicable

## 17. Hypermedia

Must: Use REST Maturity Level 2
May: Use REST Maturity Level 3 - HATEOAS
Must: Use full, absolute URI
Must: Use Common Hypertext Controls
Should: Use Simple Hypertext Controls for Pagination and Self-References
Must: Not Use Link Headers with JSON Entities

## 18. Common Headers

Must: Use Content-* Headers Correctly
May: Use Standardized Headers
May: Use Content-Location Header
Should: Use Location Header instead of Content-Location Header
May: Consider to Support Prefer Header to Handle Processing Preferences
May: Consider to Support ETag Together With If-Match/If-None-Match Header
May: Consider to Support Idempotency-Key Header

## 19. Proprietary Headers

Must: Use Only the Specified Proprietary Zalando Headers
Must: Propagate Proprietary Headers
Must: Support X-Flow-ID

## 20. API Operation

Must: Publish OpenAPI Specification
Should: Monitor API Usage

## 21. Events

Must: Treat Events as part of the service interface
Must: Make Event schema available for review
Must: Ensure Event schema conforms to Open API Schema Object
Must: Ensure that Events are registered as Event Types
Must: Ensure Events conform to a well-known Event Category
Must: Ensure that Events define useful business resources
Must: Events must not provide sensitive customer personal data
Must: Use the General Event Category to signal steps and arrival points in business processes
Must: Use Data Change Events to signal mutations
Should: Provide a means for explicit event ordering
Should: Use the hash partition strategy for Data Change Events
Should: Ensure that Data Change Events match API representations
Must: Indicate ownership of Event Types
Must: Define Event Payloads in accordance with the overall Guidelines
Must: Maintain backwards compatibility for Events
Should: Avoid additionalProperties in event type definitions
Must: Use unique Event identifiers
Should: Design for idempotent out-of-order processing
Must: Follow Naming Convention for Event Type Names
Must: Prepare for duplicate Events

## Appendix A: References

OpenAPI Specification
Publications, specifications and standards
Dissertations
Books
Blogs

## Appendix B: Tooling

API First Integrations
Support Libraries

## Appendix C: Best Practices

Optimistic Locking in RESTful APIs

## Appendix D: Changelog

Rule Changes

