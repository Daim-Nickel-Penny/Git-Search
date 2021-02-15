# Git-Search

This library returns the list of github repositories. <br>The list is sorted in the **descending** order and the **last updated time**

### For Installation

- **NPM** installation
  `npm install github-repos-search`
- **Yarn** Installation
  `yarn add github-repos-search`

### Usage

- using `import`
  `import { getRepos } from 'github-repos-search';`

- using `require`
  `const { getRepos } = require('github-repos-search');`

### Code Snippet

#### using promises

    `getRepos({
      username: 'YOUR_USERNAME', // replace this with the github username
      page: 1, // optional property: default value is 1 for 1 page
      per_page: 50 // optional property: default value is 30 for the list length of repositories
    }).then((repositories) => console.log(repositories));
    //check the console for output in JSON

#### using async/await

    const getRepositories = async function () {
      const repositories = await getRepos({
        username: 'YOUR_USERNAME', // replace this with the github username
        page: 1, // optional property: default value is 1 for 1 page
        per_page: 50 // optional property: default value is 30 for the list length of repositories
      });
      console.log(repositories);
       //check the console for output in JSON
    };

    getRepositories();
