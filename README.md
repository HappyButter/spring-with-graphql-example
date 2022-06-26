# Getting Started with GraphQL and Spring Boot

---

### Steps to start the application

* `mvn package` - produces artifact and build a docker image

* `docker-compose up` - starts mongodb, and the api service

---
Go to: `http://localhost:8080/graphiql`

And try:
```
query {
    getArticles {
        title
        id
        text
        comments {
            text
        }
    }
}
```

OR

```
mutation {
    addArticle(title: "A New Article", text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.") {
        id
        title
        comments {
            text
        }
    }
}
```

OR

```
mutation {
  addComment(articleId: "6266e99e165951703e083aa4", text: "New Comment") {
    title
    comments {
      text
    }
  }
}
```

--- 

### Based on 

[Baeldung Courses](https://www.baeldung.com/spring-graphql)

[Spring Boot GraphQL Tutorial](https://medium.com/geekculture/spring-boot-graphql-tutorial-77300048909b)