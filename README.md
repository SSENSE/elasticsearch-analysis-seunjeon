# Elasticsearch analysis seunjeon

[seunjeon](https://bitbucket.org/eunjeon/seunjeon/src/master/elasticsearch/) is a plugin to user Korean morpheme anylyzer for Elasticsearch.

This repo does not add any new features to the seunjeon plugin itself. It is just a rebuild of the analyzer so that it is compatible with Elasticsearch version > 6.1.0.

## Limit of this rebuild

The current rebuild provides two patch files, working with ES version 7.8.1 or 7.1.1. 

The rebuild will fail if any plugin dependencies are not compatible with Elasticsearch you choose. In this case, the `build.sbt` file inside the plug-in repository will need manual modifications to suit the changes. And you are very welcome make a diff patch file and add into this repo.

## Implementation

see [rebuild steps](rebuild.md)

## Authors
- [**Marshall Scorcio**](https://github.com/marshalium)
- [**Matty Wang**](https://github.com/MattyChance)

## License

This project is licensed under the Apache License, Version 2.0 - see the [LICENSE.md](LICENSE.md) file for details.
