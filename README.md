```bash
          __
   ____ _/ /_  ____ _
  / __ `/ __ \/ __ `/
 / /_/ / / / / /_/ /
 \__, /_/ /_/\__,_/
/____/
```

> github actions workflow commands, simplified

[![latest release](https://badgen.net/github/release/KamaranL/gha?icon=github&cache=3600)](https://github.com/KamaranL/gha/releases/latest)

- [Installation and Usage](#installation-and-usage)
  - [Dependencies](#dependencies)
  - [Install](#install)
    - [Local](#local)
    - [GitHub Actions](#github-actions)
  - [Usage](#usage)
- [Validity](#validity)

## Installation and Usage

### Dependencies

- bash `>=3`

### Install

#### Local

While it might not yeild any benefit installing gha scripts on your local machine, there's nothing that says you can't. Just know that commands will not work the same as they would in the GitHub Actions environment.

#### GitHub Actions

```yml
#...
jobs:
  ci:
    runs-on: ubuntu-latest
    steps:
      - uses: KamaranL/gha@main
#...
```

### Usage

The usage is similar to that of the [actions toolkit](https://docs.github.com/en/actions/using-workflows/workflow-commands-for-github-actions#using-workflow-commands-to-access-toolkit-functions), available for javascript/typescript actions. However, these commands become available for use in your workflow file (or composite action), immediately after setup.

```text
usage: core [options]
options:
  add-mask            add a mask to a string or variable to keep it from being printed in the log
  add-path            prepend a directory to the system path for subsequent jobs to use
  debug               print a debug message to the log
  end-group           close an already opened log group (see 'group')
  error               create an error message and print the message to the log
  export-variable     set an environment variable that can be accessed from the current workflow job
  group               create an expandable group in the log
  is-debug            check if debug is enabled on the runner
  notice              create a notice message and print the message to the log
  set-output          set an output variable that can be accessed from subsequent workflow jobs
  summary             print a markdown-capable message to be displayed on the summary page of a workflow run
  warning             create a warning message and print the message to the log
  -v,--version        print the current version of this executable
  -h,--help           print this help message
```

## Validity

Everyone has doubts, see [my wiki page](https://github.com/KamaranL/KamaranL/wiki#validation) on validation if you're like everyone :smile:
