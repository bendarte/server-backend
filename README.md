# Bendarte - Backend Server.

![project_structure](https://github-production-user-asset-6210df.s3.amazonaws.com/143492796/302132285-4aaa3f7c-ea67-4a1e-b774-282afa9a9c24.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240209%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240209T171245Z&X-Amz-Expires=300&X-Amz-Signature=eec3a4f4cb53fdf5d091bc183ef9953abfb418c47a65677d30f67b6a6ad26587&X-Amz-SignedHeaders=host&actor_id=143505763&key_id=0&repo_id=744033747)

## Run Complete Project:

### `Auth and Frontend Servers:`
- You can find the Auth Server here:
```Auth
https://github.com/bendarte/server-auth.git
```
- You can find the Frontend Server here:
```Frontend
https://github.com/bendarte/server-frontend.git
```

```NOTES
HOW TO RUN COMPLETE PROJECT:
You will have to add the same JWT_SECRET in .env file of the Auth Server.
So the Auth Server can assign JWT to user at login.
```

## TTFHW Backend Server - 5min

### `Backend Setup:`
- Git clone https://github.com/bendarte/server-backend.git
- Go to the root folder of the project and run "npm install" in the terminal to get all correct node_modules.
- Create .env file in root folder of project, add a cryptokey to JWT_SECRET & PORT to .env config file.

```.ENV
ADD FOLLOWING BELOW TO BACKEND'S .ENV FILE:
JWT_SECRET=SAME KEY AS AUTH SERVER
PORT=3002
```

### `How to start the Backend Server:`
- You can now run "npm start" in the root folder to start the Backend Server.

#### `Run Complete Project:`
- You will need to add both Auth and Frontend Servers to run the complete project.
- Run Frontend Server on PORT=3000
- Run Auth Server on PORT=3001
- Run Backend Server on PORT=3002
- .ENV file in both Auth & Backend Server, both containing the same JWT_SECRET.

## Functions - Backend Server
`1. Jsonwebtoken - authentication and authoriziation:`
- JWT is used to verify users and to determine user roles.
- Users token is stored in httpOnly cookie.
  
`2. Helmet - To protect from multiple attacks such as:`
- Cross-Site Scripting (XSS) 
- Clickjacking 
- Man-in-the-middle 
- Cross-site Request Forgery
- DNS Prefetch Control
- Content-Type Sniffin

`3. CORS - Resource Sharing:`
- Cors is used to control and restrict cross-origin requests.
- Cors allows applications on one domain to make request for resources from a different origin / domain.
- Cors also prevents CSRF and XSS attacks.

`4. DOTENV - Environment Variables:`
- dotenv is used to store and access sensitive information.
- dotenv is used to avoid storing configuration details inside of source code.
- JWT Secret is stored inside of .ENV file.

`5. Rate-Limit - Controls rate of incoming requests:`
- Helps to protect from brute-force attacks.
- Helps protect server resources.
- Helps to ensure fair usage of resources between users.
