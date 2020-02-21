# youkol-parent
youkol-parent is the youkol parent POM which has to be inherited by all youkol modules.

### 1. Config your maven setting.xml
```xml
<servers>
    ...
    <server>
        <id>ossrh</id>
        <username>[username]</username>
        <password>[password]</password>
    </server>
    ...
</servers>
```

### 2. Commands
```shell
# Cleaning a Maven project.
$ mvn clean

# Compile the source code of the project
$ mvn clean compile

# Take the compiled code and package it in its distributable format, such as a JAR.
$ mvn clean package

# Install the built artifact into the local repository.
# If license.txt exist, add at the top of your source files a license
$ mvn clean install
$ mvn clean install -Plicense
$ mvn clean install -Prelease

# Deploy the built artifact to the remote repository.
$ mvn clean deploy -Prelease

# Release the current project - updating the POM and tagging in the SCM.
# Prepare for a release in SCM.
$ mvn release:prepare
# Perform a release from SCM, either from a specified tag, 
# or the tag representing the previous release in the working copy created by release:prepare. 
$ mvn release:perform
# Rollback changes made by a previous release. 
$ mvn release:rollback
```

### 3. About author
- Site: https://www.youkol.com
- Issuse: https://github.com/youkol/youkol-parent/issues