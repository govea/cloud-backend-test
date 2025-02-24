# Superformula Cloud Backend Test

Be sure to read **all** of this document carefully, and follow the guidelines within.

### Summary

Please build an GraphQL API that manages Users and respects the following data model:

```
{
  "id": "xxx",                  // user ID (must be unique)
  "name": "backend test",       // user name
  "dob": "",                    // date of birth
  "address": "",                // user address
  "description": "",            // user description
  "createdAt": "",              // user created date
  "updatedAt": "",              // user updated date
  "imageUrl": ""                // user avatar image url
}
```

### Requirements

#### Functionality

1. This should be a GraphQL API that can `create`, `read`, `update`, and `delete` a given user
1. The API should follow typical GraphQL API design patterns
1. Please store data from all write operations to a persistence database
1. Proper error handling should be used
1. Paginating and filtering (by name) users list
1. The API should have a Query to fetch geolocation information based off an address

#### Tech Stack
  - Use of **Typescript** is required 
  - **Please use Infrastructure-as-code tooling** that can be used to deploy all resources to AWS. 
    - Terraform (preferred)
    - CloudFormation / SAM
    - Serverless Framework
    - AWS CDK
  - Use AWS Lambda + API Gateway or AWS AppSync is recommended
  - Use any AWS Database-as-a-Service persistence store
  - Location query must use [NASA](https://api.nasa.gov/) or [Mapbox](https://www.mapbox.com/api-documentation/) APIs to resolve the coordinate based on the address; use AWS Lambda.

#### Developer Experience 
- Write unit tests for business logic
- Write concise and clear commit messages
- Document and diagram the architecture of your solution
- Write clear documentation:
    - Repository structure
    - Environment variables and any defaults.
    - How to build/run/test the solution
    - Deployment guide

### Bonus

These may be used for further challenges. You can freely skip these; feel free to try out if you feel up to it.

#### Developer Experience (in order)

1. E2E Testing
1. Integration testing
1. Code-coverage report generation
1. Describe your strategy for Lambda error handling, retries, and DLQs
1. Describe your cloud-native logging, monitoring, and alarming strategy across all queries/mutations
1. Online interactive demo with a publicly accessible link to your API
1. Brief description of the frameworks/tools used in the solution
1. Optimized lambda build.
1. Commit linting
1. Semantic release


#### API Consumer Experience (in order)

1. Document how consumers can quickly prototype against your APIs
    - GraphQL Playground setup
    - Insomnia/Postman setup
    - Feel free to use any other tool/client you might know that enable consumers to prototype against your API
1. GraphQL Documentation Generation
1. Client API/SDK generation


## Frontend Wireframes/Mockups (Do not implement those screens)

Assume the GraphQL API you are developing will be used by a hypothetical front-end team to build the following screens:

![Superformula-front-end-test-mockup](./mockup1.png)

![Superformula-front-end-test-mockup-2](./mockup2.png)

> [Source Figma file](https://www.figma.com/file/hd7EgdTxJs2fpTzzSKlNxo/Superformula-full-stack-test)

- Client will be performing real-time search against this API
- List of users should be updated automatically after single user is updated

## What We Care About

Use any libraries that you would normally use if this were a real production App. Please note: we're interested in your code & the way you solve the problem, not how well you can use a particular library or feature.

_We're interested in your method and how you approach the problem just as much as we're interested in the end result._

Here's what you should strive for:

- Good use of current Typescript, Node.js, GraphQL & performance best practices.
- Solid testing approach.
- Extensible code and architecture.
- Delightful experience for other backend engineers working in this repository
- Delightful experience for engineers consuming your APIs

## Q&A

> How should I start this code challenge?

Fork this repo to your own account and make git commits to add your code as you would on any other project.

> Where should I send back the result when I'm done?

Send us a pull request when you think you are done. There is no deadline for this task unless otherwise noted to you directly.

> What if I have a question?

Create a new issue [in this repo](https://github.com/Superformula/cloud-backend-test/issues) and we will respond and get back to you quickly.

> Should I validate inputs?

Please assume a hard requirement has not been set by the product owner. We welcome any input validations and your reasoning for why they add value.

> What is the location format?

Examples:
- Seattle, Washington
- Digital Nomad
- New Jersey
- Northern Bergen County, NJ

> I almost finished, but I don't have time to create everything what is required

Please provide a plan for the rest of the things that you would do.
