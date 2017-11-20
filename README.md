###Запросы получения данных
```graphql
{
    apple: company(id: "1") {
        ...companyDetails
    }
    google: company(id: "2") {
        ...companyDetails
    }
}

fragment companyDetails on Company {
    id
    name
    description
}
```

###Добвить нового пользователя
```graphql
mutation {
  addUser(firstName: "Vasy", age: 25){
    id
    firstName
    age
  }
}
```

###Удаление пользователя
```graphql
mutation {
  deleteUser(id: "1"){
    id
  }
}
```

###Редактирование пользователя
```graphql
mutation {
  editUser(id: "2", age: 10){
    id
    age
    firstName
  }
}
```
