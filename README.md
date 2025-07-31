# OAS2_And_OAS3_Differences
A comprehensive repository showcasing Swagger examples for OpenAPI Specification 2.0 and 3.0, along with a detailed comparison of their key differences.

# OpenAPI Specification Swagger Examples

This repository contains Swagger definitions for both **OpenAPI Specification 2.0 (OAS2)** and **OpenAPI Specification 3.0 (OAS3)**. It also highlights the key differences between the two specifications using a common example: `CustomerDetails`.

---

## 📁 Contents

- `oas2/customer-details-oas2.yaml`: Swagger file using OAS2
- `oas3/customer-details-oas3.yaml`: Swagger file using OAS3
- Key differences between OAS2 and OAS3


---

## 📊 Key Differences Between OAS2 and OAS3

| Feature                     | OAS2 (Swagger 2.0)                                | OAS3 (OpenAPI 3.0)                                |
|----------------------------|---------------------------------------------------|---------------------------------------------------|
| **Specification Version**  | `swagger: '2.0'`                                  | `openapi: 3.0.x`                                  |
| **Base URL**               | `host`, `basePath`, `schemes`                     | `servers` array                                   |
| **Request Body**           | Defined as a parameter with `in: body`            | Defined using `requestBody` object                |
| **Content Negotiation**    | `consumes` and `produces`                         | `content` object with media types                 |
| **Reusable Components**    | `definitions`, `parameters`, `responses`          | Unified under `components`                        |
| **Parameter Types**        | `in: query`, `in: path`, `in: header`, `in: body` | Same, but `in: body` replaced by `requestBody`    |
| **Multiple Examples**      | Not natively supported                            | Supported using `examples` object                 |
| **Callbacks & Links**      | Not supported                                     | Supported                                         |
| **Security Definitions**   | `securityDefinitions`                             | `securitySchemes` under `components`              |
| **File Uploads**           | `type: file` in formData                          | `type: string`, `format: binary` in requestBody   |

---

## 🧪 Swagger Example Explanation

### ✅ Common API: `CustomerDetails`

This API includes three endpoints:

1. **GET /getCustomerById**  
   - Accepts `UserId` as a query parameter and `Organization` as a header.
   - Returns a `customer` object.

2. **GET /getCustomerById/{UserId}**  
   - Accepts `UserId` as a path parameter.
   - Returns a `customer` object.

3. **POST /createCustomer**  
   - Accepts a `customer` object in the request body.
   - Returns a success message.

### 🔍 OAS2 Highlights

- Uses `swagger: '2.0'`
- Defines request body using `parameters` with `in: body`
- Uses `definitions` for schema reuse
- Specifies `consumes` and `produces` for content types

### 🔍 OAS3 Highlights

- Uses `openapi: 3.0.1`
- Introduces `requestBody` for body payloads
- Uses `components/schemas` for reusable models
- Replaces `basePath` with `servers`

---

## 🚀 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/openapi-swagger-oas2-vs-oas3.git
