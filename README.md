oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g lang-drop
$ lang-drop COMMAND
running command...
$ lang-drop (--version)
lang-drop/0.0.0 linux-x64 node-v16.15.1
$ lang-drop --help [COMMAND]
USAGE
  $ lang-drop COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`lang-drop hello PERSON`](#lang-drop-hello-person)
* [`lang-drop hello world`](#lang-drop-hello-world)
* [`lang-drop help [COMMANDS]`](#lang-drop-help-commands)
* [`lang-drop plugins`](#lang-drop-plugins)
* [`lang-drop plugins:install PLUGIN...`](#lang-drop-pluginsinstall-plugin)
* [`lang-drop plugins:inspect PLUGIN...`](#lang-drop-pluginsinspect-plugin)
* [`lang-drop plugins:install PLUGIN...`](#lang-drop-pluginsinstall-plugin-1)
* [`lang-drop plugins:link PLUGIN`](#lang-drop-pluginslink-plugin)
* [`lang-drop plugins:uninstall PLUGIN...`](#lang-drop-pluginsuninstall-plugin)
* [`lang-drop plugins:uninstall PLUGIN...`](#lang-drop-pluginsuninstall-plugin-1)
* [`lang-drop plugins:uninstall PLUGIN...`](#lang-drop-pluginsuninstall-plugin-2)
* [`lang-drop plugins update`](#lang-drop-plugins-update)

## `lang-drop hello PERSON`

Say hello

```
USAGE
  $ lang-drop hello PERSON -f <value>

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

_See code: [dist/commands/hello/index.ts](https://github.com/lappjeff/lang-drop/blob/v0.0.0/dist/commands/hello/index.ts)_

## `lang-drop hello world`

Say hello world

```
USAGE
  $ lang-drop hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ lang-drop hello world
  hello world! (./src/commands/hello/world.ts)
```

## `lang-drop help [COMMANDS]`

Display help for lang-drop.

```
USAGE
  $ lang-drop help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for lang-drop.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.8/src/commands/help.ts)_

## `lang-drop plugins`

List installed plugins.

```
USAGE
  $ lang-drop plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ lang-drop plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.4.3/src/commands/plugins/index.ts)_

## `lang-drop plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ lang-drop plugins:install PLUGIN...

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
  $ lang-drop plugins add

EXAMPLES
  $ lang-drop plugins:install myplugin 

  $ lang-drop plugins:install https://github.com/someuser/someplugin

  $ lang-drop plugins:install someuser/someplugin
```

## `lang-drop plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ lang-drop plugins:inspect PLUGIN...

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
  $ lang-drop plugins:inspect myplugin
```

## `lang-drop plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ lang-drop plugins:install PLUGIN...

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
  $ lang-drop plugins add

EXAMPLES
  $ lang-drop plugins:install myplugin 

  $ lang-drop plugins:install https://github.com/someuser/someplugin

  $ lang-drop plugins:install someuser/someplugin
```

## `lang-drop plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ lang-drop plugins:link PLUGIN

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
  $ lang-drop plugins:link myplugin
```

## `lang-drop plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ lang-drop plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ lang-drop plugins unlink
  $ lang-drop plugins remove
```

## `lang-drop plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ lang-drop plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ lang-drop plugins unlink
  $ lang-drop plugins remove
```

## `lang-drop plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ lang-drop plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ lang-drop plugins unlink
  $ lang-drop plugins remove
```

## `lang-drop plugins update`

Update installed plugins.

```
USAGE
  $ lang-drop plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
