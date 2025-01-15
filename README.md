## **1xx: Informational**
These codes indicate that the request has been received and is being processed.

### **100 Continue**
- **Explanation**: The server has received the request headers and the client can proceed to send the request body.
- **When to use**: Used during chunked data transfer or large file uploads to verify headers before proceeding.

### **101 Switching Protocols**
- **Explanation**: The server agrees to switch protocols as requested by the client (e.g., upgrading to WebSocket).
- **When to use**: Use during protocol upgrades like switching from HTTP/1.1 to WebSocket.

### **102 Processing (WebDAV)**
- **Explanation**: The server has received and is processing the request, but no response is yet available.
- **When to use**: Use when processing will take significant time to indicate the server is working.

---

## **2xx: Success**
These codes indicate that the action was successfully received, understood, and accepted.

### **200 OK**
- **Explanation**: The request was successful, and the response body contains the requested data.
- **When to use**: General success cases, such as returning a resource or result of an operation.

### **201 Created**
- **Explanation**: The request was successful, and a new resource was created.
- **When to use**: Use for resource creation operations, e.g., creating a user or adding a record.

### **202 Accepted**
- **Explanation**: The request has been accepted for processing but is not yet completed.
- **When to use**: Use for asynchronous operations, where processing happens later.

### **203 Non-Authoritative Information**
- **Explanation**: The request was successful, but the returned metadata is not from the origin server.
- **When to use**: Rarely used; when returning transformed or proxied data.

### **204 No Content**
- **Explanation**: The request was successful, but there is no content to send in the response.
- **When to use**: Use for operations like delete or updates that don't need a response body.

### **205 Reset Content**
- **Explanation**: The client should reset the document view (e.g., form reset).
- **When to use**: Rarely used, but appropriate after actions like clearing user input.

### **206 Partial Content**
- **Explanation**: Only part of the resource is being sent due to a range request.
- **When to use**: Use for downloading files in chunks.

---

## **3xx: Redirection**
These codes indicate the client must take additional action to complete the request.

### **300 Multiple Choices**
- **Explanation**: Indicates multiple options for the resource.
- **When to use**: Use when a resource can be served in different ways, like different formats.

### **301 Moved Permanently**
- **Explanation**: The requested resource has been permanently moved to a new URL.
- **When to use**: Use when redirecting to a new URL permanently.

### **302 Found**
- **Explanation**: The requested resource is temporarily located at a different URL.
- **When to use**: Use for temporary redirections.

### **303 See Other**
- **Explanation**: The response is at a different URL, accessible with a GET request.
- **When to use**: Use after successful actions like form submissions.

### **304 Not Modified**
- **Explanation**: The resource has not changed since the last request.
- **When to use**: Use for caching optimization.

### **307 Temporary Redirect**
- **Explanation**: The resource is temporarily moved to another URL. The HTTP method must not change.
- **When to use**: Use for temporary redirects where method preservation is required.

### **308 Permanent Redirect**
- **Explanation**: The resource is permanently moved to another URL. The HTTP method must not change.
- **When to use**: Use for permanent redirects where method preservation is required.

---

## **4xx: Client Errors**
These codes indicate an error caused by the client.

### **400 Bad Request**
- **Explanation**: The request is invalid or malformed.
- **When to use**: Use for validation errors or incorrect query parameters.

### **401 Unauthorized**
- **Explanation**: Authentication is required but has failed or not been provided.
- **When to use**: Use when a user needs to log in or provide credentials.

### **403 Forbidden**
- **Explanation**: The server understands the request but refuses to authorize it.
- **When to use**: Use for access control violations, e.g., insufficient permissions.

### **404 Not Found**
- **Explanation**: The requested resource does not exist on the server.
- **When to use**: Use when a URL or resource is invalid or doesn't exist.

### **405 Method Not Allowed**
- **Explanation**: The HTTP method is not allowed for the requested resource.
- **When to use**: Use when a resource does not support a specific HTTP method.

### **409 Conflict**
- **Explanation**: The request conflicts with the current state of the resource.
- **When to use**: Use for duplicate records or conflicts, e.g., "User already exists."

### **422 Unprocessable Entity**
- **Explanation**: The request was well-formed but cannot be processed due to semantic errors.
- **When to use**: Use for domain-specific validation errors.

### **429 Too Many Requests**
- **Explanation**: The client has sent too many requests in a given period.
- **When to use**: Use for rate-limiting responses.

---

## **5xx: Server Errors**
These codes indicate an error caused by the server.

### **500 Internal Server Error**
- **Explanation**: A generic server error occurred.
- **When to use**: Use for unexpected errors or unhandled exceptions.

### **501 Not Implemented**
- **Explanation**: The server does not support the functionality required to fulfill the request.
- **When to use**: Use for features not yet implemented.

### **503 Service Unavailable**
- **Explanation**: The server is temporarily unavailable due to overload or maintenance.
- **When to use**: Use for planned maintenance or downtime.

### **504 Gateway Timeout**
- **Explanation**: The server did not receive a timely response from an upstream server.
- **When to use**: Use for timeouts in APIs or services.
