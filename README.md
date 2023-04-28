# ox64-manifests

## Prerequisites

Install the [repo](https://gerrit.googlesource.com/git-repo) tool

````shell
# assuming ~/.local/bin/ exists and is on your path
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.local/bin/repo
chmod a+rx ~/.local/bin/repo
``````

## Usage

Create a directory and cd into it. Next use the repo tool to fetch all required sources

````shell
mkdir ox64
cd ox64
repo init -u git@github.com:KorribanMaster/ox64-manifests.git -b main -m manifests/experimental/ox64.xml
repo sync
``````
## Build the image

````shell
source experimental-init-env
MACHINE=ox64 bitbake core-image-sato
``````
