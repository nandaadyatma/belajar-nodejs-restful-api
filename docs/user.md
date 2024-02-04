# User API Spec

## Register User API

Endpoint POST /api/users

Request Body :

```json
{
    "username" : "iniusername",
    "password" : "inipassword",
    "name" : "Ini nama"
}
```

Response Body Success :
```json
{
    "data" : {
        "username" : "iniusername",
        "name" : "Ini nama"
    }
}
```

Response Body Error :
```json
{
    "errors" : "Username already registered"
}
```

## Login User API

Endpoint : POST /api/users/login

Request Body :
```json
{
    "username" : "iniusername",
    "password" : "inipassword"
}
```

Response Body Success :
```json
{
    "data" : {
        "token" : "unique-token"
    }
}
```

Response Body Error :
```json
{
    "errors" : "Username or password is not valid"
}
```

## Update User API

Endpoint : PATCH /api/users/current

Headers :
- Authorization : token

Request Body : 
```json
{
    {
        "name" : "new name", //optional
        "password" : "new password" //optional
    }
}
```

Response Body Success :
```json
{
    "data" : {
        "username" : "username",
        "name" : "new name"
    }
}
```

Response Body Error :
```json
{
    "errros" : "Name length max 100"
}
```

## Get User API

Endpoint : GET /api/users/current

Headers :
- Authorization : token

Response Body Success :
```json
{
    "data" : {
        "username" : "username",
        "name" : "name"
    }
}
```

Response Body Error :
```json
{
    "errors" : "Unauthorized"
}
```

## Logout User API

Endpoint : DELETE /api/users/logout

Headers :
- Authorization : token

Response Body Success :
```json
{
    "data" : "OK"
}
```

Response Body Error :
```json
{
    "errors" : "Unathorized"
}
```