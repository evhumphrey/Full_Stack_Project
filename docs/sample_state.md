```js
{
  currentUser: {
    id: 1,
    username: "app-academy"
  },
  forms: {
    signUp: {errors: []},
    logIn: {errors: []},
    createReview: {errors: ["body can't be blank"]}
    createBook: {errors: ["body/title/author can't be blank"]}
  },
  Books: {
    1: {
      title: "Sample State",
      blurb: "is useful to plan",
      author_id: 1,
      tags: {
        1: {
          id: 1
          name: "Coding"
        }
      }
    }
  },
  reviews: {
    1: {
      title: "Redux",
      author_id: 1,
      book_id: 1,
      description: "is cool"
    }
  }
  tagFilters: [1, 7, 14] // maybe implement similar in bonus to narrow browsing books
}
```
