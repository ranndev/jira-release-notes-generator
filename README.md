jira-release-notes-generator (jrng)
===================================

This project is a CLI tool built with [oclif](https://oclif.io) for generating release notes in Jira.

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
$ npm install -g jira-release-notes-generator
$ jrng COMMAND
running command...
$ jrng (--version)
jira-release-notes-generator/0.0.0 darwin-x64 node-v14.17.5
$ jrng --help [COMMAND]
USAGE
  $ jrng COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`jrng hello PERSON`](#jrng-hello-person)
* [`jrng hello world`](#jrng-hello-world)
* [`jrng help [COMMAND]`](#jrng-help-command)
* [`jrng plugins`](#jrng-plugins)
* [`jrng plugins:install PLUGIN...`](#jrng-pluginsinstall-plugin)
* [`jrng plugins:inspect PLUGIN...`](#jrng-pluginsinspect-plugin)
* [`jrng plugins:install PLUGIN...`](#jrng-pluginsinstall-plugin-1)
* [`jrng plugins:link PLUGIN`](#jrng-pluginslink-plugin)
* [`jrng plugins:uninstall PLUGIN...`](#jrng-pluginsuninstall-plugin)
* [`jrng plugins:uninstall PLUGIN...`](#jrng-pluginsuninstall-plugin-1)
* [`jrng plugins:uninstall PLUGIN...`](#jrng-pluginsuninstall-plugin-2)
* [`jrng plugins update`](#jrng-plugins-update)

## `jrng hello PERSON`

Say hello

```
USAGE
  $ jrng hello [PERSON] -f <value>

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

_See code: [dist/commands/hello/index.ts](https://github.com/ranndev/jira-release-notes-generator/blob/v0.0.0/dist/commands/hello/index.ts)_

## `jrng hello world`

Say hello world

```
USAGE
  $ jrng hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ jrng hello world
  hello world! (./src/commands/hello/world.ts)
```

## `jrng help [COMMAND]`

Display help for jrng.

```
USAGE
  $ jrng help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for jrng.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.19/src/commands/help.ts)_

## `jrng plugins`

List installed plugins.

```
USAGE
  $ jrng plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ jrng plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.7/src/commands/plugins/index.ts)_

## `jrng plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ jrng plugins:install PLUGIN...

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
  $ jrng plugins add

EXAMPLES
  $ jrng plugins:install myplugin 

  $ jrng plugins:install https://github.com/someuser/someplugin

  $ jrng plugins:install someuser/someplugin
```

## `jrng plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ jrng plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ jrng plugins:inspect myplugin
```

## `jrng plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ jrng plugins:install PLUGIN...

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
  $ jrng plugins add

EXAMPLES
  $ jrng plugins:install myplugin 

  $ jrng plugins:install https://github.com/someuser/someplugin

  $ jrng plugins:install someuser/someplugin
```

## `jrng plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ jrng plugins:link PLUGIN

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
  $ jrng plugins:link myplugin
```

## `jrng plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ jrng plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jrng plugins unlink
  $ jrng plugins remove
```

## `jrng plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ jrng plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jrng plugins unlink
  $ jrng plugins remove
```

## `jrng plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ jrng plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jrng plugins unlink
  $ jrng plugins remove
```

## `jrng plugins update`

Update installed plugins.

```
USAGE
  $ jrng plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
