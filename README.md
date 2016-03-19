# solr-elasticsearch-map-search
Mapping the differences between Sorl and Elasticsearch

| Feature       | Solr         | Elasticsearch  |
| ------------- |:-------------:| -----:|
| query all      | **q**=\*:\* |  {**"query": { "match_all": {} }**}|
| num results        | q=\*:\*&**rows**=10 | {"query":{"match_all":{}},"**size**":1}|
| paginations    | q=\*:\*&**start**=10  | {"query":{"match_all":{}},"**from**":10} |
|field list|q=\*:\*&**fl**=account_number,balance| {"query":{"match_all":{}},"**_source**":["account_number","balance"]}|
|basic fielded search query|**q=account_number:20** | {"query":{**"match":{"account_number":20}**}}|
