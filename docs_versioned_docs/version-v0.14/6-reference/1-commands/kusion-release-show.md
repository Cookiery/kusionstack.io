# kusion release show

Show details of a release of the current or specified stack

## Synopsis

Show details of a release of the current or specified stack.

This command displays detailed information about a release of the current project in the current or a specified workspace

```
kusion release show [flags]
```

## Examples

```
  # Show details of the latest release of the current project in the current workspace
  kusion release show
  
  # Show details of a specific release of the current project in the current workspace
  kusion release show --revision=1
  
  # Show details of a specific release of the specified project in the specified workspace
  kusion release show --revision=1 --project=hoangndst --workspace=dev
  
  # Show details of the latest release with specified backend
  kusion release show --backend=local
  
  # Show details of the latest release with specified output format
  kusion release show --output=json
```

## Options

```
      --backend string     The backend to use, supports 'local', 'oss' and 's3'
  -h, --help               help for show
  -o, --output string      Specify the output format
      --project string     The project name
      --revision uint      The revision number of the release
      --workspace string   The workspace name
```

## Options inherited from parent commands

```
      --profile string          Name of profile to capture. One of (none|cpu|heap|goroutine|threadcreate|block|mutex) (default "none")
      --profile-output string   Name of the file to write the profile to (default "profile.pprof")
```

## SEE ALSO

* [kusion release](kusion-release.md)	 - Observe and operate Kusion release files

###### Auto generated by spf13/cobra on 21-Jan-2025
