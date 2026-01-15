Little Lemon API endpoints to test:

- GET/POST: http://127.0.0.1:8000/api/menu-items/
- GET/PUT/PATCH/DELETE: http://127.0.0.1:8000/api/menu-items/<id>
- ViewSet (Booking) via router:
  - GET/POST: http://127.0.0.1:8000/api/booking/tables/
  - GET/PUT/PATCH/DELETE: http://127.0.0.1:8000/api/booking/tables/<id>/
- Auth:
  - Token obtain: http://127.0.0.1:8000/api-token-auth/
    - POST JSON: {"username": "<user>", "password": "<pass>"}
    - Response: {"token": "<token_value>"}
    - Use header on subsequent requests: Authorization: Token <token_value>
  - Djoser auth: http://127.0.0.1:8000/auth/token/login/ and http://127.0.0.1:8000/auth/token/logout/
    - Login: POST JSON {"username": "<user>", "password": "<pass>"}; returns auth token
    - Logout: POST with Authorization: Token <token_value> to revoke
  - Djoser users: http://127.0.0.1:8000/auth/users/
    - Register: POST JSON {"username": "<user>", "password": "<pass>"}
    - List users: GET with proper auth (staff/superuser typically required)
    - Retrieve detail: GET http://127.0.0.1:8000/auth/users/<id>/ with auth
