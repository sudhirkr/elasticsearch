# elasticsearch

elastic stack will be installed by docker-compose file.
command to run - #docker-compose up -d

##### Access elasticsearch
http://35.240.177.145:9200

#### Access Kibana
http://35.240.177.145:5601

#### Create mapping inside elasticsearch
curl -H "Content-Type: application/json" -XPUT '35.240.177.145:9200/shakespeare?pretty' -d @shakes-mapping.json

#### Populate index
curl  -H "Content-Type: application/json" -XPOST '35.240.177.145:9200/shakespeare/_bulk' --data-binary @shakespeare_7.0.json

#### Check the data through dejavu

Install dejavu

docker run -p 1358:1358 -d appbaseio/dejavu
open http://35.240.177.145:1358

Refer to https://github.com/appbaseio/dejavu

#### Check the data inside elasticsearch in tabular format through dejavu
Connect to - http://root:ssl123435@35.240.177.145:9200
index - shakespeare
