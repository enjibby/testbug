# Regression in Visual Studio Code

## Expected Behaviour

Ensure that Visual Studio Code and the Remote Development extension is installed, clone this projects into a folder on WSL2, and open the folder in VSCode.

* Using the integrated terminal, project starts correctly when using the command `docker-compose -f .devcontainer/docker-compose.yml --env-file .env up`.
* Using the integrated terminal, project starts correctly when using the command `docker-compose up` (as the project root .env contains `COMPOSE_FILE=.devcontainer/docker-compose.yml`)
* Using VSCode's `Shift+Ctrl+P` command palette, project starts when selecting "Remote-Containers: Re-open in Container".

## Actual Behaviour

Containers start correctly when invoked from the command line, but an error occurs when starting using Remote Development. Error can be avoided if an additional .env file is created in the .devcontainer subfolder with the correct variables defined.