# VSCode DevContainer

This is my standard workspace for VScode environments. Preferred over installing everything on local machine (allows separate dev environments between projects more easily)

## Modify the .devcontainer files

- devcontainer.json
  - Replace the containerEnv.USERNAME with your username (ideally from host machine)
- Dockerfile
  - Replace the USER arg with your username (must match devcontainer.json file)

## Use

Copy the `.devcontainer` directory to your new project, then open in vscode followed by the command "reopen in devcontainer" (usually `ctl+shift+p` with the word "reopen").

You will have to build the devcontainer the first time

Can also set a workspace configuration in the JSON file to point to a folder that may house all your projects/any bundled projects and use one devcontainer for all.


May also use the devcontainer.env file to set container env variables

## Tools included (so far)

- kubectl
- oc (openshift CLI)
- dos2unix
- docker (docker-in-docker) as rootless/non-sudo user
- helm
- kubeval
- minikube (configured to use docker, 4cpu, 8GB mem)
- sudo priviledges in container
