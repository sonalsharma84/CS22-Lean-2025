FROM mcr.microsoft.com/devcontainers/base:jammy

USER vscode
WORKDIR /home/vscode

RUN curl https://raw.githubusercontent.com/leanprover/elan/master/elan-init.sh -sSf | sh -s -- -y --default-toolchain none
RUN wget https://bootstrap.pypa.io/get-pip.py && python3 get-pip.py && python3 -m pip install requests && rm get-pip.py

ENV PATH="/home/vscode/.elan/bin:/workspaces/CS22-Lean-2025/scripts:${PATH}"
