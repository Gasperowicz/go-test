# go-tuto
mkdir $GOPATH/src/github.com/jerem/stringutil #in that folder, create reverse.go

go build github.com/jerem/helloUsingLibrary/stringutil #Or, in the package's source directory, just:go build (This won't produce an output file. To do that, you must use go install, which places the package object inside the pkg directory of the workspace.)

Whenever the go tool installs a package or binary, it also installs whatever dependencies it has. So when you install the hello program, the stringutil package will be installed as well, automatically.
