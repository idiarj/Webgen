webgen (Not there yet, i am lazy sorry)
=================

Generador de web components mediante linea de comandos.


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/webgen.svg)](https://npmjs.org/package/webgen)
[![Downloads/week](https://img.shields.io/npm/dw/webgen.svg)](https://npmjs.org/package/webgen)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g webgen
$ webgen COMMAND
running command...
$ webgen (--version)
webgen/0.0.0 win32-x64 node-v20.11.0
$ webgen --help [COMMAND]
USAGE
  $ webgen COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`webgen hello PERSON`](#webgen-hello-person)
* [`webgen hello world`](#webgen-hello-world)
* [`webgen help [COMMAND]`](#webgen-help-command)
* [`webgen plugins`](#webgen-plugins)
* [`webgen plugins add PLUGIN`](#webgen-plugins-add-plugin)
* [`webgen plugins:inspect PLUGIN...`](#webgen-pluginsinspect-plugin)
* [`webgen plugins install PLUGIN`](#webgen-plugins-install-plugin)
* [`webgen plugins link PATH`](#webgen-plugins-link-path)
* [`webgen plugins remove [PLUGIN]`](#webgen-plugins-remove-plugin)
* [`webgen plugins reset`](#webgen-plugins-reset)
* [`webgen plugins uninstall [PLUGIN]`](#webgen-plugins-uninstall-plugin)
* [`webgen plugins unlink [PLUGIN]`](#webgen-plugins-unlink-plugin)
* [`webgen plugins update`](#webgen-plugins-update)

## `webgen hello PERSON`

Say hello

```
USAGE
  $ webgen hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ webgen hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/Dise%C3%B1o-de-compiladores/webgen/blob/v0.0.0/src/commands/hello/index.ts)_

## `webgen hello world`

Say hello world

```
USAGE
  $ webgen hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ webgen hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/Dise%C3%B1o-de-compiladores/webgen/blob/v0.0.0/src/commands/hello/world.ts)_

## `webgen help [COMMAND]`

Display help for webgen.

```
USAGE
  $ webgen help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for webgen.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.27/src/commands/help.ts)_

## `webgen plugins`

List installed plugins.

```
USAGE
  $ webgen plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ webgen plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.36/src/commands/plugins/index.ts)_

## `webgen plugins add PLUGIN`

Installs a plugin into webgen.

```
USAGE
  $ webgen plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into webgen.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the WEBGEN_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the WEBGEN_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ webgen plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ webgen plugins add myplugin

  Install a plugin from a github url.

    $ webgen plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ webgen plugins add someuser/someplugin
```

## `webgen plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ webgen plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ webgen plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.36/src/commands/plugins/inspect.ts)_

## `webgen plugins install PLUGIN`

Installs a plugin into webgen.

```
USAGE
  $ webgen plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into webgen.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the WEBGEN_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the WEBGEN_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ webgen plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ webgen plugins install myplugin

  Install a plugin from a github url.

    $ webgen plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ webgen plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.36/src/commands/plugins/install.ts)_

## `webgen plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ webgen plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ webgen plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.36/src/commands/plugins/link.ts)_

## `webgen plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ webgen plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ webgen plugins unlink
  $ webgen plugins remove

EXAMPLES
  $ webgen plugins remove myplugin
```

## `webgen plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ webgen plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.36/src/commands/plugins/reset.ts)_

## `webgen plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ webgen plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ webgen plugins unlink
  $ webgen plugins remove

EXAMPLES
  $ webgen plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.36/src/commands/plugins/uninstall.ts)_

## `webgen plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ webgen plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ webgen plugins unlink
  $ webgen plugins remove

EXAMPLES
  $ webgen plugins unlink myplugin
```

## `webgen plugins update`

Update installed plugins.

```
USAGE
  $ webgen plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.36/src/commands/plugins/update.ts)_
<!-- commandsstop -->
