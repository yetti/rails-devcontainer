# Ruby on Rails devcontainer based development

Based on [robzolkos/rails-devcontainer](https://github.com/robzolkos/rails-devcontainer)

This devcontainer contains:
- Ruby 3.3.0
- Postgres latest
- Redis latest

You can update the Dockerfile and docker-compose.yml to add any other dependencies you may need.

Make sure you have the [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) extension pack installed in VS Code.

### Usage

1. Clone this repo
2. `cd` into it
3. Start vscode and it will prompt you to start the project in a dev container - yes!
4. Rename the app in `devcontainer.json`
5. `rails new . -d postgresql -c tailwind -j esbuild` (or whatever)
6. `bin/dev` to start normal rails dev servers

#### Database config sample

- see the `database.yml.example` on how to set the `host` for the database. As the database is in docker you need to give the docker host name `db` or the ENV VAR `DB_HOST`
