Use this README to rebuild the plugin according to your ES version.

# Install sbt
```
brew install sbt
```

cd under the original repo elasticsearch for the following steps

# git clone the original repo
```
git clone https://bitbucket.org/eunjeon/seunjeon/src/master/elasticsearch/
```

# Download the dictionary
```
./scripts/download-dict.sh mecab-ko-dic-2.0.1-20150920
```

# Modify the file build.sbt to work it with your ES version 

```
sed 's/\$es_version_for_rebuild/"your_es_version"/' ~/elasticsearch-analysis-seunjeon/seunjeon-patch.diff | git apply
```

# Build the dictionary
```
sbt -J-Xmx2G "runMain org.bitbucket.eunjeon.seunjeon.DictBuilder"
```

This step might fail if your es version does not work with certain types or dependencies of the plugin. You may need to manually change certain parts in the plug in code to make the build pass. See [Limit of this rebuild](README.md)
# Build es plugin
```
sbt elasticsearch/esZip 
```

In your Elasticsearch cluster
# Install plugin in Elasticsearch
```
bin/elasticsearch-plugin install file:///elasticsearch/target/elasticsearch-analysis-seunjeon-assembly-7.1.1.1.zip
```