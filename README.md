# Elasticsearch analysis seunjeon

[seunjeon](https://bitbucket.org/eunjeon/seunjeon/src/master/elasticsearch/) is a plugin to user Korean morpheme anylyzer for Elasticsearch.

This repo does not add any new features to the seunjeon plugin itself. It is just a rebuild of the analyzer so that it is compatible with Elasticsearch version > 6.1.0.

# Limit of this rebuild

The current rebuild works well with ES version 7.8. The rebuild will fail if any plugin dependencies introduce broken changes. `build.sbt` file inside the plug-in repository will need manual modifications to suit the changes.

# Implementation

see [rebuild steps](rebuild.md)