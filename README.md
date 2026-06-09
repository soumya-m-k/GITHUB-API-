# GITHUB API DOCUMENTATION
THE github API allows developers to interact with github programatically. It enables access to users,repositories,issues and other github features.

## Uses of Github API
- Automation - github api helps tocreate repositories,manage issues and make pull request programatically.
- CI/CD - making ir cancling workflow using github actions REST API.

  ### Base URL
  https://api.github.com

  ### Authentication
  Github API requires API key to access private data and work with it. because it makes sure that only valid user can access the data and provides security to your personal data and protects from unauthorized person to breach the data.

  **How to get API Keys**
  - login to github Account
  - navigate to github account setting
  - go to developer setting
  - choose personal access token
  - click generate new token
  - copy the token and paste it

  **select the endpoint you wanted**
  
  choose the enpoint you want make request
  * get/user/{username} - get the user profile
  * get/user/{username}/repo - retrieve the repos of a user
  * post/user/repo - create the repository

    
