# autoradio-steering-api-dummy
This is a dummy API catering to dev modules of the autoradio project by [Radio FRO](https://www.fro.at/), [Freies Radio Freistadt](https://www.frf.at/), [Radio Helsinki](https://helsinki.at) and [Radio Orange](https://o94.at/). It uses the [JSON Server](https://github.com/typicode/json-server) to provide an API based on the `db-extended.json` file in this repository.

Setup
=====
All you need is the [JSON Server](https://github.com/typicode/json-server), which should be easily set up with:

```
$ npm install -g json-server

```

Then grab this repo use the following command to start the JSON Server in read-only mode:

```
$ json-server --ro --watch --routes routes.json db-extended.json

```

If you also want to be able to write to the database through the API, then leave out the `--ro` option.

Notes on the db.json file
=========================
The `db.json` file is a reduced test data sample one could use with [my-json-server by typicode](https://my-json-server.typicode.com/). But this does not actually work out nicely. There is a limitation of <10k for the whole databases. Beyond that also only 5 fields are permitted per entry, which is not very useful for our test cases.

So in future commits we'll get rid of this file and move our `db-extended.json` into its place.
