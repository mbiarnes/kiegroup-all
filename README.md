# kiegroup-all

This project aggregates relevant kiegroup repositories into one big multi-module maven project
to enable building and managing repositories from one central place.

## Compile everything

```bash
git submodule init

git submodule update --remote

MAVEN_OPTS="-Xmx8G" \
mvn clean install \
--errors \
--batch-mode \
--fail-at-end \
-T1C \
-DskipTests \
-Dgwt.compiler.skip=true \
-Dgwt.skipCompilation=true \
-Denforcer.skip=true \
-Dcheckstyle.skip=true \
-Dfindbugs.skip=true \
-Drevapi.skip=true
```
