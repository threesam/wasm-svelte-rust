# Svelte + Rust (WASM) App Template

This is a project template for Svelte apps that integrates Rust (WASM) as well.

To create a new project based on this template using cargo-generate:

```bash
cargo generate --git https://git.stlrust.org/j4ng5y/svelte-wasm-template --branch main --name <my app name>
cd <my app name>
```

## Prereqs

* Cargo-generate installed (just to get the template -- `cargo install cargo-generate`)
* Node.js installed
* Rust installed
* wasm-pack installed

## Get Started

Install the dependencies...

```bash
cd <my app name>
npm install
```

...then start Rollup:

```bash
npm run dev
```

Navigate to localhost:5000. You should see your app running. Edit a Svelte component file in `src`, or the WASM component in `src/greeting/src`, save it, restart the dev server to recompile the WASM, and then reload your page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in `package.json` to include the option `--host 0.0.0.0`.

If you're using VSCode, we recommend installing the offical Svelte extension as well as the offical Rust extension. If you are using other editors, your may need to install a plugin in order to get syntax highlighting and intellisense for both Svelte and Rust.

## Building and running in production mode

To create an optimized version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses `sirv`, which is invluded in your `package.json`'s dependencies so that the app will work with you deploy to platforms like Heroku.

## Single-page app mode

By default, `sirv` will only respond to requests that match files in `public`. This is to maximize compatibility with static file servers, allowing you to deploy your app almost anywhere.

If you're building a single-page application (SPA) with multiple routes, `sirv` needs to be able to respond to requests for ANY path. You can make it so by editing the `start` command in `package.json`:

```bash
"start": "sirv public --single"
```

## Deployment

I'll write this section as soon as I deploy it :smile: