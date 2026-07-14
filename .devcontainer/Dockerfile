FROM mcr.microsoft.com/devcontainers/python:3.13-bookworm

ENV UV_LINK_MODE=copy \
    UV_PROJECT_ENVIRONMENT=/workspaces/SSHLibrary/.venv \
    PATH="/workspaces/SSHLibrary/.venv/bin:${PATH}"

RUN apt-get update \
    && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y --no-install-recommends \
        build-essential \
        libffi-dev \
        libssl-dev \
        make \
        openssh-client \
        openssh-server \
    && rm -rf /var/lib/apt/lists/*

RUN python -m pip install --no-cache-dir --upgrade uv
