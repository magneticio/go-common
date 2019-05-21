# go-common

Common libraries for golang projects

This repository contains common resources that we use in Vamp.io

For versioning, we use go modules. Minimum Go 1.12 required.

## logging

This is a logging library we use that enables a verbose mode and logs include file name and line. It makes debugging easier.

```golang
import (
	"github.com/magneticio/go-common/logging"
)
```

In your main code start with:

```golang
logging.Init(os.Stdout, os.Stderr)
```

Set Verbose to true to enable logging
```golang
logging.Verbose = true
```

Print formatted info
```golang
logging.Info("Here is an info with int value: %v\n", 10)
```

Print formatted error
```golang
err := errors.New("This is an error")
logging.Error("Here is an error with error struct: %v\n", err)
```


## util

Util library includes mainly file processing utilities.
We process mainly YAML and JSON files.

```golang
import (
	"github.com/magneticio/go-common/util"
)
```
