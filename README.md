scrypt-h64 for Go
=================

```
package scrypth64 // import "github.com/mjolnir42/scrypth64"

scrypth64 derives password hashes and verifies passwords against them
according to the scrypt-h64 specification. It includes a number of ready to
use parameter sets. The modular crypt format is used, and its de-facto
standard as well as historic precedents are followed.

func Digest(password string, params *Parameter) (string, error)
func Verify(password, mcf string) (bool, error)
func DefaultParams() *Parameter
func HighParams() *Parameter
func PaperParams() *Parameter
type Parameter struct { ... }

func Digest(password string, params *Parameter) (string, error)
    Digest calculates a new scrypt digest and returns it as a scrypt-h64 MCF
    formatted string. If params is nil, DefaultParams are used. Returns an empty
    string if err != nil.

func Verify(password, mcf string) (bool, error)
    Verify takes a password and a scrypt-h64 string in MCF format and returns
    true is the password matches the provided digest. The result is always false
    if error != nil.
```

Specification
=============

See separate file `Specification.md`
