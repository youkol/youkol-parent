# youkol-parent
youkol-parent is the youkol parent POM which has to be inherited by all youkol modules.

### config your maven setting.xml
```
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

### commands
```shell
$ mvn clean

$ mvn clean compile

$ mvn clean package

$ mvn clean install
$ mvn clean install -Plicense

$ mvn clean deploy -Prelease

$ mvn release:prepare
$ mvn release:perform
$ mvn release:rollback
```