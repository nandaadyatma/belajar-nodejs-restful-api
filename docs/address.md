# Address API Spec

## Create Address API

Endpoint : POST /api/contacts/:contactId/addresses

Headers :
- Authorization : token

Request Body : 

```json
    {
        "street" : "Address street",
        "city" : "City name",
        "province" : "Province name",
        "country" : "Country name",
        "postal_code" : "IUHSW782"
    }

```

Response Body Success :

```json
{
    "data" : {
        "id" : 1,
        "street" : "Address street",
        "city" : "City name",
        "province" : "Province name",
        "country" : "Country name",
        "postal_code" : "IUHSW782"
    }
}

```

Response Body Error :

```json
{
    "errors" : "Country is required"
}
```


## Update Address API

Endpoint : PUT /api/contacts/:contanctId/addresses/:addressId

Headers :
- Authorization : token

Request Body
```json
{
        "street" : "Address street",
        "city" : "City name",
        "province" : "Province name",
        "country" : "Country name",
        "postal_code" : "IUHSW782"
    }
```

Response Body Success :
```json
{
    "data" : {
        "id" : 1,
        "street" : "Address street",
        "city" : "City name",
        "province" : "Province name",
        "country" : "Country name",
        "postal_code" : "IUHSW782"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Country is required"
}
```

## Get Address API

Endpoint : GET /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Response Body Success :

```json
{
    "data" : {
        "id" : 1,
        "street" : "Address street",
        "city" : "City name",
        "province" : "Province name",
        "country" : "Country name",
        "postal_code" : "IUHSW782"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Contact is not found"
}
```

## List Addresses API

Endpoint : GET /api/contacts/:contactId/addresses

Headers :
- Authorization : token

Response Body Success :

```json
{
    "data" : [
        {
            "id" : 1,
            "street" : "Address street",
            "city" : "City name",
            "province" : "Province name",
            "country" : "Country name",
            "postal_code" : "IUHSW782"
        },
        {
            "id" : 2,
            "street" : "Address street",
            "city" : "City name",
            "province" : "Province name",
            "country" : "Country name",
            "postal_code" : "IUHSW782"
        },
        {
            "id" : 3,
            "street" : "Address street",
            "city" : "City name",
            "province" : "Province name",
            "country" : "Country name",
            "postal_code" : "IUHSW782"
        },
    ]
}
```

Response Body Error :

```json
{
    "errors" : "Contact is not found"
}
```

## Remove Address API

Endpoint : DELETE /api/contacts/:contactId/addresses/:addressId

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
    "errors" : "Address is not found"
}
```
