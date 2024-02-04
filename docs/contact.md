# Contact API Spec

## Create Contact API

Endpoint : POST /api/contacs

Headers :
- Authorization : token

Request Body : 

```json 
{
    "first_name" : "Nanda",
    "last_name" : "Adyatma",
    "email" : "nandaadyatma@gmail.com",
    "phone" : "08982893221"
}

```

Response Body Success :

```json
{
    "data" : {
        "id" : 1,
        "first_name" : "Nanda",
        "last_name" : "Adyatma",
        "email" : "nandaadyatma@gmail.com",
        "phone" : "08982893221"

    }   
}
```
Response Body Error :
```json
{
    "errors" : "Email is not valid format"
}
```

## Update Contact API

Endpoint : PUT /api/contacs/:id

Headers :
- Authorization : token

Request Body :
```json
   {
        "first_name" : "Nanda",
        "last_name" : "Adyatma",
        "email" : "nandaadyatma@gmail.com",
        "phone" : "08982893221"
    } 
```

Response Body Success :
```json
{
"data" : {
        "id" : 1,
        "first_name" : "Nanda",
        "last_name" : "Adyatma",
        "email" : "nandaadyatma@gmail.com",
        "phone" : "08982893221"

    } 
}
```

Response Body Error :
```json
{
    "errors" : "Email is not valid"
}
```

## Get Contact API

Endpoint : GET /api/contacs/:id

Headers :
- Authorization : token

Response Body Success :
```json
{
    "data" : {
        "id" : 1,
        "first_name" : "Nanda",
        "last_name" : "Adyatma",
        "email" : "nandaadyatma@gmail.com",
        "phone" : "08982893221"

    } 
}
```

Response Body Error :

```json
{
    "errors" : "Contact is not found"
}
```

## Search Contact API

Endpoint : GET /api/contacs

Headers :
- Authorization : token

Query params :
- name : Search by first_name or last_name, using like, optional
- email : Search by email using like, optional
- phone : Search by phone using like, optional
- page : number of page, default 1
- size : size per page, default 10

Response Body Success :
```json
{
    "data" : [
        {   "id" : 1,
            "first_name" : "Nanda",
            "last_name" : "Adyatma",
            "email" : "nandaadyatma@gmail.com",
            "phone" : "08982893221"

        },
        {   "id" : 2,
            "first_name" : "Nanda",
            "last_name" : "Adyatma",
            "email" : "nandaadyatma@gmail.com",
            "phone" : "08982893221"

        },
        {   "id" : 3,
            "first_name" : "Nanda",
            "last_name" : "Adyatma",
            "email" : "nandaadyatma@gmail.com",
            "phone" : "08982893221"

        },
    ],
    "paging" : {
        "page" : 1,
        "total_page" : 3,
        "total_item" : 30
    }
}
```

Response Body Error :

# Remove Contact API

Endpoint : DELETE /api/contacs

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
    "errors" : "Contact is not found"
}
```