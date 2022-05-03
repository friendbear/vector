# vector

* [top](https://vector.dev/)

## create alias

```.bash_aliases
alias vector='sudo docker run -i --rm timberio/vector:0.21.1-debian'
```

## help

```sh
$ vector --help
vector 0.21.1 (armv7-unknown-linux-gnueabihf 18787c0 2022-04-22)

USAGE:
    vector [OPTIONS] [SUBCOMMAND]

OPTIONS:
    -c, --config <config>
            Read configuration from one or more files. Wildcard paths are supported. File format is
            detected from the file name. If zero files are specified the default config path
            `/etc/vector/vector.toml` will be targeted

            [env: VECTOR_CONFIG=]

    -C, --config-dir <config-dir>
            Read configuration from files in one or more directories. File format is detected from
            the file name.

            Files not ending in .toml, .json, .yaml, or .yml will be ignored.

            [env: VECTOR_CONFIG_DIR=]

        --config-toml <config-toml>
            Read configuration from one or more files. Wildcard paths are supported. TOML file
            format is expected

            [env: VECTOR_CONFIG_TOML=]

        --config-json <config-json>
            Read configuration from one or more files. Wildcard paths are supported. JSON file
            format is expected

            [env: VECTOR_CONFIG_JSON=]

        --config-yaml <config-yaml>
            Read configuration from one or more files. Wildcard paths are supported. YAML file
            format is expected

            [env: VECTOR_CONFIG_YAML=]

    -r, --require-healthy <REQUIRE_HEALTHY>
            Exit on startup if any sinks fail healthchecks

            [env: VECTOR_REQUIRE_HEALTHY=]

    -t, --threads <THREADS>
            Number of threads to use for processing (default is number of available cores)

            [env: VECTOR_THREADS=]

    -v, --verbose
            Enable more detailed internal logging. Repeat to increase level. Overridden by `--quiet`

    -q, --quiet
            Reduce detail of internal logging. Repeat to reduce further. Overrides `--verbose`

        --log-format <LOG_FORMAT>
            Set the logging format

            [env: VECTOR_LOG_FORMAT=]
            [default: text]
            [possible values: text, json]

        --color <COLOR>
            Control when ANSI terminal formatting is used.

            By default `vector` will try and detect if `stdout` is a terminal, if it is ANSI will be
            enabled. Otherwise it will be disabled. By providing this flag with the `--color always`
            option will always enable ANSI terminal formatting. `--color never` will disable all
            ANSI terminal formatting. `--color auto` will attempt to detect it automatically.

            [env: VECTOR_COLOR=]
            [default: auto]
            [possible values: auto, always, never]

    -w, --watch-config
            Watch for changes in configuration file, and reload accordingly

            [env: VECTOR_WATCH_CONFIG=]

    -h, --help
            Print help information

    -V, --version
            Print version information

SUBCOMMANDS:
    validate
            Validate the target config, then exit
    generate
            Generate a Vector configuration containing a list of components
    config
            (experimental) Output a provided Vector configuration file/dir as a single JSON object,
            useful for checking in to version control
    list
            List available components, then exit
    test
            Run Vector config unit tests, then exit. This command is experimental and therefore
            subject to change. For guidance on how to write unit tests check out
            <https://vector.dev/guides/level-up/unit-testing/>
    graph
            Output the topology as visual representation using the DOT language which can be
            rendered by GraphViz
    top
            Display topology and metrics in the console, for a local or remote Vector instance
    tap
            Observe output log events from source or transform components. Logs are sampled at a
            specified interval
    vrl
            Vector Remap Language CLI
    help
            Print this message or the help of the given subcommand(s)
pi@mayurin:~/python_games $ vector -h
vector 0.21.1 (armv7-unknown-linux-gnueabihf 18787c0 2022-04-22)

USAGE:
    vector [OPTIONS] [SUBCOMMAND]

OPTIONS:
    -c, --config <config>
            Read configuration from one or more files. Wildcard paths are supported. File format is
            detected from the file name. If zero files are specified the default config path
            `/etc/vector/vector.toml` will be targeted [env: VECTOR_CONFIG=]

    -C, --config-dir <config-dir>
            Read configuration from files in one or more directories. File format is detected from
            the file name [env: VECTOR_CONFIG_DIR=]

        --config-toml <config-toml>
            Read configuration from one or more files. Wildcard paths are supported. TOML file
            format is expected [env: VECTOR_CONFIG_TOML=]

        --config-json <config-json>
            Read configuration from one or more files. Wildcard paths are supported. JSON file
            format is expected [env: VECTOR_CONFIG_JSON=]

        --config-yaml <config-yaml>
            Read configuration from one or more files. Wildcard paths are supported. YAML file
            format is expected [env: VECTOR_CONFIG_YAML=]

    -r, --require-healthy <REQUIRE_HEALTHY>
            Exit on startup if any sinks fail healthchecks [env: VECTOR_REQUIRE_HEALTHY=]

    -t, --threads <THREADS>
            Number of threads to use for processing (default is number of available cores) [env:
            VECTOR_THREADS=]

    -v, --verbose
            Enable more detailed internal logging. Repeat to increase level. Overridden by `--quiet`

    -q, --quiet
            Reduce detail of internal logging. Repeat to reduce further. Overrides `--verbose`

        --log-format <LOG_FORMAT>
            Set the logging format [env: VECTOR_LOG_FORMAT=] [default: text] [possible values: text,
            json]

        --color <COLOR>
            Control when ANSI terminal formatting is used [env: VECTOR_COLOR=] [default: auto]
            [possible values: auto, always, never]

    -w, --watch-config
            Watch for changes in configuration file, and reload accordingly [env:
            VECTOR_WATCH_CONFIG=]

    -h, --help
            Print help information

    -V, --version
            Print version information

SUBCOMMANDS:
    validate    Validate the target config, then exit
    generate    Generate a Vector configuration containing a list of components
    config      (experimental) Output a provided Vector configuration file/dir as a single JSON
                    object, useful for checking in to version control
    list        List available components, then exit
    test        Run Vector config unit tests, then exit. This command is experimental and
                    therefore subject to change. For guidance on how to write unit tests check out
                    <https://vector.dev/guides/level-up/unit-testing/>
    graph       Output the topology as visual representation using the DOT language which can be
                    rendered by GraphViz
    top         Display topology and metrics in the console, for a local or remote Vector
                    instance
    tap         Observe output log events from source or transform components. Logs are sampled
                    at a specified interval
    vrl         Vector Remap Language CLI
    help        Print this message or the help of the given subcommand(s)
```
