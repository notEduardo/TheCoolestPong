## Build Docker Image
docker build -t thecoolestpong .

(TO RUN LOCALLY) docker run -p 8080:80 thecoolestpong

## Get GCP Auth
gcloud auth configure-docker {region}-docker.pkg.dev

## Push to GCP
docker tag thecoolestpong {region}-docker.pkg.dev/{project-name}/{repo-name}/thecoolestpong:v1
docker push {region}-docker.pkg.dev/{project-name}/{repo-name}/thecoolestpong:v1

