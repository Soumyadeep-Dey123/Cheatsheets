# HTTP Status Codes Cheatsheet

This document provides a comprehensive reference for HTTP status codes, their meanings, and their common use cases.

## Table of Contents

- [1xx: Informational](#1xx-informational)
- [2xx: Success](#2xx-success)
- [3xx: Redirection](#3xx-redirection)
- [4xx: Client Error](#4xx-client-error)
- [5xx: Server Error](#5xx-server-error)
- [Special Notes](#special-notes)
- [References](#references)

## 1xx: Informational

These status codes indicate that the request has been received and the process is continuing.

| Code | Name | Description |
|------|------|-------------|
| **100** | Continue | The server has received the request headers and the client should proceed to send the request body. |
| **101** | Switching Protocols | The server is switching protocols as requested by the client. |
| **102** | Processing | WebDAV - The server has received and is processing the request, but no response is available yet. |
| **103** | Checkpoint | Used in the resumable requests proposal to resume aborted PUT or POST requests. |
| **122** | Request-URI too long | This is a non-standard IE7-specific code, which indicates that the URI is longer than a maximum of 2083 characters. |

## 2xx: Success

These status codes indicate that the client's request was successfully received, understood, and accepted.

| Code | Name | Description |
|------|------|-------------|
| **200** | OK | The request has succeeded. |
| **201** | Created | The request has been fulfilled and resulted in a new resource being created. |
| **202** | Accepted | The request has been accepted for processing, but the processing has not been completed. |
| **203** | Non-Authoritative Information | The server successfully processed the request, but is returning information that may be from another source. |
| **204** | No Content | The server successfully processed the request but is not returning any content. |
| **205** | Reset Content | The server successfully processed the request but is not returning any content. Unlike 204, this response requires the requester to reset the document view. |
| **206** | Partial Content | The server is delivering only part of the resource due to a range header sent by the client. |
| **207** | Multi-Status | WebDAV - The message body that follows is an XML message and can contain a number of separate response codes. |
| **208** | Already Reported | WebDAV - The members of a DAV binding have already been enumerated in a previous reply to this request, and are not being included again. |
| **226** | IM Used | The server has fulfilled a GET request for the resource, and the response is a representation of the result of one or more instance-manipulations applied to the current instance. |

## 3xx: Redirection

These status codes indicate that further action needs to be taken by the client in order to complete the request.

| Code | Name | Description |
|------|------|-------------|
| **300** | Multiple Choices | The requested resource has multiple representations, each with different characteristics. |
| **301** | Moved Permanently | The requested resource has been assigned a new permanent URI. |
| **302** | Found | The requested resource resides temporarily under a different URI. |
| **303** | See Other | The response to the request can be found under a different URI and should be retrieved using a GET method. |
| **304** | Not Modified | The resource has not been modified since the last request. |
| **305** | Use Proxy | The requested resource must be accessed through the proxy given by the Location field. |
| **306** | Switch Proxy | This code is no longer used. It was used in a previous version of the HTTP specification. |
| **307** | Temporary Redirect | The requested resource resides temporarily under a different URI. Unlike 302, the request method should not be changed when reissuing the original request. |
| **308** | Permanent Redirect | The requested resource has been assigned a new permanent URI. Unlike 301, the request method should not be changed when reissuing the original request. |

> **Note:** Status codes 307 and 308 are similar to 302 and 301, but the new request method after redirect must be the same as the initial request method.

## 4xx: Client Error

These status codes indicate that the client seems to have made an error.

| Code | Name | Description |
|------|------|-------------|
| **400** | Bad Request | The server cannot or will not process the request due to an apparent client error. |
| **401** | Unauthorized | Authentication is required and has failed or has not yet been provided. |
| **402** | Payment Required | Reserved for future use. Originally intended for digital payment systems. |
| **403** | Forbidden | The server understood the request but refuses to authorize it. |
| **404** | Not Found | The requested resource could not be found but may be available in the future. |
| **405** | Method Not Allowed | The request method is known by the server but has been disabled and cannot be used. |
| **406** | Not Acceptable | The requested resource is only capable of generating content not acceptable according to the Accept headers sent. |
| **407** | Proxy Authentication Required | Authentication is required with the proxy. |
| **408** | Request Timeout | The server timed out waiting for the request. |
| **409** | Conflict | The request could not be processed because of conflict in the request. |
| **410** | Gone | The requested resource is no longer available and will not be available again. |
| **411** | Length Required | The request did not specify the length of its content, which is required by the requested resource. |
| **412** | Precondition Failed | The server does not meet one of the preconditions specified in the request. |
| **413** | Request Entity Too Large | The request is larger than the server is willing or able to process. |
| **414** | Request-URI Too Long | The URI provided was too long for the server to process. |
| **415** | Unsupported Media Type | The request entity has a media type which the server or resource does not support. |
| **416** | Requested Range Not Satisfiable | The client has asked for a portion of the file, but the server cannot supply that portion. |
| **417** | Expectation Failed | The server cannot meet the requirements of the Expect request-header field. |
| **418** | I'm a teapot | This code was defined in 1998 as an April Fools' joke and is not expected to be implemented by actual HTTP servers. |
| **422** | Unprocessable Entity | WebDAV - The request was well-formed but was unable to be followed due to semantic errors. |
| **423** | Locked | WebDAV - The resource is locked. |
| **424** | Failed Dependency | WebDAV - The request failed due to failure of a previous request. |
| **425** | Unordered Collection | Defined in drafts of WebDAV Advanced Collections, but not present in the final specification. |
| **426** | Upgrade Required | The client should switch to a different protocol. |
| **428** | Precondition Required | The origin server requires the request to be conditional. |
| **429** | Too Many Requests | The user has sent too many requests in a given amount of time. |
| **431** | Request Header Fields Too Large | The server is unwilling to process the request because either an individual header field or all the header fields collectively are too large. |
| **444** | No Response | A non-standard status code used by nginx to indicate that the server has returned no information to the client and closed the connection. |
| **449** | Retry With | A Microsoft extension indicating that the request should be retried after performing the appropriate action. |
| **450** | Blocked By Windows Parental Controls | A Microsoft extension indicating that Windows Parental Controls are blocking access to the given webpage. |
| **451** | Unavailable For Legal Reasons | The server is denying access to the resource as a consequence of a legal demand. |
| **499** | Client Closed Request | A non-standard status code introduced by nginx for the case when a client closes the connection while nginx is processing the request. |

## 5xx: Server Error

These status codes indicate that the server is aware that it has encountered an error or is otherwise incapable of performing the request.

| Code | Name | Description |
|------|------|-------------|
| **500** | Internal Server Error | A generic error message, given when an unexpected condition was encountered and no more specific message is suitable. |
| **501** | Not Implemented | The server either does not recognize the request method, or it lacks the ability to fulfill the request. |
| **502** | Bad Gateway | The server was acting as a gateway or proxy and received an invalid response from the upstream server. |
| **503** | Service Unavailable | The server is currently unavailable (because it is overloaded or down for maintenance). |
| **504** | Gateway Timeout | The server was acting as a gateway or proxy and did not receive a timely response from the upstream server. |
| **505** | HTTP Version Not Supported | The server does not support the HTTP protocol version used in the request. |
| **506** | Variant Also Negotiates | The server has an internal configuration error: transparent content negotiation for the request results in a circular reference. |
| **507** | Insufficient Storage | WebDAV - The server is unable to store the representation needed to complete the request. |
| **508** | Loop Detected | WebDAV - The server detected an infinite loop while processing the request. |
| **509** | Bandwidth Limit Exceeded | A non-standard status code used by many servers to indicate when a bandwidth limit has been exceeded. |
| **510** | Not Extended | Further extensions to the request are required for the server to fulfill it. |
| **511** | Network Authentication Required | The client needs to authenticate to gain network access. |
| **598** | Network read timeout error | A non-standard status code indicating network read timeout behind the proxy. |
| **599** | Network connect timeout error | A non-standard status code indicating network connect timeout behind the proxy. |

## Special Notes

### Code Annotations

- **WebDAV**: Web Distributed Authoring and Versioning extension
- **1.1**: HTTP/1.1 specification
- **GET, POST, PUT**: Applies to these HTTP methods only
- **IE**: Internet Explorer extension
- **MS**: Microsoft extension
- **nginx**: nginx web server extension
- **RFC numbers**: Defined in RFC documents (e.g., 2518, 2817, 2295, etc.)
- **draft**: Proposed draft standard
- **nostd**: Non-standard extension
- **res**: Reserved for future use
- **unused**: No longer in use, deprecated

### WebDAV Status Codes

WebDAV (Web Distributed Authoring and Versioning) is an extension of HTTP that allows clients to perform remote web content authoring operations. It adds several status codes to the HTTP specification:

- 102 Processing
- 207 Multi-Status
- 208 Already Reported
- 422 Unprocessable Entity
- 423 Locked
- 424 Failed Dependency
- 507 Insufficient Storage
- 508 Loop Detected

## References

- This cheatsheet is based on information from [Cheatography](https://cheatography.com/kstep/cheat-sheets/http-status-codes/)
- Original source: [Wikipedia - HTTP Status Codes](http://en.wikipedia.org/wiki/HTTP_status_code)
- [HTTP/1.1 Status Code Definitions (RFC 7231)](https://tools.ietf.org/html/rfc7231)
- [WebDAV Status Codes (RFC 4918)](https://tools.ietf.org/html/rfc4918)
- [Additional HTTP Status Codes (RFC 6585)](https://tools.ietf.org/html/rfc6585)