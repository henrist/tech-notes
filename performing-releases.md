# Performing releases

## Java / Maven

Using Maven Release Plugin.

When including sources, there is a bug in Maven that causes the sources to be uploaded twice. A workaround seems to be to disable the release profile. See [https://stackoverflow.com/a/13276206](https://stackoverflow.com/a/13276206) for some more context.

```text
mvn release:prepare release:perform -DuseReleaseProfile=false
```

The command will ask for the version to release and what will be the next snapshot. It needs push access to the Git repo and credentials to the Maven repo available in ~/.m2/settings.xml.

