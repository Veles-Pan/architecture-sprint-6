```
type Query {
  client(id: String!): Client
  clients(ids: [String!]!): [Client]
  documents(clientId: String!): [Document]
  relatives(clientId: String!): [Relative]
}
```

Получить основные данные клиента

```
query {
  client(id: {userId}) {
    id
    name
  }
}
```

Получить данные клиента и его документы и родственников

```
query {
  client(id: {userId}) {
    id
    name
    documents {
      id
      type
    }
    relatives {
      id
      name
      relationType
    }
  }
}
```

Получить данные по нескольким клиентам и их документам

```

query {
  clients(ids: [{userId1}, {userId2}]) {
    id
    name
    documents {
      id
      type
    }
  }
}

```

Получить только документы клиента

```
query {
  documents(clientId: {userId}) {
    id
    type
    number
  }
}

```
