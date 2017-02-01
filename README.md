# SWBBundle
git master repository to clone and build all SWB Packages and dependencies

To clone this repo use:

```sh
git clone --recursive https://github.com/SemanticWebBuilder/SWBBundle.git
```

All submodules will be checked out in **detached HEAD** state. To attach all submodules to a branch just type:

```sh
git submodule foreach 'git checkout <branchname>'
```

Where _&lt;branchname>_ stands for the name of the branch to checkout.

## Build SWB application
Project's POM contains several profiles to build SWB. If you want to build SWB using the default profile just type:

```sh
cd SWBBundle
mvn package
```

This profile uses [jitpack](https://jitpack.io/) to resolve dependencies based on master branch for each submodule.

If you want to build SWB using local checked out code just type:

```sh
cd SWBBundle
mvn package -Dlocal=true
```

If you want to build SWB using a branch tag on each submodule (tag must exist in each repository) just type:

```sh
cd SWBBundle
mvn package -Dbranchtag=<tagname>
```

Where _&lt;tagname>_ stands for the name of the branch to use. This profile uses [jitpack](https://jitpack.io/) to resolve dependencies.

Whatever option you choose, the application's WAR will be generated in folder **SWB/target**.

We'll try to have submodules always to head, but it might get behind

To update to head commit:

```sh
git submodule update --remote
```
