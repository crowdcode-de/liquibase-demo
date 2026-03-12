# Liquibase Demonstration

This is the repository containing the sources of my talk "Datenbankkatastrophen vermeiden mit Liquibase"

# Build

All you need is maven. Or IntelliJ. Use the Profile "with-local-postgres" oer "with-file-h2" to start

## Demo Plugin required

By default the pluign is enabled, you can find it here: https://github.com/crowdcode-de/liquibase-demo-plugin


## Embedded Execution

Start the application with the profile "with-local-postgres" or "with-file-h2".

## Command Line Execution


```
liquibase \
--search-path=src/main/resources/ \
update \
--changelog-file=db/changelog/changelog-master.xml \
--url="jdbc:postgresql://localhost:5432/postgres" \
--username=postgres \
--password=postgres      
```

## Maven Execution

```
mvn clean liquibase:update -Prun-liquibase
```