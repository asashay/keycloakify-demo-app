<p align="center">
    <img src="https://user-images.githubusercontent.com/6702424/110417203-6bae4e80-8095-11eb-8211-2592a5758668.png">  
</p>
<p align="center">
    <i></i>
    <br>
    <br>
    <img src="https://github.com/garronej/keycloakify-demo-app/workflows/ci/badge.svg?branch=main">
</p>

This repo constitutes an easily reusable CI setup for React App in general and Apps that generates Keycloaks's theme 
using [`keycloakify`](https://github.com/InseeFrLab/keycloakify) in particular.


- To release **don't create a tag manually**, the CI do it for you. Just update the `package.json`'s version field and push.
- The `.jar` files that bundle the Keycloak theme will be attached as an asset with every GitHub release. [Example](https://github.com/InseeFrLab/keycloakify-demo-app/releases/tag/v0.1.0)).
- The CI publishes the app docker image on DockerHub. `<org>/<repo>:main` for each commits on `main`  
  and `<org>/<repo>:latest` and `<org>/<repo>:X.Y.Z` when releasing a new version. [See on DockerHub](https://hub.docker.com/r/garronej/keycloakify-demo-app/tags?page=1&ordering=last_updated)
- A [CHANGELOG.md](https://github.com/InseeFrLab/keycloakify-demo-app/blob/main/CHANGELOG.md) will be maintained for you using the commit messages between releases. *If you don't want a specific commit to appear
  in the changelog do something like. `git commit -am "yadi yada (changelog ignore)`.*
  
![image](https://user-images.githubusercontent.com/6702424/110415780-ceeab180-8092-11eb-98a5-68ded9bfeeb7.png)

# DockerHub credentials

To enables the CI to publish on DockerHub on your behalf go to 
repository ``Settings`` tab, then ``Secrets`` you will need to add two new secrets:
- ``DOCKERHUB_TOKEN``, you Dockerhub authorization token.
- ``DOCKERHUB_USERNAME``, Your Dockerhub username.
