<!--
  _____   ____    _   _  ____ _______   ______ _____ _____ _______
 |  __ \ / __ \  | \ | |/ __ \__   __| |  ____|  __ \_   _|__   __|
 | |  | | |  | | |  \| | |  | | | |    | |__  | |  | || |    | |
 | |  | | |  | | | . ` | |  | | | |    |  __| | |  | || |    | |
 | |__| | |__| | | |\  | |__| | | |    | |____| |__| || |_   | |
 |_____/ \____/  |_| \_|\____/  |_|    |______|_____/_____|  |_|

This file is auto-generated by scripts/update-agent-help.sh, please update the
agent CLI help in https://github.com/buildkite/agent and run the generation
script.

-->

### Usage

`buildkite-agent env get [variables]`

### Description
Retrieves environment variables and their current values from the current job execution environment.

Note that this subcommand is only available from within the job executor with the `job-api` experiment enabled.

Changes to the job environment only apply to the environments of subsequent phases of the job. However, `env get` can be used to inspect the changes made with `env set` and `env unset`.

### Examples

Getting all variables in key=value format:

```
$ buildkite-agent env get
ALPACA=Geronimo the Incredible
BUILDKITE=true
LLAMA=Kuzco
```

Getting the value of one variable:

```
$ buildkite-agent env get LLAMA
Kuzco
```

Getting multiple specific variables:

```
$ buildkite-agent env get LLAMA ALPACA
ALPACA=Geronimo the Incredible
LLAMA=Kuzco
```

Getting variables as a JSON object:

```
$ buildkite-agent env get --format=json-pretty
{
"ALPACA": "Geronimo the Incredible",
"BUILDKITE": "true",
"LLAMA": "Kuzco",
...
}
```


### Options

<!-- vale off -->

<table class="Docs__attribute__table">
<tr id="format"><th><code>--format value</code> <a class="Docs__attribute__link" href="#format">#</a></th><td><p>Output format: plain, json, or json-pretty (default: "plain")<br /><strong>Environment variable</strong>: <code>$BUILDKITE_AGENT_ENV_GET_FORMAT</code></p></td></tr>
</table>

<!-- vale on -->
