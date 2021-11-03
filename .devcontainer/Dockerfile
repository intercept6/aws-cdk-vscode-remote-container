# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.202.5/containers/javascript-node/.devcontainer/base.Dockerfile

# [Choice] Node.js version (use -bullseye variants on local arm64/Apple Silicon): 16, 14, 12, 16-bullseye, 14-bullseye, 12-bullseye, 16-buster, 14-buster, 12-buster
ARG VARIANT="16-bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:0-${VARIANT}

USER node

# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

RUN npm install -g aws-cdk prettier gts

RUN install -o node -g node -d /home/node/.aws/ && \
    install -o node -g node -d /home/node/.ssh/
