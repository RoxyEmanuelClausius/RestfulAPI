# Address API Spec

## Create Address

Endpoint : POST /api/contacts/{idContact}/addresses

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request Body :

```json
{
  "street" : "Jalan Rose Garden 3",
  "city" : "Bekasi Selatan",
  "province" : "Bekasi",
  "country" : "Indonesia",
  "postalCode" : "55187"
}
```

Response Body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "street" : "Jalan Rose Garden 3",
    "city" : "Bekasi Selatan",
    "province" : "Bekasi",
    "country" : "Indonesia",
    "postalCode" : "55187"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Contact is not found"
}
```

## Update Address

Endpoint : PUT /api/contacts/{idContact}/addresses/{idAddress}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request Body :

```json
{
  "street" : "Jalan Rose Garden 3",
  "city" : "Bekasi Selatan",
  "province" : "Bekasi",
  "country" : "Indonesia",
  "postalCode" : "55187"
}
```

Response Body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "street" : "Jalan Rose Garden 3",
    "city" : "Bekasi Selatan",
    "province" : "Bekasi",
    "country" : "Indonesia",
    "postalCode" : "55187"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Address is not found"
}
```

## Get Address

Endpoint : GET /api/contacts/{idContact}/addresses/{idAddress}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "street" : "Jalan Rose Garden 3",
    "city" : "Bekasi Selatan",
    "province" : "Bekasi",
    "country" : "Indonesia",
    "postalCode" : "55187"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Address is not found"
}
```

## Remove Address

Endpoint : DELETE /api/contacts/{idContact}/addresses/{idAddress}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data" : "OK"
}
```

Response Body (Failed) :

```json
{
  "errors" : "Address is not found"
}
```

## List Address

Endpoint : GET /api/contacts/{idContact}/addresses

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data": [
    {
      "id": "randomstring",
      "street" : "Jalan Rose Garden 3",
      "city" : "Bekasi Selatan",
      "province" : "Bekasi",
      "country" : "Indonesia",
      "postalCode" : "55187"
    }
  ]
}
```

Response Body (Failed) :

```json
{
  "errors" : "Contact is not found"
}
```