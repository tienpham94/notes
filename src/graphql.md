# GraphQL on server

Fields inside resolver have the same name as in query can resolve itself

If you ask for id, will run the id resolver and `console.log` stuff

We have no control over when resolver get ran
```js
module.exports = {
  Query: {
    project,
    projects
  },
  Mutation: {
    newProject
  },
  Project: {
    id(project) {
      console.log('wut')
      return project._id + ''
    },
    // resolve some fields here
  }
}
```
