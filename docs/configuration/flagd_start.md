<!-- markdownlint-disable-file -->
## flagd start

Start flagd

```
flagd start [flags]
```

### Options

```
  -b, --bearer-token string                 DEPRECATED: Superseded by --sources.
  -C, --cors-origin strings                 CORS allowed origins, * will allow all origins
  -e, --evaluator string                    DEPRECATED: Set an evaluator e.g. json, yaml/yml.Please note that yaml/yml and json evaluations work the same (yaml/yml files are converted to json internally) (default "json")
  -h, --help                                help for start
  -z, --log-format string                   Set the logging format, e.g. console or json  (default "console")
  -m, --metrics-port int32                  Port to serve metrics on (default 8014)
  -p, --port int32                          Port to listen on (default 8013)
  -c, --server-cert-path string             Server side tls certificate path
  -k, --server-key-path string              Server side tls key path
  -d, --socket-path string                  Flagd socket path. With grpc the service will become available on this address. With http(s) the grpc-gateway proxy will use this address internally.
  -s, --sources string                      JSON representation of an array of SourceConfig objects. This object contains 2 required fields, uri (string) and provider (string). Documentation for this object: https://github.com/open-feature/flagd/blob/main/docs/configuration/configuration.md#sync-provider-customisation
  -y, --sync-provider string                DEPRECATED: Set a sync provider e.g. filepath or remote
  -a, --sync-provider-args stringToString   DEPRECATED: Sync provider arguments as key values separated by = (default [])
  -f, --uri .yaml/.yml/.json                Set a sync provider uri to read data from, this can be a filepath,url (http and grpc) or FeatureFlagConfiguration. When flag keys are duplicated across multiple providers the merge priority follows the index of the flag arguments, as such flags from the uri at index 0 take the lowest precedence, with duplicated keys being overwritten by those from the uri at index 1. Please note that if you are using filepath, flagd only supports files with .yaml/.yml/.json extension.
```

### Options inherited from parent commands

```
      --config string   config file (default is $HOME/.agent.yaml)
  -x, --debug           verbose logging
```

### SEE ALSO

* [flagd](flagd)	 - Flagd is a simple command line tool for fetching and presenting feature flags to services. It is designed to conform to Open Feature schema for flag definitions.

