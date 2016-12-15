# SWBBundle
git master repository to clone and build all SWB Packages and dependencies

To clone this repo use:

```git clone --recursive https://github.com/SemanticWebBuilder/SWBBundle.git```

To  build use:

```
cd SWBBundle
mvn package
```

we'll try to have submodules allways to head, but it migth get behind
To update to head commit:

```
git submodule update --remote
```
