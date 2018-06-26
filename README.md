# Glitch App on a custom domain

This is a Fly Edge Application that lets you deliver your Glitch apps with custom hostnames/domain names.

## Local development

You can run it locally to see what it does. First clone the repository. Then edit [index.js#L4] with your Glitch Application URL (it uses fly-example by default).

```bash
git clone https://github.com/superfly/glitch-custom-hostnames.git
npm install
npm start
```

Then open http://localhost:3000

## Deploying + adding hostnames

```bash
fly login # register at https://fly.io first
fly apps create <app-name> # create an edge app
fly deploy # deploy your app
fly hostnames add <your-custom-hostname.com> # add a hostname
```