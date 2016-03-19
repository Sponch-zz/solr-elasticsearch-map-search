# solr-elasticsearch-map-search
Mapping the differences between Sorl and Elasticsearch

| Feature       | Solr         | Elasticsearch  |
| ------------- |:-------------:| -----:|
| query all      | q=\*:\* |  {"query": { "match_all": {} }}|
| num results        | rows=10 | {"query":{"match_all":{}},"*size*":1}|
| paginations    | start=10  | {"query":{"match_all":{}},"*from*":10} |
||||
