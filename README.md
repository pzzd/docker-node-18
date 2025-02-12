# docker-node-18

Clone a Node app to the app directory.

Run with `docker compose up -d`. The app will be started with `npm start` in the compose file.

Make sure you can see http://localhost:3000 in a browser.

## Troubleshooting


Running `npm install -g @sitecore-jss/sitecore-jss-cli` I get this error.
```
npm error code EACCES
npm error syscall mkdir
npm error path /usr/local/lib/node_modules/@sitecore-jss
npm error errno -13
npm error [Error: EACCES: permission denied, mkdir '/usr/local/lib/node_modules/@sitecore-jss'] {
npm error   errno: -13,
npm error   code: 'EACCES',
npm error   syscall: 'mkdir',
npm error   path: '/usr/local/lib/node_modules/@sitecore-jss'
npm error }
```
Try `chown -R node /usr/local/lib/node_modules/` and run your command again.
