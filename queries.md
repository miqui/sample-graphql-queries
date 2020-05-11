## URLS
 - [apollo-example](https://github.com/katopz/react-apollo-graphql-github-example)

## github
```
{
  search(query: "language:JavaScript stars:>10000", type: REPOSITORY, first: 10) {
    repositoryCount
    edges {
      node {
        ... on Repository {
          name
          descriptionHTML
          stargazers {
            totalCount
          }
          forks {
            totalCount
          }
          updatedAt
        }
      }
    }
  }
}
```

```
uery($number_of_repos:Int!){
  viewer {
    name
     repositories(last: $number_of_repos) {
       nodes {
         name
       }
     }
   }
}
```
```
{
  viewer {
    login
    starredRepositories {
      totalCount
    }
    repositories(first: 3) {
      edges {
        node {
          name
          stargazers {
            totalCount
          }
          forks {
            totalCount
          }
          watchers {
            totalCount
          }
          issues(states:[OPEN]) {
            totalCount
          }
        }
      }
    }
  }
}
```
