# CamelK-customerAPI

### How to Run

```sh
git clone https://github.com/abouchama/CamelK-customerAPI.git
cd CamelK-customerAPI
kamel run --name customers --dependency camel-undertow --property camel.rest.port=8080 --logs --open-api customer-api.json customer-api.xml
```

![Camel K Routes started](images/CamelK_Routes_Started.png "Camel-k Routes started")

### Print rest routes:

You have to enable DEBUG logging level:

```sh
kamel run --name customers --dependency camel-undertow --property camel.rest.port=8080 --logs --open-api customer-api.json --logging-level org.apache.camel.k=DEBUG customer-api.xml
```

![Camel K Rests Routes](images/CamelK-Rests.png "Camel-k Rests Routes")
