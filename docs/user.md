# User API Spec

## Register User

- Endpoint : POST /api/users

Request Body:

```json
{
  "username": "roxy.emanuel",
  "password": "Roxy2603",
  "name": "Roxy Emanuel Clausius"
}
```

Response Body (Success):

```json
{
  "data": "OK"
}
```

Response Body (Failed) :

```json
{
  "error": "Username must not blank, ???"
}
```

## Login User

- Endpoint : POST /api/auth/login

Request Body:

```json
{
  "username": "roxy.emanuel",
  "password": "Roxy2603"
}
```

Response Body (Success):

```json
{
  "data": {
    "token": "TOKEN",
    "expiredAT" 60000 //milisecon
  }
}
```

Response Body (Failed,401) :

```json
{
  "error": "Username or Password Wrong"
}
```

## Get User

- Endpoint : GET /api/users/current

Request Header:

- X-API-TOKEN : Token (Mandatory)

Response Body (Success):

```json
{
  "data": {
    "username": "roxy.emanuel",
    "name": "Roxy Emanuel Clausius"
  }
}
```

Response Body (Failed,401) :

```json
{
  "error": "Unauthorized"
}
```

## Update User
- Endpoint : PATCH /api/users/current

Request Header:

- X-API-TOKEN : Token (Mandatory)

Request Body: 

```json
{
  "name": "Roxy Emanuel Clausius",
  "password": "New Password"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "roxy.emanuel",
    "name": "Roxy Emanuel Clausius"
  }
}
```

Response Body (Failed,401) :

```json
{
  "error": "Unauthorized"
}
```

## Logout User

-Endpoint : DELETE /api/auth/logout


Request Header:

- X-API-TOKEN : Token (Mandatory)

Response Body (Success):

```json
{
  "data": "ok"
}
```