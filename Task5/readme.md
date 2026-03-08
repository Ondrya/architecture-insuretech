# Проект контракта

```graphql
type Query {
  """
  Возвращает информацию о клиенте.
  """
  client(id: String!): Client

  """
  Возвращает список документов клиента по ID.
  """
  clientDocuments(id: String!): [Document]

  """
  Возвращает информацию о родственниках клиента по ID.
  """
  clientRelatives(id: String!): [Relative]
}

"""
Информация о клиенте
"""
type Client {
  id: String
  name: String
  age: Int
}

"""
Документ
"""
type Document {
  id: String
  type: String
  number: String
  issueDate: String
  expiryDate: String
}

"""
Родственник
"""
type Relative {
  id: String
  relationType: String
  name: String
  age: Int
}
```
