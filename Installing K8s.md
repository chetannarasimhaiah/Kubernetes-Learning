
Command to install k8s

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl"

=============

Validate the binary (optional)

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl.sha256"

===============


Validate the kubectl binary against the checksum file:

echo "$(<kubectl.sha256)  kubectl" | shasum -a 256 --check

================


If valid, the output is:

kubectl: OK

==================


Make the kubectl binary executable.

chmod +x ./kubectl

=================

Move the kubectl binary to a file location on your system PATH.

sudo mv ./kubectl /usr/local/bin/kubectl
sudo chown root: /usr/local/bin/kubectl

================

Check Version

kubectl version --client
Client Version: version.Info{Major:"1", Minor:"21", GitVersion:"v1.21.2", GitCommit:"092fbfbf53427de67cac1e9fa54aaa09a28371d7", GitTreeState:"clean", BuildDate:"2021-06-16T12:59:11Z", GoVersion:"go1.16.5", Compiler:"gc", Platform:"darwin/amd64"}

=================


OR INSTALLING
Install with Homebrew on macOS

brew install kubectl 
