# follow

### SET-UP

1) #### Aufruf in der Konsole:

docker run --publish=7474:7474 --publish=7687:7687 -e 'NEO4J_AUTH=neo4j/secret' neo4j:4.2.4

2) #### Docker Desktop öffnen und neo4j Datenbank im Browser öffnen

3) #### Passwort auf "secret" ändern

---

### REST

`POST localhost:8080/api/person/`


##### 1. POST /person

`POST localhost:8080/api/person/`

**Request-Body:**
````json
{
  "name":"BeiRegistrierung",
  "persons" :[
    {

    }
  ]
}
````

**Response-Body:**
```
{
    "entityId": X,
    "name": "BeiRegistrierung",
    "persons": [
        {
            "entityId": X,
            "name": null,
            "persons": null
        }
    ]
}
```

---

##### 2. PATCH /person/{id}

`PATCH localhost:8080/api/person/{id}`

**Request-Body:**
````json
{
  "name":"BeiRegistrierung",
  "persons" :[
    {
      "name":"Neuer Freund"
    }
  ]
}
````

**Response-Body:**
```
{
    "entityId": X,
    "name": "BeiRegistrierung",
    "persons": [
        {
            "entityId": X,
            "name": "Neuer Freund",
            "persons": null
        }
    ]
}
```

---

##### 3. GET /person/{id}

`GET localhost:8080/api/person/{id}`



**Response-Body:**
```
{
    "entityId": X,
    "name": "BeiRegistrierung",
    "persons": [
        {
            "entityId": X,
            "name": "Neuer Freund",
            "persons": null
        }
    ]
}
```
