
1. Create a pipline in a yaml file. >> gke_deploy.yml, location >> .github/workflows
2. Add an event

```
on:
  push:
    branches:
      - main
```

3. Create all variables and secrets required.

    Repository on Github >> settings >> Secrets and Variables

    Add your variables and Secrets required

4. Create rest of the pipeline

- Create the Docker images for frontend and backend
- Push the images to the DockerHub or any other private registry

6. Create a service account on yor google cloud and add a key in json format

7. Add this key as a secret in your Github secrets

8. Create another job for Deploy code on Cluster

- Fetch the code
- Authenticate using auth action
- Get the authentication for Cluster
- Apply the kubectl commands to deploy the code!