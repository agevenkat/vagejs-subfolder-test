# vagejs on a GitHub Pages project site

A small example site built with [vagejs](https://vagejs.com), live at **https://agevenkat.github.io/vagejs-subfolder-test/**.

GitHub Pages serves a repository like this one from a subfolder (`/vagejs-subfolder-test/`), not from the root of the domain. One line in `vage.config.ts` makes that work:

```ts
site: "https://agevenkat.github.io/vagejs-subfolder-test",
```

vagejs then adds `/vagejs-subfolder-test` to every link, image, script and stylesheet in the build. Pages still link to each other from the site root (`/about/`), and `npm run check` checks them as usual.

## Try it

```bash
npm install
npm run preview   # after npm run build: serves the site under /vagejs-subfolder-test/, as GitHub does
npx vage deploy   # builds, checks and publishes to GitHub Pages
```

See [Deployment: GitHub Pages](https://vagejs.com/docs/deployment/#github-pages) in the vagejs docs.
