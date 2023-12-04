---
title: roslynator configuration in MegaLinter
description: How to use roslynator (configure, ignore files, ignore errors, help & version documentations) to analyze CSHARP files
---
<!-- markdownlint-disable MD033 MD041 -->
<!-- @generated by .automation/build.py, please don't update manually -->
# <a href="https://github.com/JosefPihrt/Roslynator" target="blank" title="Visit linter Web Site"><img src="http://pihrt.net/images/Roslynator.ico" alt="roslynator" height="100px" class="megalinter-logo"></a>roslynator
[![GitHub stars](https://img.shields.io/github/stars/JosefPihrt/Roslynator?cacheSeconds=3600)](https://github.com/JosefPihrt/Roslynator) ![formatter](https://shields.io/badge/-format-yellow) [![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/JosefPihrt/Roslynator?sort=semver)](https://github.com/JosefPihrt/Roslynator/releases) [![GitHub last commit](https://img.shields.io/github/last-commit/JosefPihrt/Roslynator)](https://github.com/JosefPihrt/Roslynator/commits) [![GitHub commit activity](https://img.shields.io/github/commit-activity/y/JosefPihrt/Roslynator)](https://github.com/JosefPihrt/Roslynator/graphs/commit-activity/) [![GitHub contributors](https://img.shields.io/github/contributors/JosefPihrt/Roslynator)](https://github.com/JosefPihrt/Roslynator/graphs/contributors/)

## roslynator documentation

- Version in MegaLinter: **0.8.0.0**
- Visit [Official Web Site](https://github.com/JosefPihrt/Roslynator#readme){target=_blank}
- See [How to configure roslynator rules](https://github.com/JosefPihrt/Roslynator/blob/main/docs/Configuration.md){target=_blank}

[![Roslynator - GitHub](https://gh-card.dev/repos/JosefPihrt/Roslynator.svg?fullname=)](https://github.com/JosefPihrt/Roslynator){target=_blank}

## Configuration in MegaLinter

- Enable roslynator by adding `CSHARP_ROSLYNATOR` in [ENABLE_LINTERS variable](https://megalinter.io/beta/configuration/#activation-and-deactivation)
- Disable roslynator by adding `CSHARP_ROSLYNATOR` in [DISABLE_LINTERS variable](https://megalinter.io/beta/configuration/#activation-and-deactivation)

- Enable **autofixes** by adding `CSHARP_ROSLYNATOR` in [APPLY_FIXES variable](https://megalinter.io/beta/configuration/#apply-fixes)

| Variable                                      | Description                                                                                                                                                                                  | Default value      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| CSHARP_ROSLYNATOR_ARGUMENTS                   | User custom arguments to add in linter CLI call<br/>Ex: `-s --foo "bar"`                                                                                                                     |                    |
| CSHARP_ROSLYNATOR_COMMAND_REMOVE_ARGUMENTS    | User custom arguments to remove from command line before calling the linter<br/>Ex: `-s --foo "bar"`                                                                                         |                    |
| CSHARP_ROSLYNATOR_FILTER_REGEX_INCLUDE        | Custom regex including filter<br/>Ex: `(src\|lib)`                                                                                                                                           | Include every file |
| CSHARP_ROSLYNATOR_FILTER_REGEX_EXCLUDE        | Custom regex excluding filter<br/>Ex: `(test\|examples)`                                                                                                                                     | Exclude no file    |
| CSHARP_ROSLYNATOR_CLI_LINT_MODE               | Override default CLI lint mode<br/>- `file`: Calls the linter for each file<br/>- `project`: Call the linter from the root of the project                                                    | `file`             |
| CSHARP_ROSLYNATOR_FILE_EXTENSIONS             | Allowed file extensions. `"*"` matches any extension, `""` matches empty extension. Empty list excludes all files<br/>Ex: `[".py", ""]`                                                      | `[".csproj"]`      |
| CSHARP_ROSLYNATOR_FILE_NAMES_REGEX            | File name regex filters. Regular expression list for filtering files by their base names using regex full match. Empty list includes all files<br/>Ex: `["Dockerfile(-.+)?", "Jenkinsfile"]` | Include every file |
| CSHARP_ROSLYNATOR_PRE_COMMANDS                | List of bash commands to run before the linter                                                                                                                                               | None               |
| CSHARP_ROSLYNATOR_POST_COMMANDS               | List of bash commands to run after the linter                                                                                                                                                | None               |
| CSHARP_ROSLYNATOR_UNSECURED_ENV_VARIABLES     | List of env variables explicitly not filtered before calling CSHARP_ROSLYNATOR and its pre/post commands                                                                                     | None               |
| CSHARP_ROSLYNATOR_DISABLE_ERRORS              | Run linter but consider errors as warnings                                                                                                                                                   | `true`             |
| CSHARP_ROSLYNATOR_DISABLE_ERRORS_IF_LESS_THAN | Maximum number of errors allowed                                                                                                                                                             | `0`                |
| CSHARP_ROSLYNATOR_CLI_EXECUTABLE              | Override CLI executable                                                                                                                                                                      | `['roslynator']`   |

## IDE Integration

Use roslynator in your favorite IDE to catch errors before MegaLinter !

|                                                                   <!-- -->                                                                   | IDE                                                  | Extension Name                                                                                   |                                                                                      Install                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------:|------------------------------------------------------|--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/default.ico" alt="" height="32px" class="megalinter-icon"></a> | visual_studio                                        | [Roslynator 2022](https://marketplace.visualstudio.com/items?itemName=josefpihrt.Roslynator2022) |                                  [Visit Web Site](https://marketplace.visualstudio.com/items?itemName=josefpihrt.Roslynator2022){target=_blank}                                   |
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/vscode.ico" alt="" height="32px" class="megalinter-icon"></a>  | [Visual Studio Code](https://code.visualstudio.com/) | [Roslynator](https://marketplace.visualstudio.com/items?itemName=josefpihrt-vscode.roslynator)   | [![Install in VSCode](https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/btn_install_vscode.png)](vscode:extension/josefpihrt-vscode.roslynator){target=_blank} |

## MegaLinter Flavours

This linter is available in the following flavours

|                                                                         <!-- -->                                                                         | Flavor                                                       | Description                                              | Embedded linters |                                                                                                                                                                                             Info |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------|:---------------------------------------------------------|:----------------:|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/mega-linter-square.png" alt="" height="32px" class="megalinter-icon"></a> | [all](https://megalinter.io/beta/supported-linters/)         | Default MegaLinter Flavor                                |       121        |                       ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter) |
|       <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/dotnet.ico" alt="" height="32px" class="megalinter-icon"></a>        | [dotnet](https://megalinter.io/beta/flavors/dotnet/)         | Optimized for C, C++, C# or VB based projects            |        64        |         ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-dotnet/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-dotnet) |
|      <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/dotnetweb.ico" alt="" height="32px" class="megalinter-icon"></a>      | [dotnetweb](https://megalinter.io/beta/flavors/dotnetweb/)   | Optimized for C, C++, C# or VB based projects with JS/TS |        73        |   ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-dotnetweb/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-dotnetweb) |
|     <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/formatters.ico" alt="" height="32px" class="megalinter-icon"></a>      | [formatters](https://megalinter.io/beta/flavors/formatters/) | Contains only formatters                                 |        17        | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-formatters/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-formatters) |

## Behind the scenes

### How are identified applicable files

- File extensions: `.csproj`

<!-- markdownlint-disable -->
<!-- /* cSpell:disable */ -->
### How the linting is performed

- roslynator is called one time by identified file (`file` CLI lint mode)

### Example calls

```shell
roslynator analyze myproject.csproj
```

```shell
roslynator fix myproject.csproj
```


### Help content

```shell
Roslynator Command Line Tool version 0.8.0.0 (Roslyn version 4.7.0.0)
Usage: roslynator [command] [arguments]

Commands:
  analyze            Analyzes specified project or solution and reports diagnostics.
  find-symbol        Finds symbols in the specified project or solution.
  fix                Fixes diagnostics in the specified project or solution.
  format             Formats whitespace in the specified project or solution.
  generate-doc       Generates reference documentation from specified project/solution.
  generate-doc-root  [deprecated] Generates root documentation file from specified project/solution.
  list-symbols       Lists symbols from the specified project or solution.
  lloc               Counts logical lines of code in the specified project or solution.
  loc                Counts physical lines of code in the specified project or solution.
  migrate            Migrates analyzers to a new version.
  rename-symbol      Rename symbols in the specified project or solution.
  spellcheck         Searches the specified project or solution for possible misspellings or typos.

Run 'roslynator help [command]' for more information on a command.
```

### Installation on mega-linter Docker image

- Dockerfile commands :
```dockerfile
# Parent descriptor install
RUN wget --tries=5 -q -O dotnet-install.sh https://dot.net/v1/dotnet-install.sh \
    && chmod +x dotnet-install.sh \
    && ./dotnet-install.sh --install-dir /usr/share/dotnet -channel 6.0 -version latest

ENV PATH="${PATH}:/root/.dotnet/tools:/usr/share/dotnet"
# Linter install
RUN wget --tries=5 -q -O dotnet-install.sh https://dot.net/v1/dotnet-install.sh \
    && chmod +x dotnet-install.sh \
    && ./dotnet-install.sh --install-dir /usr/share/dotnet -channel 6.0 -version latest

ENV PATH="${PATH}:/root/.dotnet/tools:/usr/share/dotnet"
RUN /usr/share/dotnet/dotnet tool install -g roslynator.dotnet.cli
```
