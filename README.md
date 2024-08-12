# VE3-project
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

With GraphQL, clients can specify exactly what data they need, and the server responds with only that data, reducing the amount of data transferred over the network.

Rest API Endpoint for get all users: http://localhost:5000/rest/getAllUsers

GraphQL Endpont: http://localhost:5000/graphql

Query for below scenarios:

1) Get All Users with query operation
    query{ getAllUsers{ id email } }

2)  Get single user details
    query{ findUserById(id:1000){ id firstName lastName email } }

3) Create User with mutation operation
    mutation{ createUser(firstName:"bhupendra",lastName:"patil",email:"bhupenpatil277@gmail.com",password:"password"){ id firstName lastName email } }


   >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
 
    # CI/CD Pipeline with GitHub Actions for AWS ECS

   ## Overview

This repository demonstrates a CI/CD pipeline that automates the deployment of a Node.js web application to AWS ECS using GitHub Actions. The pipeline includes the following steps:

1. **Checkout:** Retrieves the latest code from the GitHub repository.
2. **Build:** Builds a Docker image using a multi-stage build with Nginx as a reverse proxy.
3. **Push:** Pushes the Docker image to Amazon ECR.
4. **Deploy:** Deploys the Docker image to AWS ECS.
5. **Test:** Runs integration tests to verify the deployment.
6. **Rollback:** Automatically rolls back the deployment in case of a failure during testing.

## Setup

### Prerequisites

- AWS account with access to ECS and ECR.
- GitHub repository with the application code.
- Docker installed on your local machine.

### GitHub Secrets

Add the following secrets to your GitHub repository:

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_REGION`
- `ECR_REPOSITORY`
- `ECS_CLUSTER`
- `ECS_SERVICE`
- `ECS_TASK_DEFINITION`

### Running the Pipeline

1. Push your code to the `main` branch.
2. Monitor the workflow in the "Actions" tab.

### Rollback Mechanism

If the integration tests fail, the pipeline automatically rolls back the deployment to the previous stable version.

## Testing

- The integration tests can be customized in the `project-ve3.yml` file.
- Ensure that the tests are reliable to prevent unnecessary rollbacks.

## Documentation

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [AWS ECS Documentation](https://docs.aws.amazon.com/ecs)

  >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
