# Commands

Statusfy comes with a set of useful commands, both for development and production purposes. You can use `--help` with any command to get detailed usage.


## init

Install a new version of Statusfy.

``` bash
statusfy init
```

### Arguments

- `-d` or `--dir`: specify the installation directory (default: current/working directory)

## dev

Starts the application in development mode (hot-code reloading, error reporting, etc.).

``` bash
statusfy dev
```

### Arguments

- `-p <port>` or `--port <port>`: use specified **port** (default: 3000)
- `-s` or `--ssr`: force SSR (Server-Side Rendering)

## build

Compiles the application for production deployment.

``` bash
statusfy build
```

::: warning
After executing this command, you should launch the application using the [`statusfy start`](#start) command.
:::

### Arguments

- `-a` or `--analyze`: launch the final bundle analysis

## generate

Generate a static web application (server-rendered).

``` bash
statusfy generate
```

### Arguments

- `-d` or `--dir`: specify generate output dir (default: ./dist)
- `-a` or `--analyze`: launch the final bundle analysis

## start

Starts the application in production mode.

``` bash
statusfy start
```

::: warning
The application should be compiled with [`statusfy build`](#build) first.
:::

### Arguments

- `-p <port>` or `--port <port>`: use specified **port** (default: 3000)
- `-h <port>` or `--host <host>`: use specified **host** (default: 127.0.0.1)

## new-incident

Creates a new incident after answering a few questions. An initial Markdown file is generated for your incident for all the available languages.

``` bash
statusfy new-incident
```

The name of the created file follows this pattern:

```
YYYY-MM-DD_slug.md
```

where `YYYY-MM-DD` is the ***creation date*** and `slug` a ***short name***.

::: tip TIP
You can skip the Front Matter Format Question by defining the `frontMatterFormat` field in your configuration file. More information in the [Config Reference Guide](../config/README.md#frontmatterformat).
:::