# Pipeline--Commit-Build-ECR-DockerHub
CodePipeline to create a Commit + Build project to publish docker images to ECR/DockerHub
This code publishes a docker image to the ECR/ DockerHub. The image is built using ``docker build`` and pushed into the repository.

# CodeCommit
Source Code Repository that uses familiar git commands for version control of the code. Commit is added to Pipeline (which is an Orchestration tool), triggers the Pipeline flow whenever a new change is pushed to the branch

# CodeBuild
Provides a managed Build and test Environment. The Environment for build is Amazon Linux docker image and source code is from Codecommit. AWS_ACCOUNT, REGION and other Image details are furnished as Environment Variables in Build process. The build image is published in Docker Hub/ Elastic Container Registry.
