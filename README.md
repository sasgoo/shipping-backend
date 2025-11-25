# Backend Team README


This README is specifically prepared for the **Back-end Team** working on the Shipping Project. Your responsibility is to build the API, handle the business logic, manage database operations, and ensure stable communication between the front-end and the server.

## Your Role in the Project

The Back-end team is responsible for:

* Building all REST API endpoints
* Implementing the system's business logic
* Managing database operations (CRUD)
* Securing the API and validating requests
* Returning structured and clean JSON responses
* Ensuring smooth integration with the Front-end team

## Repository Structure

Expected structure for the back-end repository:

shipping-backend/
│
├── src/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── services/
│   ├── middleware/
│   ├── config/
│   └── utils/
│
├── database/
├── package.json
└── README.md



## API Development

The API must follow a clean and consistent structure. All endpoints will be documented in the file:

### **API-SPEC.md**


* API endpoints
* HTTP methods (GET, POST, PUT, DELETE)
* Request body format
* Response JSON format
* Error examples

### Example Endpoint

POST /api/shipments
Request:
{
  "sender": "string",
  "receiver": "string",
  "address": "string",
  "weight": 3.5
}

Response:
{
  "status": "success",
  "shipmentId": "12345",
  "message": "Shipment created successfully"
}




## Database Responsibilities

The back-end team handles:

* Creating database schema
* Writing queries or ORM models
* Ensuring proper relationships between tables
* Handling migrations (if needed)
* Securing sensitive information (credentials, tokens)

Supported database examples:

* PostgreSQL


## Error Handling & Validation

Every endpoint must:

* Validate incoming data
* Handle missing or invalid fields
* Return proper error messages such as:

{
  "status": "error",
  "message": "Invalid request body"
}

## Security Guidelines

* Do not expose keys or secrets
* Use environment variables
* Sanitize all inputs
* Protect routes when needed (Auth middleware)


## Integration with Front-end

The API will be consumed by the front-end using HTTP requests.
Back-end must:

* Ensure CORS is configured correctly
* Return consistent JSON
* Document any changes immediately
* Communicate if an endpoint is updated


## Weekly Updates

All back-end members must provide:

* Completed endpoints
* Pending tasks
* Issues or blockers (database, logic, etc.)
* Any integration problems


## Tools & Technologies (Back-end)

The back-end stack includes:


Runtime Environment             Node.js                                                            
Main Framework                    NestJS (TypeScript)                                                
Programming Language        TypeScript                                                          ORM                                       Prisma ORM                                                         
Architecture                             Modular Monolithic → Microservices (scalable for future expansion) 
Real-time Communication       Socket.io                                                          
GitHub for collaboration

Install dependencies with:

npm install

## Final Deliverables

Back-end team must deliver:

* Fully functional API
* Database schema + seed data if needed
* Clean and organized folder structure
* Unit tests (if applicable)
* API documentation file (API-SPEC.md)
* Successful integration with front-end
