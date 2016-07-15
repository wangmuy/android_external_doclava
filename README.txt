based on aosp tag android-5.1.1_r6

To generate an api list of public classes and interfaces:

javadoc \
-encoding UTF-8 \
`cat list-of-src-files` \
-J-Xmx1280m \
-XDignore.symbol.file \
-quiet \
-doclet com.google.doclava.Doclava \
-docletpath libs/jsilver.jar:build/libs/doclava.jar \
-bootclasspath core-libart.jar \
-classpath <src-needed-classpath> \
-sourcepath <src-dir>:<classpath-dir> \
-d build/docs \
-public \
-stubs <stubbed-src-dir> \
-api <generated-api-file> \
-removedApi <generated-removed-api-file> \
-skippackages java \
-keeponlypackages com.example.mypackage \
-nodocs