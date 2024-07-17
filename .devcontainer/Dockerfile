#-------------------------------------------------------------------------------------------------------------
# Copyright (c) Microsoft Corporation. All rights reserved.
# Licensed under the MIT License. See https://go.microsoft.com/fwlink/?linkid=2090316 for license information.
#-------------------------------------------------------------------------------------------------------------

# Update the VARIANT arg in devcontainer.json to pick an Alpine version: 3.10, 3.11, 3.12
# To fully customize the contents of this image, use the following Dockerfile instead:
# https://github.com/microsoft/vscode-dev-containers/tree/v0.128.0/containers/alpine/.devcontainer/base.Dockerfile
ARG VARIANT="3.12"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-alpine-${VARIANT}

RUN apk update \
    && apk add --no-cache --no-progress \
                    ansible=2.9.9-r0 \
                    ansible-lint=4.2.0-r0 \
                    bash=5.0.17-r0 \
                    coreutils=8.32-r0 \
                    git=2.26.2-r0 \
                    openssh-client=8.3_p1-r0 \
                    python3=3.8.5-r0 \
    && ln -s /usr/bin/python3 /usr/bin/python