# Static Site (w/ Tailwind)

## The Stack
- [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [Tailwindcss](https://tailwindcss.com/docs/installation/)

## How to run
### DEV
- Run `yarn serve:dev` This will _serve_ `src` with `index.html` as your entry point.

- To compile Tailwind CSS manually for `dev` without watching run `yarn compile:css:dev`
> _Note:_ "This ain't no fancy React app K.I.S.S and just hit the refresh button."

### Building for Production
So you actually want to deploy this thing...
- Run `yarn build:all` to do "all the things"
  This will copy over all the `*.html` files to a `/build` directory and compile `app.css` with the `NODE_ENV=production`. This tells Tailwind to use our preset `purge` option from [tailwind.config.js](./tailwind.config.js)

- Copy this `/build` directory to any static hosting site... Or tell your static hosting site to use `/build/index.html` as it's entry point. If you're lucky you can have it run the same `build:all` command for you as well. 

### That's it
That is it folks... Drop in some static HTML, link `index.css`, and have fun.

_Hosted with [Vercel](vercel.com)_ at [mthomps4.com](mthomps4.com)
