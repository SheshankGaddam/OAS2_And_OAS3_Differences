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

| Feature                      | OAS2 (Swagger 2.0)                                | OAS3 (OpenAPI 3.0)                                |
|-----------------------------|---------------------------------------------------|---------------------------------------------------|
| **Specification Version**   | `swagger: '2.0'`                                  | `openapi: 3.0.1`                                  |
| **Base Path**               | `basePath` used                                   | Replaced by `servers` object                     |
| **Request Body**            | Defined as a parameter in `in: body`              | Defined using `requestBody` object               |
| **Content Type**            | `consumes` and `produces`                         | Defined under `content` with media types         |
| **Components**              | `definitions`, `parameters`, `responses`          | Unified under `components`                       |
| **Parameter Location**      | `in: body`, `in: query`, `in: header`, etc.       | Same, but `in: body` replaced by `requestBody`   |
| **Multiple Examples**       | Not natively supported                            | Supported using `examples` object                |
| **Callbacks & Links**       | Not supported                                     | Supported                                         |

---

## 🧪 Example: CustomerDetails API

Both specifications define the following endpoints:

- `GET /getCustomerById` (query param)
- `GET /getCustomerById/{UserId}` (path param)
- `POST /createCustomer` (request body)

Each version demonstrates how these endpoints are modeled differently in OAS2 and OAS3.

---

## 🚀 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/openapi-spec-swagger-examples.git
   ```
