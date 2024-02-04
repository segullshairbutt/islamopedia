# Technology specifications and workflow

## 1. Technology stack 
We are using Django for full-stack development to launch the application as fast as possible. We want to have a sustainable and mature framework with well-grounded community to avoid the deprecations in future. As Js eco-system is fast moving, we can't rely on their frameworks/libraries. 

### Code format and patterns
Details to be added after setting the initial environment ready.

## 2. Devops
### CI/CD
We are using GitHub runners for CI/CD. We are doing security checks, lint check, formatting checks by using `ruff` & `mypy`. We will also trigger `pytest` and `cypress` jobs in order to make sure that new changes did not introduced any bug to previous features so far.

### Deployment
We are going to use Google cloud platform for the deployment and data storage. Following resources might be helpful to achieve it:
https://stackoverflow.com/questions/62623119/how-to-host-deploy-my-django-project-to-firebase

We will use **firebase realtime-database** for storing the content of the books. Meanwhile, we will also have [another GitHub repository](https://github.com/segullshairbutt/islamopedia-books) to store all of the data in `.md` format. 

**NOTE:** The reason to keep the uploaded content in `.md` is to make it easy for reviewing the uploaded content. A user can preview it easily using Github PRs. 

## 3. Testing
We will do heavy testing on frontend, backend and e2e-testing to make the platform reliable and less error-prone. Following are the tools which we are going to use to achieve it.
    1. pytest, mocker, factoryboy, faker (for backend testing)
    2. Cypress (for end-to-end testing)
