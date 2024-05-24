# Federation Demo

This demo uses the "customers" (dev/customer) and "orders" (dev/order) APIs.

## Prep
Remove any existing imports.
```
make clean
```

## Build Federated API.

### Import Customers graph
```
stepzen import graphql https://YOUR_DEPLOYED_API_URL/dev/customers/__graphql \
--name customers \
--header "Authorization: apikey $(stepzen whoami --apikey)"
```

### Import Orders graph
```
stepzen import graphql https://YOUR_DEPLOYED_API_URL/dev/orders/__graphql \
--name orders \
--header "Authorization: apikey $(stepzen whoami --apikey)"
```

### Connect APIs
Add `extensions.graphql` to `index.graphql` `@sdl` entry.