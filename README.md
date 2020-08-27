# E2Easy-Go
E2Easy-Go

Example .yaml:
````
name: contract_retention
steps:
  - name: create_contract
    path: https://contract.api.com.br
    method: POST
    body: "{ \"name\": \"tst\", \"age\": 27, \"type\": \"GOLANG\" }"
    vars:
      response: "response.body"
  - name: get_retention
    path: https://retention.api.com.br
    method: GET
    vars:
      retention: "response.body.id"
``