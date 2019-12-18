# CoreMedia Content Cloud App Stub Preparation

The script in this repository can be used to add new custom apps to your 
CoreMedia Content Cloud Blueprints Workspace.

## Status and Feedback

This is just a starting point. Please contribute or give [feedback][issues] via 
the usual [github][github] means.

## Usage

```
./app-create.sh TARGET-DIRECTORY APP-NAME
```

The target directory might be the pre-existing directory suitable for the new
app with the given name, or the apps directory or even the root directory of
your CoreMedia Content Cloud 10 Workspace.

If the app's directory does not exist, it gets created.

## Function

The script creates the following basic sub folder structure with maven poms 
and a Dockerfile for an app inside of the CoreMedia Content Cloud 10 Blueprints
Workspace:

```    
pom.xml
├── blueprint-parent
│   └── pom.xml
├── docker
│   ├── APP_NAME-app
│   │   ├── Dockerfile
│   │   └── pom.xml
│   └── pom.xml
├── APP_NAME-blueprint-bom
│   └── pom.xml
├── modules
│   └── pom.xml
└── spring-boot
    ├── APP_NAME-app (with scr/main/[java|resources] boilerplates 
    │   └── pom.xml
    └── pom.xml
```

The [base workspace itself is available in from CoreMedia][coremedia-blueprints]. 
Please consult the [Product Homepage][coremedia].

[coremedia]: https://www.coremedia.com/
[coremedia-blueprints]: https://github.com/coremedia-contributions/coremedia-blueprints-workspace/tree/cmcc-10-1907
[issues]: https://github.com/blackappsolutions/cmccAppCreator/issues
[github]: https://github.com/
