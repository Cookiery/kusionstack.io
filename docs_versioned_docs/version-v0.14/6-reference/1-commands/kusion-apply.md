# kusion apply

Apply the operational intent of various resources to multiple runtimes

## Synopsis

Apply a series of resource changes within the stack.

 Create, update or delete resources according to the operational intent within a stack. By default, Kusion will generate an execution preview and prompt for your approval before performing any actions. You can review the preview details and make a decision to proceed with the actions or abort them.

```
kusion apply [flags]
```

## Examples

```
  # Apply with specified work directory
  kusion apply -w /path/to/workdir
  
  # Apply with specified arguments
  kusion apply -D name=test -D age=18
  
  # Apply with specifying spec file
  kusion apply --spec-file spec.yaml
  
  # Skip interactive approval of preview details before applying
  kusion apply --yes
  
  # Apply without output style and color
  kusion apply --no-style=true
  
  # Apply without watching the resource changes and waiting for reconciliation
  kusion apply --watch=false
  
  # Apply with the specified timeout duration for kusion apply command, measured in second(s)
  kusion apply --timeout=120
  
  # Apply with localhost port forwarding
  kusion apply --port-forward=8080
```

## Options

```
  -a, --all --detail            Automatically show all preview details, combined use with flag --detail
  -D, --argument stringArray    Specify arguments on the command line
      --backend string          The backend to use, supports 'local', 'oss' and 's3'.
  -d, --detail                  Automatically show preview details with interactive options (default true)
      --dry-run                 Preview the execution effect (always successful) without actually applying the changes
  -h, --help                    help for apply
      --ignore-fields strings   Ignore differences of target fields
      --no-style                no-style sets to RawOutput mode and disables all of styling
  -o, --output string           Specify the output format
      --port-forward int        Forward the specified port from local to service
      --spec-file string        Specify the spec file path as input, and the spec file must be located in the working directory or its subdirectories
      --timeout int             The timeout duration for kusion apply command, measured in second(s)
      --watch                   After creating/updating/deleting the requested object, watch for changes (default true)
  -w, --workdir string          The work directory to run Kusion CLI.
      --workspace string        The name of target workspace to operate in.
  -y, --yes                     Automatically approve and perform the update after previewing it
```

## Options inherited from parent commands

```
      --profile string          Name of profile to capture. One of (none|cpu|heap|goroutine|threadcreate|block|mutex) (default "none")
      --profile-output string   Name of the file to write the profile to (default "profile.pprof")
```

## SEE ALSO

* [kusion](index.md)	 - Kusion is the Platform Orchestrator of Internal Developer Platform
		
Find more information at: https://www.kusionstack.io

###### Auto generated by spf13/cobra on 21-Jan-2025
