# import customers API
## Sample API call
```
curl https://customerapi-zo6fgz3fza-uc.a.run.app/customers/4 | jq '.'
```


```
stepzen import curl https://customerapi-zo6fgz3fza-uc.a.run.app/customers/4 --name customers --query-type Customer --query-name customer --path-params '/customers/$id'
```