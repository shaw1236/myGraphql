# Test using curl 

- Query the messages - getMessageList

$curl -i -H 'Content-Type: application/json' -X POST -d '{"query": "query {getMessageList{id author content}}"}' http://localhost:4000/graphql


- Read a message - getMessage

$curl -i -H 'Content-Type: application/json' -X POST -d '{"query": "query {getMessage(id: 1) {id author content}}"}' http://localhost:4000/graphql


- Create a message - createMessage

$curl -i -H 'Content-Type: application/json' -X POST -d '{"query": "mutation {createMessage(author: \"curl\", content: \"test\") {id author content}}"}' http://localhost:4000/graphql


- Update/patch a message - updateMessage

$curl -i -H 'Content-Type: application/json' -X POST -d '{"query": "mutation {updateMessage(id: 9, content: \"curl test\")}"}' http://localhost:4000/graphql


- Delete a message - deleteMessage

$curl -i -H 'Content-Type: application/json' -X POST -d '{"query": "mutation {deleteMessage(id: 9)}"}' http://localhost:4000/graphql
