#First Go software:
echo $GOPATH #to see if it’s set or empty<br>
export GOPATH=$HOME/Web/Go/src/github.com/username/helloUsingLibrary<br>
echo $GOPATH # to see it has changed<br>
mkdir -p $GOPATH/src/hello<br>
cd !$ # cd ~/Web/Go/src/github.com/username/helloUsingLibrary/src/hello<br>
echo $PATH<br>
export PATH=$PATH:$GOPATH/bin<br>
echo $PATH # to see it has changed<br>
vim hello.go # You can create hello.go<br>

# First Go library:
mkdir $GOPATH/src/github.com/username/stringutil #in that folder, create reverse.go<br>

go build github.com/username/helloUsingLibrary/stringutil #Or, in the package's source directory, just:go build (This won't produce an output file. To do that, you must use go install, which places the package object inside the pkg directory of the workspace.)<br>

Whenever the go tool installs a package or binary, it also installs whatever dependencies it has. So when you install the hello program, the stringutil package will be installed as well, automatically.<br>

# Run the application
go install hello.go<br>
$GOPATH/bin/hello # to run hello.go or « hello » because $GOPATH/bin is now in the PATH<br>
