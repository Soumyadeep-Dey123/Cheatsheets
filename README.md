# HTTP Status Codes Cheat Sheet

A comprehensive reference guide to HTTP status codes, categorized based on their type and function.

## 📌 Table of Contents
- [1xx: Informational Codes](#1xx-informational-codes)
- [2xx: Successful Codes](#2xx-successful-codes)
- [3xx: Redirection Codes](#3xx-redirection-codes)
- [4xx: Client Error Codes](#4xx-client-error-codes)
- [5xx: Server Error Codes](#5xx-server-error-codes)
- [Additional Information](#additional-information)

---

## 1xx: Informational Codes
Status codes in this category indicate that the request was received and the process is continuing.

| Code | Meaning |
|------|---------|
| 100  | Continue |
| 101  | Switching Protocols |
| 102  | Processing (WebDAV) |
| 103  | Checkpoint (Draft, POST, PUT) |
| 122  | Request-URI too long (IE7) |

---

## 2xx: Successful Codes
These status codes confirm that the client's request was successfully received, understood, and accepted.

| Code | Meaning |
|------|---------|
| 200  | OK |
| 201  | Created |
| 202  | Accepted |
| 203  | Non-Authoritative Information (HTTP/1.1) |
| 204  | No Content |
| 205  | Reset Content |
| 206  | Partial Content |
| 207  | Multi-Status (WebDAV 4918) |
| 208  | Already Reported (WebDAV 5842) |
| 226  | IM Used (RFC 3229) |

---

## 3xx: Redirection Codes
These status codes indicate that further action is needed to complete the request.

| Code | Meaning |
|------|---------|
| 300  | Multiple Choices |
| 301  | Moved Permanently |
| 302  | Found |
| 303  | See Other (HTTP/1.1) |
| 304  | Not Modified |
| 305  | Use Proxy (HTTP/1.1) |
| 306  | Switch Proxy (Unused) |
| 307  | Temporary Redirect (HTTP/1.1) |
| 308  | Permanent Redirect (RFC 7538) |

ℹ️ **Note:** `307` and `308` behave like `302` and `301`, but they enforce the same request method as the initial request.

---

## 4xx: Client Error Codes
These status codes indicate an error caused by the client.

| Code | Meaning |
|------|---------|
| 400  | Bad Request |
| 401  | Unauthorized |
| 402  | Payment Required (Reserved) |
| 403  | Forbidden |
| 404  | Not Found |
| 405  | Method Not Allowed |
| 406  | Not Acceptable |
| 407  | Proxy Authentication Required |
| 408  | Request Timeout |
| 409  | Conflict |
| 410  | Gone |
| 411  | Length Required |
| 412  | Precondition Failed |
| 413  | Request Entity Too Large |
| 414  | Request-URI Too Long |
| 415  | Unsupported Media Type |
| 416  | Requested Range Not Satisfiable |
| 417  | Expectation Failed |
| 418  | I'm a teapot (RFC 2324) ☕ |
| 422  | Unprocessable Entity (WebDAV 4918) |
| 423  | Locked (WebDAV 4918) |
| 424  | Failed Dependency (WebDAV 4918) |
| 425  | Unordered Collection (RFC 3648) |
| 426  | Upgrade Required (RFC 2817) |
| 428  | Precondition Required (Draft) |
| 429  | Too Many Requests (Draft) |
| 431  | Request Header Fields Too Large (Draft) |
| 444  | No Response (nginx) |
| 449  | Retry With (Microsoft) |
| 450  | Blocked By Windows Parental Controls (Microsoft) |
| 451  | Unavailable For Legal Reasons (Draft) |
| 499  | Client Closed Request (nginx) |

---

## 5xx: Server Error Codes
These status codes indicate a server-side failure.

| Code | Meaning |
|------|---------|
| 500  | Internal Server Error |
| 501  | Not Implemented |
| 502  | Bad Gateway |
| 503  | Service Unavailable |
| 504  | Gateway Timeout |
| 505  | HTTP Version Not Supported |
| 506  | Variant Also Negotiates (RFC 2295) |
| 507  | Insufficient Storage (WebDAV 4918) |
| 508  | Loop Detected (WebDAV 5842) |
| 509  | Bandwidth Limit Exceeded (Non-Standard) |
| 510  | Not Extended (RFC 2774) |
| 511  | Network Authentication Required (Draft) |
| 598  | Network Read Timeout Error (Non-Standard) |
| 599  | Network Connect Timeout Error (Non-Standard) |

---

## Additional Information
- **WebDAV**: Web Distributed Authoring and Versioning extension
- **HTTP/1.1**: Indicates status codes introduced in HTTP/1.1
- **Draft**: Proposed status codes under discussion
- **Non-Standard (nostd)**: Custom codes used in specific implementations
- **RFC Numbers**: Standards documentation where the codes are specified
- **MS (Microsoft-specific)** and **nginx-specific** extensions

📝 **Sources:** [HTTP Status Codes](https://cheatography.com/kstep/cheat-sheets/http-status-codes/)

---

📌 **Contributing**
If you notice any missing codes or errors, feel free to submit a pull request!

📌 **License**
This cheat sheet is open-source and freely available for use and modification.
