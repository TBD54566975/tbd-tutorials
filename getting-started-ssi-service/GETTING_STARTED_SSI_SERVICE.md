# Getting Started with the SSI Service

---

**NOTE**
This tutorial is adapted from a 
[blog post](https://frankhinek.com/getting-started-with-tbds-ssi-service/)
by [Frank Hinek](https://twitter.com/frankhinek).

---

This tutorial will focus on the 
[Self-Sovereign Identity Service](https://github.com/TBD54566975/ssi-service),
a RESTful web service that leverages the 
[Self-Sovereign Identity SDK](https://github.com/TBD54566975/ssi-sdk) (SSI SDK). The 
SSI Service will eventually incorporate a broad range of functionality relating to 
interaction with [DIDs](https://www.w3.org/TR/did-core/), 
[Verifiable Credentials](https://www.w3.org/TR/vc-data-model), and 
[Decentralized Web Node](https://identity.foundation/decentralized-web-node/spec/) (DWN) 
messaging. This tutorial covers the following features:

* DID Management
* Verifiable Credential Schema Management
* Mock Verifiable Credential Issuance & Verification

This tutorial will cover the following:

* How to run the SSI Service locally
* How to use the SSI Service to:
  * Create a DID key
  * Create a Verifiable Credential schema
  * Issue a Verifiable Credential

## Prerequisites

