# User Api

**Project**: [rcs-user-api][project-url]

**Live**: [rcs-user-api-live][project-demo]

**Postman Collection**: [postman-collection-link][collection-link]

## Instruction

```sh
# clone this repo
git clone --branch https://github.com/arkarhtethan/rcs-user-api.git
# `cd` into project folder
cd rcs-user-api
# install dependencies
npm install
```

after running these commands create a .env file in project root directory (where index.js file is)
and add the following variables to your .env file shown in .env.example

now just run command `npm run start:dev`

## Routes

| token | route                      | http method | props                                         | description                                 |
| ----- | -------------------------- | ----------- | --------------------------------------------- | ------------------------------------------- |
|       | /user/register             | post        | name, email, password                         | register user with username,email,password  |
|       | /api/user/login            | post        | email, password                               | login and get access token                  |
|   *   | /api/user                  | get         |                                               | get user list for logged in user            |
|   *   | /api/user/:id              | get         |                                               | get user details for logged in user         |
|   *   | /api/user/profile          | get         |                                               | get my profile for logged in user           |
|   *   | /api/user/change-password  | patch       |                                               | get my profile for logged in user           |
|   *   | /api/user/                 | delete      |                                               | delete account for logged in user           |

**\*** requires access token in `x-jwt` header

[project-url]: https://github.com/arkarhtethan/rcs-user-api.git
[project-demo]: https://rcs-user-api.herokuapp.com/
[collection-link]: https://go.postman.co/workspace/RCS~cb9f9bb0-d398-45dd-8d63-2be7e53aca69/collection/7196426-f9ba51d4-7c24-4078-b352-d8c759b637ee
