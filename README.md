# solr-elasticsearch-map-search
Mapping the differences between Sorl and Elasticsearch

| Feature       | Solr         | Elasticsearch  |
| ------------- |:-------------:| -----:|
| query all      | q=\*:\* |  {"query": { "match_all": {} }}|
| rows        | rows = 10 | {"query":{"match_all":{}},"size":1}|
