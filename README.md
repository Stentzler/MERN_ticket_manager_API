# Support App

- Website: https://frontend-iota-lilac-23.vercel.app/
- API: https://stentzlersupportservice.onrender.com

## Tecnologias utilizadas:

- React
- Node.JS
- Express
- MongoDB
- Mongoose

## Deploy services:

- Front-end: [Vercel](https://vercel.com/)
- Back-end: [Render](https://render.com/)

# API Endpoints:

BASE_URL: https://stentzlersupportservice.onrender.com

## 1.0 - User_Routes

### 1.0.1 - Create_User

- POST /api/users
- Expected body request example:

```json
{
	"name": "test",
	"email": "test@gmail.com",
	"password": "test1234"
}
```

### 1.0.2 - Get_User_Profile

- GET /api/users/me
- No body request needed.
- User token required.

### 1.0.3 - User_Login

- POST /api/users/login
- No token required.
- Expected body request example:

```json
{
	"email": "Teste",
	"password": "teste1234"
}
```

## 2.0 - Ticket_Routes

### 2.0.1 - Create_Tickets

- POST /api/tickets
- Token required.
- Expected body request example:

```json
{
	"product": "iPhone",
	"description": "Not turning on"
}
```

### 2.0.2 - Get_Tickets

- GET /api/tickets
- Token required
- No body request

### 2.0.3 - Get_Single_Ticket

- GET /api/tickets/:ticket_id
- Token required
- No body request
-

### 2.0.4 - Update_Ticket

- PUT /api/tickets/:ticket_id
- Token required
- Expected body request example:

```json
{
	"product": "iPad",
	"description": "Screen cracked"
}
```

### 2.0.5 - Delete_Ticket

- DELETE /api/tickets/:ticket_id
- Token required
- No body request

## 3.0 - Notes_Routes

### 3.0.1 - Create_Ticket_Note

- POST /api/tickets/:ticket_id/notes
- Token required.
- Expected body request example:

```json
{
	"text": "Just an example"
}
```

### 3.0.2 - Get_Ticket_Note

- GET /api/tickets/:ticket_id/notes
- Token required.
- No body request.
