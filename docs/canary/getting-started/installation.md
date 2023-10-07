---
description: |
  Create a new Fresh project by running the Fresh project creation tool. This
  scaffolds out the various files and folders a Fresh project needs.
---

> [info]: The documentation assumes you have Deno `1.35.0` or later installed.
> To install Deno, follow the
> [installation instructions](https://deno.land/manual/getting_started/installation)
> in the Deno manual. For the best user experience, you should also
> [set up your editor or IDE](https://deno.land/manual/getting_started/setup_your_environment)
> to play nice with Deno.

To create a new project, run:

```sh Terminal
deno run -A -r https://fresh.deno.dev
```

This will scaffold out the new project with the following folder structure:

```txt Project structure
├── islands/      # Interactive component folder
|   └── ...
├── routes/       # Route files that map to URLs
|   └── ...
├── dev.ts        # starts Fresh in development mode
├── main.ts       # starts Fresh in production mode
├── fresh.gen.ts  # autogenerated meta file
└── deno.json     # Deno's configuration file
```

The next step after scaffolding out a new project, is to actually start it. To
do this you can run `deno task start`. Environment variables will be
automatically read from `.env`.

```sh Terminal
$ deno task start
Watcher Process started.
 🍋 Fresh ready
     Local: http://localhost:8000
```

Go to the URL printed in the terminal to see your running project. Try change
some of the text in `routes/index.tsx` and see how the page updates
automatically when you save the file.

> [info]: Fresh needs a couple of permissions to run. If you're using the
> `deno task start` task then these will be set automatically.
>
> - `--allow-net`: Required to start the HTTP server
> - `--allow-read`: Required to read (static) files from disk
> - `--allow-env`: Required to read environment variables that can be used to
  > configure your project