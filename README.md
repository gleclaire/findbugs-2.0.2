findbugs-2.0.2
==============

Refactor build to use Maven instead of ANT


TODO
----

1. Remove IDE project files
2. Create Master POM
3. Create Modules POMs (leave source where it currently is located).
4. Remove jar files
5. Move Source code to correct modules and directory structure.
6. Remove ANT Build files
7. Ensure apple dependency is not packaged
8. Re-write history to eliminate repository-bloat from binary aftifacts


[Sonatype OSS Maven Repository Usage Guide](https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide)

Research from TattleTale
------------------------

1. jsr305.jar, annotations.jar, and jcip-annotations.jar all get merged into annotations.jar
This is messy and the resulting artifact should be a different name like findbugs-annotations.jar
1. annotations.jar and findbugs.jar both contain the package  edu.umd.cs.findbugs.annotations.*  The package should be removed from on of the jars.
1. findbugs-ant.jar and findbugs.jar both contain the edu.umd.cs.findbugs.anttask.* package. It looks like there is not a need to create the findbugs-ant.jar artifact anymore.


Unused Jar
-----------
1. asm-xml-3.3.jar
1. findbugs-ant.jar
1. jdepend-2.9.jar
1. yjp-controller-api-redist.jar



