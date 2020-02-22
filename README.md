<a href="foundry.gg"><img src="https://foundry.gg/wp-content/uploads/2019/07/logo150.png" title="Foundry" alt="Foundry"></a>

# Command Foundry
This project serves as the backend for [Command Foundry](foundry.gg).

If you are interested in learning more or contributing then reach out to us on the [Deck Forge Discord Server](https://discord.gg/fxv6e2d).


## Overview
Card data is sourced from [MTGJSON](mtgjson.com) while supplementary information (e.g. acceleration, stax, tutors) are sourced by the community.

### Project Structure
    .
    ├── db/                 # database scripts
    ├── src/                # source files
    │   └──cardImporter     # fetch & import new card info
    └── test/               # unit tests

### Getting Started
#### Install
```shell
$ git clone git@github.com:yharnam/mtg-foundry.git
$ npm i
```

#### Configure
* Install MySQL locallyL (ref: [MySQL Installation Guide](https://dev.mysql.com/doc/mysql-installation-excerpt/8.0/en/))
* Initialize this database by running `db/dbInit.sql`
* Create `db/database.json` and populate it with the following information:
    ```json
    {
      "defaultEnv": "localhost",
      "localhost": {
        "driver": "mysql",
        "host": "localhost",
        "user": "",
        "password": "",
        "database": "foundry_db",
        "multipleStatements": true
      },
      "sql-file" : true
    }
    ```
* Update your db schema to the latest version by running `$ npm run db-up`


## Features
#### Codex
It supplements card information with crowd sourced cEDH metadata to provide a unique deck building resource.

#### cEDH Content Aggregation By Commander
> coming soon...