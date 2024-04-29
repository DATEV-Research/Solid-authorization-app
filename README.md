# AuthorizationApp - Portable, Reusable Solid App for GDPR-compliant Access Granting

One of the key principles of the Solid concept, the ability to dynamically bind an identity to a Solid application and a Solid pod, means that users must frequently process data access requests on demand and grant or deny them or revoke existing access rights to data. Processing and managing such access requests and access rights in a Solid environment requires a comparatively high number of HTTP requests.

To enable efficient handling of these tasks and to prevent the need to re-implement this functionality for new use cases, we developed a prototype of a reusable web-based user interface to grant access to data in a Solid Pod, the *AuthorizationApp*. 
The application allows both the monitoring and processing of received, existing, rejected, and revoked requests for data sharing. 

By design, the AuthorizationApp is not integrated directly into the business applications. The Authorization Agent, resp. the application, for a given Social Agent can be discovered by de-referencing the identity of that Social Agent, and extracting the object value of the `interop:hasAuthorizationAgent` statement defined in the W3C Solid Community Group's Application Interoperability Specification from the Social Agent graph in the returned identity profile document.
Further, we designed the application to avoid the need to copy or store data outside the personal / company context, meaning all data remains under the user's / company's control.
By this, any business app just needs to redirect the web browser to the corresponding IRI to provide the user with the functionality of data sharing. 

# To start the AuthApp locally run:

- npm install
- npm run serve
