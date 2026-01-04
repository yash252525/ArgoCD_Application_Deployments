# Install Image Updater

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj-labs/argocd-image-updater/v0.12.2/manifests/install.yaml

# Create Github PAT and Docker Hub PAT
# Push v1.0.0 image to Docker hub
# create Secret for Github
# Change Image name in deploy.yml
# Create secret for Github
# Annotate to the following application (repository in Docker Hub so whenever the latest image is pulled it automatically updates the image to GitHub)

