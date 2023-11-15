## Building

For each container, the build steps are the same. The examples below
are for the `show` container. Replace `show` with `backend` for the
backend container.

## Google Container Registry ([GCR](https://cloud.google.com/tools/container-registry/))

    docker build -t gcr.io/<project-name>/show .
    gcloud docker push gcr.io/<project-name>/show

## Docker Hub

    docker build -t <username>/show .
    docker push <username>/show

## Change Pod Definitions

Edit both `show-rc.yaml` and `backend-rc.yaml` and replace the
specified `image:` with the one that you built.



