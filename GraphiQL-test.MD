-- Test with GraphiQL

- Query
{
  getMessageList {
    id
    author
    content
  }
}

- Create
mutation {
  createMessage(author: "andy", content: "hope is a good thing") {
    id author content
  }
}

- Update/patch
mutation {
  updateMessage(id: 3, author: "andy", content: "andy's test")
}

- Read
{
  getMessage(id: 1) {
    id content author
  }
}

- Delete
mutation {
  deleteMessage(id: 2)
}
