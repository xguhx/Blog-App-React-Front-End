

# NodeJs Express Blog Rest API Front End
---

 The purpose of this app is to make Fetch calls to the REST API and display the Data.

 It uses GraphQL in the Fetch, it looks like this:

```js
const graphqlQuery = {
      query: `
      mutation SignUp ($email: String!, $name: String!, $password: String!) {
        createUser(userInput: {email: $email, name: $name , password: $password}) {
          _id
          email
        }
      }
      `,
      variables: {
        email: authData.signupForm.email.value,
        name: authData.signupForm.name.value,
        password: authData.signupForm.password.value,
      },
    };
    fetch(`${process.env.REACT_APP_API}/graphql`, {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify(graphqlQuery),
    })

```



---

## How this app works?

> User can create an account.

> User can create a post and upload an image.

> User can see everyone posts but can only edit or delete his own.

> User can add and edit the status.

---

#### Feel free to send me a message if you have an idea on how to improve this App. Also feel free to contribute!
#### Thank you fo reading!
