---
title: php-cs-fixer configuration in MegaLinter
description: How to use php-cs-fixer (configure, ignore files, ignore errors, help & version documentations) to analyze PHP files
---
<!-- markdownlint-disable MD033 MD041 -->
<!-- @generated by .automation/build.py, please don't update manually -->
# <a href="https://cs.symfony.com/" target="blank" title="Visit linter Web Site"><img src="https://cs.symfony.com/_static/images/logo.png" alt="php-cs-fixer" height="100px" class="megalinter-logo"></a>php-cs-fixer
[![GitHub stars](https://img.shields.io/github/stars/PHP-CS-Fixer/PHP-CS-Fixer?cacheSeconds=3600)](https://github.com/PHP-CS-Fixer/PHP-CS-Fixer) [![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/PHP-CS-Fixer/PHP-CS-Fixer?sort=semver)](https://github.com/PHP-CS-Fixer/PHP-CS-Fixer/releases) [![GitHub last commit](https://img.shields.io/github/last-commit/PHP-CS-Fixer/PHP-CS-Fixer)](https://github.com/PHP-CS-Fixer/PHP-CS-Fixer/commits) [![GitHub commit activity](https://img.shields.io/github/commit-activity/y/PHP-CS-Fixer/PHP-CS-Fixer)](https://github.com/PHP-CS-Fixer/PHP-CS-Fixer/graphs/commit-activity/) [![GitHub contributors](https://img.shields.io/github/contributors/PHP-CS-Fixer/PHP-CS-Fixer)](https://github.com/PHP-CS-Fixer/PHP-CS-Fixer/graphs/contributors/)

## php-cs-fixer documentation

- Version in MegaLinter: **3.59.1**
- Visit [Official Web Site](https://cs.symfony.com/){target=_blank}
  - If custom `.php-cs-fixer.dist.php` config file isn't found, [.php-cs-fixer.dist.php](https://github.com/oxsecurity/megalinter/tree/main/TEMPLATES/.php-cs-fixer.dist.php){target=_blank} will be used

[![PHP-CS-Fixer - GitHub](https://gh-card.dev/repos/PHP-CS-Fixer/PHP-CS-Fixer.svg?fullname=)](https://github.com/PHP-CS-Fixer/PHP-CS-Fixer){target=_blank}

## Configuration in MegaLinter

- Enable php-cs-fixer by adding `PHP_PHPCSFIXER` in [ENABLE_LINTERS variable](https://megalinter.io/beta/configuration/#activation-and-deactivation)
- Disable php-cs-fixer by adding `PHP_PHPCSFIXER` in [DISABLE_LINTERS variable](https://megalinter.io/beta/configuration/#activation-and-deactivation)

| Variable                                   | Description                                                                                                                                                                                  | Default value                                   |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| PHP_PHPCSFIXER_ARGUMENTS                   | User custom arguments to add in linter CLI call<br/>Ex: `-s --foo "bar"`                                                                                                                     |                                                 |
| PHP_PHPCSFIXER_COMMAND_REMOVE_ARGUMENTS    | User custom arguments to remove from command line before calling the linter<br/>Ex: `-s --foo "bar"`                                                                                         |                                                 |
| PHP_PHPCSFIXER_FILE_EXTENSIONS             | Allowed file extensions. `"*"` matches any extension, `""` matches empty extension. Empty list excludes all files<br/>Ex: `[".py", ""]`                                                      | `[".php"]`                                      |
| PHP_PHPCSFIXER_FILE_NAMES_REGEX            | File name regex filters. Regular expression list for filtering files by their base names using regex full match. Empty list includes all files<br/>Ex: `["Dockerfile(-.+)?", "Jenkinsfile"]` | Include every file                              |
| PHP_PHPCSFIXER_PRE_COMMANDS                | List of bash commands to run before the linter                                                                                                                                               | None                                            |
| PHP_PHPCSFIXER_POST_COMMANDS               | List of bash commands to run after the linter                                                                                                                                                | None                                            |
| PHP_PHPCSFIXER_UNSECURED_ENV_VARIABLES     | List of env variables explicitly not filtered before calling PHP_PHPCSFIXER and its pre/post commands                                                                                        | None                                            |
| PHP_PHPCSFIXER_CONFIG_FILE                 | php-cs-fixer configuration file name</br>Use `LINTER_DEFAULT` to let the linter find it                                                                                                      | `.php-cs-fixer.dist.php`                        |
| PHP_PHPCSFIXER_RULES_PATH                  | Path where to find linter configuration file                                                                                                                                                 | Workspace folder, then MegaLinter default rules |
| PHP_PHPCSFIXER_DISABLE_ERRORS              | Run linter but consider errors as warnings                                                                                                                                                   | `false`                                         |
| PHP_PHPCSFIXER_DISABLE_ERRORS_IF_LESS_THAN | Maximum number of errors allowed                                                                                                                                                             | `0`                                             |
| PHP_PHPCSFIXER_CLI_EXECUTABLE              | Override CLI executable                                                                                                                                                                      | `['php-cs-fixer']`                              |

## IDE Integration

Use php-cs-fixer in your favorite IDE to catch errors before MegaLinter !

|                                                                   <!-- -->                                                                   | IDE                                                      | Extension Name                                                                  |                                             Install                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------:|----------------------------------------------------------|---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/default.ico" alt="" height="32px" class="megalinter-icon"></a> | netbeans                                                 | [PHP-CS-Fixer](https://plugins.netbeans.apache.org/catalogue/?id=36)            |      [Visit Web Site](https://plugins.netbeans.apache.org/catalogue/?id=36){target=_blank}       |
|  <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/idea.ico" alt="" height="32px" class="megalinter-icon"></a>   | [IDEA](https://www.jetbrains.com/products.html#type=ide) | [php-cs-fixer](https://www.jetbrains.com/help/phpstorm/using-php-cs-fixer.html) | [Visit Web Site](https://www.jetbrains.com/help/phpstorm/using-php-cs-fixer.html){target=_blank} |
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/sublime.ico" alt="" height="32px" class="megalinter-icon"></a> | [Sublime Text](https://www.sublimetext.com/)             | [sublime-phpcs](https://github.com/benmatselby/sublime-phpcs)                   |          [Visit Web Site](https://github.com/benmatselby/sublime-phpcs){target=_blank}           |
|   <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/vim.ico" alt="" height="32px" class="megalinter-icon"></a>   | [vim](https://www.vim.org/)                              | [vim-php-cs-fixer](https://github.com/stephpy/vim-php-cs-fixer)                 |           [Visit Web Site](https://github.com/stephpy/vim-php-cs-fixer){target=_blank}           |
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/vscode.ico" alt="" height="32px" class="megalinter-icon"></a>  | [Visual Studio Code](https://code.visualstudio.com/)     | [vscode-php-cs-fixer](https://github.com/junstyle/vscode-php-cs-fixer)          |         [Visit Web Site](https://github.com/junstyle/vscode-php-cs-fixer){target=_blank}         |

## MegaLinter Flavours

This linter is available in the following flavours

|                                                                         <!-- -->                                                                         | Flavor                                                 | Description                                     | Embedded linters |                                                                                                                                                                                       Info |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------|:------------------------------------------------|:----------------:|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/mega-linter-square.png" alt="" height="32px" class="megalinter-icon"></a> | [all](https://megalinter.io/beta/supported-linters/)   | Default MegaLinter Flavor                       |       124        |                 ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter) |
|       <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/cupcake.ico" alt="" height="32px" class="megalinter-icon"></a>       | [cupcake](https://megalinter.io/beta/flavors/cupcake/) | MegaLinter for the most commonly used languages |        83        | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-cupcake/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-cupcake) |
|         <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/php.ico" alt="" height="32px" class="megalinter-icon"></a>         | [php](https://megalinter.io/beta/flavors/php/)         | Optimized for PHP based projects                |        55        |         ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-php/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-php) |

## Behind the scenes

### How are identified applicable files

- File extensions: `.php`

<!-- markdownlint-disable -->
<!-- /* cSpell:disable */ -->
### How the linting is performed

php-cs-fixer is called once on the whole project directory (`project` CLI lint mode)

- filtering can not be done using MegaLinter configuration variables,it must be done using php-cs-fixer configuration or ignore file (if existing)
- `VALIDATE_ALL_CODEBASE: false` doesn't make php-cs-fixer analyze only updated files

### Example calls

```shell
php-cs-fixer check myfile.php
```

```shell
php-cs-fixer check mydir
```

```shell
php-cs-fixer check --config .php-cs-fixer.php
```


### Help content

```shell
Description:
  List commands

Usage:
  list [options] [--] [<namespace>]

Arguments:
  namespace             The namespace name

Options:
      --raw             To output raw command list
      --format=FORMAT   The output format (txt, xml, json, or md) [default: "txt"]
      --short           To skip describing commands' arguments
  -h, --help            Display help for the given command. When no command is given display help for the list command
  -q, --quiet           Do not output any message
  -V, --version         Display this application version
      --ansi|--no-ansi  Force (or disable --no-ansi) ANSI output
  -n, --no-interaction  Do not ask any interactive question
  -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug

Help:
  The list command lists all commands:

    /root/.composer/vendor/bin/php-cs-fixer list

  You can also display the commands for a specific namespace:

    /root/.composer/vendor/bin/php-cs-fixer list test

  You can also output the information in other formats by using the --format option:

    /root/.composer/vendor/bin/php-cs-fixer list --format=xml

  It's also possible to get raw list of commands (useful for embedding command runner):

    /root/.composer/vendor/bin/php-cs-fixer list --raw
```

### Installation on mega-linter Docker image

- Dockerfile commands :
```dockerfile
# Parent descriptor install
RUN GITHUB_AUTH_TOKEN="$(cat /run/secrets/GITHUB_TOKEN)" \
    && export GITHUB_AUTH_TOKEN \
    && wget --tries=5 -q -O phive.phar https://phar.io/releases/phive.phar \
    && wget --tries=5 -q -O phive.phar.asc https://phar.io/releases/phive.phar.asc \
    && PHAR_KEY_ID="0x6AF725270AB81E04D79442549D8A98B29B2D5D79" \
    && ( gpg --keyserver hkps://keys.openpgp.org --recv-keys "$PHAR_KEY_ID" \
       || gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$PHAR_KEY_ID" \
       || gpg --keyserver keyserver.pgp.com --recv-keys "$PHAR_KEY_ID" \
       || gpg --keyserver pgp.mit.edu --recv-keys "$PHAR_KEY_ID" ) \
    && gpg --verify phive.phar.asc phive.phar \
    && chmod +x phive.phar \
    && mv phive.phar /usr/local/bin/phive \
    && rm phive.phar.asc \
    && update-alternatives --install /usr/bin/php php /usr/bin/php83 110

COPY --from=composer/composer:2-bin /composer /usr/bin/composer
ENV PATH="/root/.composer/vendor/bin:${PATH}"
# Linter install
RUN GITHUB_AUTH_TOKEN="$(cat /run/secrets/GITHUB_TOKEN)" && export GITHUB_AUTH_TOKEN && composer global require friendsofphp/php-cs-fixer

```
