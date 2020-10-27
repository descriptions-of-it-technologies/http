# Hypertext Transfer Protocol. HTTP.





## Contents at a Glance.
* [About](#about)
* [Documentation.](#documentation)
* [HTTP/0.9](https://github.com/descriptions-of-it-technologies/http-0.9)
* [HTTP/1.0](https://github.com/descriptions-of-it-technologies/http-1.0)
* [HTTP/1.1](https://github.com/descriptions-of-it-technologies/http-1.1)
* [HTTP/2.0](https://github.com/descriptions-of-it-technologies/http-2.0)
* [HTTP/3.0](https://github.com/descriptions-of-it-technologies/http-3.0)
* [HTTPS](https://github.com/descriptions-of-it-technologies/https)
* [Request Methods.](#request-methods)
* [Safe HTTP Methods.](#safe-http-methods)
* [Idempotent HTTP Methods.](#idempotent-http-methods)
* [Non-Idempotent HTTP Methods.](#non-idempotent-http-methods)
* [Graphic HTTP Methods.](#graphic-http-methods)
* [HTTP Status Codes.](#http-status-codes)
* [Common HTTP Status Codes.](#common-http-status-codes)
* [HTTP Method GET.](#http-method-get)
* [HTTP Method PUT.](#http-method-put)
* [HTTP Method POST.](#http-method-post)
* [HTTP Method DELETE.](#http-method-delete)
* [Help](#help)





## About.





## Documentation.
* [HTTP Methods.](https://restfulapi.net/http-methods/)





## Request Methods.
* Request methods, also known as verbs, are used to indicate the desired action to be performed.
* GET - is a request for a resource (html file, javascript file, image, etc).
* GET - is used when you visit a website.
* HEAD - is like GET, but only asks for meta information without the body.
* POST - is used to post data to the server.
* Typical use case for POST is to post form data to the server (like a checkout form).
* PUT - is a request for the enclosed entity be stored at the supplied URI. If the entity exists, it is expected to be updated.
* POST is a create request.
* PUT is a create OR update request.
* DELETE - Is a request to delete the specified resource.
* TRACE - Will echo the received request. Can be used to see if request was altered by intermediate servers.
* OPTIONS - Returns the HTTP methods supported by the server for the specified URL.
* CONNECT - Converts the request to a transparent TCP/IP tunnel, typically for HTTPS through an unencrypted HTTP proxy.
* PATCH - Applies partial modifications to the specified resource.





## Safe HTTP Methods.
* Safe Methods are considered safe to use because they only fetch information and do not cause changes on the server.
* The Safe Methods are: GET, HEAD, OPTIONS, and TRACE.





## Idempotent HTTP Methods.
* Idempotence - A quality of an action such that repetitions of the action have no further effect on the outcome.
* PUT and DELETE are Idempotent Methods.
* Safe Methods (GET, HEAD, TRACE, OPTIONS) are also Idempotent.
* Being truly Idempotent is not enforced by the protocol.





## Non-Idempotent HTTP Methods.
* POST is NOT Idempotent
* Multiple Posts are likely to create multiple resources
* Ever seen websites asking you to click submit only once?





## Graphic HTTP Methods. 

|  HTTP Method  |  Request Body  |  Response Body  |  Safe  |  Idempotent  |  Cacheable  |
| ------------- | -------------- | --------------- | ------ | ------------ | ----------- |
| GET           | No             | Yes             | Yes    | Yes          | Yes         |
| HEAD          | No             | No              | Yes    | Yes          | Yes         |
| POST          | Yes            | Yes             | No     | No           | Yes         |
| PUT           | Yes            | Yes             | No     | Yes          | No          |
| DELETE        | No             | Yes             | No     | Yes          | No          |
| CONNECT       | Yes            | Yes             | No     | No           | No          |
| OPTIONS       | Optional       | Yes             | Yes    | Yes          | No          |
| TRACE         | No             | Yes             | Yes    | Yes          | No          |
| PATCH         | Yes            | Yes             | No     | No           | Yes         |





## HTTP Status Codes:
* 100 - series are informational in nature.
* 200 - series indicate successful request.
* 300 - series are redirections.
* 400 - series are client errors.
* 500 - series are server side errors.





## Common HTTP Status Codes:
* 200 Okay; 201 Created; 204 Accepted.
* 301 Moved Permanently.
* 400 Bad Request; 401 Not Authorized; 404 Not Found.
* 500 Internal Server Error; 503 Service Unavailable.





## HTTP Method GET.
* Use: to read data from resource.
* Read only.
* Idempotent.
* Safe operation - does not change state of resource.





## HTTP Method PUT.
* Use: to insert (if not found) or update (if found).
* Idempotent - Multiple PUTs will not change result.
* Like saving a file multiple times.
* Not Safe operation - does change state of resource.





## HTTP Method POST.
* Use: to create new object (insert).
* Non-Idempotent - Multiple POSTs is expected to create multiple objects.
* Not Safe operation - does change state of resource.
* Only Non-Idempotent, Non-Safe HTTP verb.





## HTTP Method DELETE.
* Use: to delete an object (resource).
* Idempotent - Multiple DELETEs will have same effects/behaviour.
* Not Safe operation - does change state of resource.





## Help.
