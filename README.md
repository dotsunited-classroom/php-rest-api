PHP REST API
============

Create a REST API which returns a list of movies as JSON formatted according
to the [HAL](https://tools.ietf.org/html/draft-kelly-json-hal) specification.

Requirements
------------

  * The REST API should be accessible as a Web API via HTTP on your local
    computer.
  * The application must be implemented in _pure_ PHP, no external software or
    libraries are allowed.
  * The movie list must be read from the provided JSON file `data/movies.json`.
  * The data file `data/movies.json` must not be accessible via HTTP.

Specification
-------------

  * The application must return correct HTTP response headers.
  * The application must return correct HTTP response bodies formatted
    according to the [HAL](https://tools.ietf.org/html/draft-kelly-json-hal)
    specification.
  * The application must return correct HTTP error responses for invalid URIs.
    Error responses should be formatted according to the
    [vnd.error](https://github.com/blongden/vnd.error) specification.
  * The application must return the full movie list from the root URL `/`.
  * The movie list must be filterable by movie title via a query string
    parameter, eg. `/?title=Titanic`.
  * The number of movies returned for a request must be controlled via a query
    string parameter, eg. `/?per_page=10`. The response must then indicate
    how to request the rest of the list.
