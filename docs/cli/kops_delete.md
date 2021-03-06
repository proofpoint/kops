
<!--- This file is automatically generated by make gen-cli-docs; changes should be made in the go CLI command code (under cmd/kops) -->

## kops delete

Delete clusters,instancegroups, or secrets.

### Synopsis

Delete Kubernetes clusters, instancegroups, and secrets, or a combination of the before mentioned.

```
kops delete -f FILENAME [--yes] [flags]
```

### Examples

```
  # Delete a cluster using a manifest file
  kops delete -f my-cluster.yaml
  
  # Delete a cluster using a pasted manifest file from stdin.
  pbpaste | kops delete -f -
  
  # Delete a cluster in AWS.
  kops delete cluster --name=k8s.example.com --state=s3://kops-state-1234
  
  # Delete an instancegroup for the k8s-cluster.example.com cluster.
  # The --yes option runs the command immediately.
  kops delete ig --name=k8s-cluster.example.com node-example --yes
```

### Options

```
  -f, --filename strings   Filename to use to delete the resource
  -h, --help               help for delete
  -y, --yes                Specify --yes to delete the resource
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --config string                    yaml config file (default is $HOME/.kops.yaml)
      --log_backtrace_at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                   If non-empty, write log files in this directory
      --log_file string                  If non-empty, use this log file
      --log_file_max_size uint           Defines the maximum size a log file can grow to. Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800)
      --logtostderr                      log to standard error instead of files (default true)
      --name string                      Name of cluster. Overrides KOPS_CLUSTER_NAME environment variable
      --skip_headers                     If true, avoid header prefixes in the log messages
      --skip_log_headers                 If true, avoid headers when openning log files
      --state string                     Location of state storage (kops 'config' file). Overrides KOPS_STATE_STORE environment variable
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
  -v, --v Level                          number for the log level verbosity
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [kops](kops.md)	 - kops is Kubernetes ops.
* [kops delete cluster](kops_delete_cluster.md)	 - Delete a cluster.
* [kops delete instancegroup](kops_delete_instancegroup.md)	 - Delete instancegroup
* [kops delete secret](kops_delete_secret.md)	 - Delete a secret

