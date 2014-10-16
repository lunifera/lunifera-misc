
org.lunifera.ide.tools.export.bundles can be used to export all bundles.
Bundles are separated in 3 categories:
- common - used for runtime and IDE
- runtime - should never be installed into IDE. Bundles for runtime server
- IDE - bundles required to startup the IDE properly

To address a category, just use its profile.

Profiles:
- lunifera-common for common bundles
- lunifera-runtime for runtime bundles
- lunifera-ide for IDE bundles

Call 
``` mvn clean verify -Plunifera-common -Dclassifier=sources ```
to download all common source bundles

Call
``` mvn clean verify -Plunifera-common ```
to download all common jar files

You also may combine profiles:
``` mvn clean verify -Plunifera-common, lunifera-runtime, lunifera-ide ```
to download bundles of different categories at once.

