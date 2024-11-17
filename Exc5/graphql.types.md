```
type Client {
  id: String
  name: String
  age: Int
  documents: [Document]
  relatives: [Relative]
}
```

```
type Document {
  id: String
  type: String
  number: String
  issueDate: String
  expiryDate: String
  client: Client
}
```

```
type Relative {
  id: String
  relationType: String
  name: String
  age: Int

}
```
