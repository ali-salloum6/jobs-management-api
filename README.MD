# Jobs management API
A NodeJS/Express API for tracking and managing job applications for different users. It utilizes Mongoose to connect to a MongoDB database. Authorization and authentication functionality was implemented following secure practices.

#### Documentation
https://jobs-management-api.onrender.com/api-docs/

#### Setup

```bash
npm install && npm start
```

#### Routers

- auth.js
- jobs.js



#### Register User

- Validate - name, email, password - with Mongoose
- Hash Password (with bcryptjs)
- Save User
- Generate Token
- Send Response with Token

#### Login User

- Validate - email, password - in controller
- If email or password is missing, throw BadRequestError
- Find User
- Compare Passwords
- If no user or password does not match, throw UnauthenticatedError
- If correct, generate Token
- Send Response with Token

#### Mongoose Errors

- Validation Errors
- Duplicate (Email)
- Cast Error

#### Security

- helmet
- cors
- xss-clean
- express-rate-limit
