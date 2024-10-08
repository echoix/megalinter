---
title: CSS linters in MegaLinter
description: stylelint is available to analyze CSS files in MegaLinter
---
<!-- markdownlint-disable MD003 MD020 MD033 MD041 -->
<!-- @generated by .automation/build.py, please don't update manually -->
<!-- Instead, update descriptor file at https://github.com/oxsecurity/megalinter/tree/main/megalinter/descriptors/css.yml -->
# CSS

## Linters

| Linter                                                                    | Additional                                                                                                                                                                               |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**stylelint**](css_stylelint.md)<br/>[_CSS_STYLELINT_](css_stylelint.md) | [![GitHub stars](https://img.shields.io/github/stars/stylelint/stylelint?cacheSeconds=3600)](https://github.com/stylelint/stylelint) ![autofix](https://shields.io/badge/-autofix-green) |

## Linted files

- File extensions:
  - `.css`
  - `.scss`
  - `.saas`

## Configuration in MegaLinter

| Variable                 | Description                                     | Default value |
|--------------------------|-------------------------------------------------|---------------|
| CSS_PRE_COMMANDS         | List of bash commands to run before the linters | None          |
| CSS_POST_COMMANDS        | List of bash commands to run after the linters  | None          |
| CSS_FILTER_REGEX_INCLUDE | Custom regex including filter                   |               |
| CSS_FILTER_REGEX_EXCLUDE | Custom regex excluding filter                   |               |

