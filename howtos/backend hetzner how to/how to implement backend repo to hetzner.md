

## What Do You need:

- a backend repo that is working locally
- a repo on GitHub


-  Clone your repo on your hetzner machine in your desired path
- make sure you have your `.env` file ready with the connection string(s)
- add [npm scripts needed for deploying repos on hetzner](../../../devops/npm%20scripts%20needed%20for%20deploying%20repos%20on%20hetzner.md) to your `package.json`  
	- you will need `npm run start` initiate your project in `pm2`
	- whenever you make a local change you will need `npm run deploy`
- when using ``nodemon`` insert following scripts instead:
```JSON
"dev": "npm run build && nodemon", "build": "tsc --build", "start": "node dist/server.js", "setup": "npm i && npm build && pm2 start --name starters-backend npm -- start", "deploy": "git pull --no-rebase && npm i && npm run build && pm2 restart starters-backend --update-env --time && pm2 save"
```

-  you will need a ``tsconfig.json`` when using typescript
- 










### ts.config options:

`noEmit`: 
The `noEmit` option in a TypeScript (tsconfig.json) configuration file is used to instruct the TypeScript compiler (tsc) not to emit any output files during the compilation process. When `noEmit` is set to `true`, the compiler will only type-check the TypeScript code and report errors if any, but it won't generate any JavaScript files or other compiled output.

