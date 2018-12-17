# fuzzy

creating DjangoRest API with Elasticsearch

### Getting set-up

run :
```bash
$ git clone https://github.com/4bic/fuzzy.git

$ cd fuzzy

$ make web  #could take a lottle while ⏳
```
Run `ctrl + c` to stop the server  or open another console and run:
```bash
$ make migration
```

Open browser and go to http://0.0.0.0:8000/products/

This should respond with :

``` json
HTTP 200 OK
Allow: GET, POST, HEAD, OPTIONS
Content-Type: application/json
Vary: Accept

[]
```

Load up the database with products data.

```bash
TODO

# $ psql fuzzy -U fuzzy -c "\COPY catalog_product(type,category,code,VEN,HFR,description,uom,price) FROM 'data/catalog_data.csv' DELIMITER ',' CSV HEADER"

```
To search for a products with description eg _dental_ :

go to http://0.0.0.0:8000/products_search/?q=dental

When you’re done, don’t forget to close down your Docker container.

```bash
$ docker-compose down

```