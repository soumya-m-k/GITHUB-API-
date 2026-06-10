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

  **Request headers**
  Every api request needs standard header
  - supply the accept header fot media version
  - authorization should carry your token

   ## how to make request
  
  + ### get authenticated user profile
    
    **Endpoint**
    
     <mark> get/user</mark>

     **description**

      Returns the information of authenticated user

    **Example request**

      GET https://api.github.com/user

    **Example response**

      {<br>
      "login": "username",<br>
      "id": 123456,<br>
      "name": "John Doe"<br>
      }

    - get public user

      **Endpoint**

       <mark> get/users/{username} </mark>

       **Example**

        get https://api.github.com/users/soumya-m-k
      

   - ### Repository API

      **List of user repository**

        **Endpoint**

         get https://api.github.com/user/repos

        **description**

        return all repositories of authenticated user
      

  - ### Create a repository

         **Endpoint**

       <mark>  POST/user/repos</mark>

         **request body**

        {<br>
           "name":"my new repo",<br>
           "description":"the new repo",<br>
           "private":false,<br>
         }

         **Response Example**

          "id": 1264740174,
      
          "node_id": "R_kgDOS2JnTg",
      
          "name": "my-repo7",
      
          "full_name": "soumya-m-k/my-repo7",
    

      **Error Handling**

       **status code**         **Meaning**

         401                    unauthorized

         400                   	Bad Request
      
         403                    Forbidden
    
         404	                  Not Found
    
         500	                  Server Error

         422                    Unprocessable content


    **EXAMPLE WORKFLOW**

     The real example of how to use github api to explore authenticated user profile, list of repositories of user and creating a new repo.

    + **Get authenticated user profile**

       you need api keys from that authenticated user.

       **Request example**

        get  https://api.github.com/user
 
          or if you want public user
 
        get  https://api.github.com/users/soumya-m-k

       **Response example**

        {

           "login":"soumya-m-k",
    
           "id":102578405,

           "name":"soumya kanabargi"

        }

  +  **list of repository**

     get all the repositories of authenticated user with all information.

     **Request example**

        get  https://api.github.com/user/repos
 
       **Response example**

        {

           "id":102578405,

           "name":"github api"

           "fullname"soumya-m-k/github api"

        }

  +  **create a repository**
 
      create a repository you wanted

     **Request example**

        get  https://api.github.com/user/repos
 
       **request body**
 
         {
     
            "name":"my repo",
     
            "description":"the new repo",
     
            "private":false

         }

       **Response example**

         {

           "id":102578405,

           "name":"my repo"

           "fullname"soumya-m-k/my repo"

         }

       **Conclusion**

        github api allows developers to manage repositories, users and issues efficiently through REST API endpoints.
