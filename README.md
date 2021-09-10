# npm-workspaces-demo


Things to try


### Installing packages

To install all packages for all workspaces run:

`npm install --workspaces`


To install a package into a single workspace run:

`npm install uuid --workspace=apps/app-a`

This will install at the root `node_modules` as the primary module, however what if `app-b` needs a different version?

`npm install uuid@8.3.1 --workspace=apps/app-b`

This will install uuid@8.3.1 into a `app-b` node_modules folder only.


### Running scripts

only one app

`npm run test --workspace=apps/app-a`

all apps

`npm run test --workspace=apps`

all packages

`npm run test --workspace=packages`

all workspaces (test everything)

`npm run test --workspaces`

### Missing scripts

If any workspace is missing a script you’ll get an error trying to use `--workspaces`. Sometimes you just want to run all the scripts if they exist, and you don’t care if they don’t. There’s an option for this:

`npm run test --workspaces --if-present`


## License

MIT
