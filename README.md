oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g c-md
$ c-md COMMAND
running command...
$ c-md (--version)
c-md/0.0.0 darwin-arm64 node-v18.17.0
$ c-md --help [COMMAND]
USAGE
  $ c-md COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`c-md hello PERSON`](#c-md-hello-person)
* [`c-md hello world`](#c-md-hello-world)
* [`c-md help [COMMANDS]`](#c-md-help-commands)
* [`c-md plugins`](#c-md-plugins)
* [`c-md plugins:install PLUGIN...`](#c-md-pluginsinstall-plugin)
* [`c-md plugins:inspect PLUGIN...`](#c-md-pluginsinspect-plugin)
* [`c-md plugins:install PLUGIN...`](#c-md-pluginsinstall-plugin-1)
* [`c-md plugins:link PLUGIN`](#c-md-pluginslink-plugin)
* [`c-md plugins:uninstall PLUGIN...`](#c-md-pluginsuninstall-plugin)
* [`c-md plugins:uninstall PLUGIN...`](#c-md-pluginsuninstall-plugin-1)
* [`c-md plugins:uninstall PLUGIN...`](#c-md-pluginsuninstall-plugin-2)
* [`c-md plugins update`](#c-md-plugins-update)

## `c-md hello PERSON`

Say hello

```
USAGE
  $ c-md hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/imjlk/c-md/blob/v0.0.0/dist/commands/hello/index.ts)_

## `c-md hello world`

Say hello world

```
USAGE
  $ c-md hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ c-md hello world
  hello world! (./src/commands/hello/world.ts)
```

## `c-md help [COMMANDS]`

Display help for c-md.

```
USAGE
  $ c-md help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for c-md.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.14/src/commands/help.ts)_

## `c-md plugins`

List installed plugins.

```
USAGE
  $ c-md plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ c-md plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.4.7/src/commands/plugins/index.ts)_

## `c-md plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ c-md plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ c-md plugins add

EXAMPLES
  $ c-md plugins:install myplugin 

  $ c-md plugins:install https://github.com/someuser/someplugin

  $ c-md plugins:install someuser/someplugin
```

## `c-md plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ c-md plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ c-md plugins:inspect myplugin
```

## `c-md plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ c-md plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ c-md plugins add

EXAMPLES
  $ c-md plugins:install myplugin 

  $ c-md plugins:install https://github.com/someuser/someplugin

  $ c-md plugins:install someuser/someplugin
```

## `c-md plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ c-md plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ c-md plugins:link myplugin
```

## `c-md plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ c-md plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ c-md plugins unlink
  $ c-md plugins remove
```

## `c-md plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ c-md plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ c-md plugins unlink
  $ c-md plugins remove
```

## `c-md plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ c-md plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ c-md plugins unlink
  $ c-md plugins remove
```

## `c-md plugins update`

Update installed plugins.

```
USAGE
  $ c-md plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
