findbugs-2.0.2
==============

Refactor build to use Maven instead of ANT


TODO
----

1. Remove IDE project files
1. Create Master POM
1. Create Modules POMs (leave source where it currently is located).
1. Remove jar files
1. Move Source code to correct modules and directory structure.
1. Remove ANT Build files
1. Ensure apple dependency is not packaged
1. Re-write history to eliminate repository-bloat from binary aftifacts
1. Get jsr305.jar into central repository
1. get updated bcel as a separate module and deployed to central repository (i.e. findbugs-bcel-5.1.jar)
1. Get jFormatString setup as a standalone project or module to deploy to Central repository.

 

[Sonatype OSS Maven Repository Usage Guide](https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide)

Research from TattleTale(http://gleclaire.github.com/findbugs-2.0.2/tattletale-findbugs/index.html)
------------------------

1. jsr305.jar, annotations.jar, and jcip-annotations.jar all get merged into annotations.jar
This is messy and the resulting artifact should be a different name like findbugs-annotations.jar
1. annotations.jar and findbugs.jar both contain the package  edu.umd.cs.findbugs.annotations.*  The package should be removed from on of the jars.
1. findbugs-ant.jar and findbugs.jar both contain the edu.umd.cs.findbugs.anttask.* package. It looks like there is not a need to create the findbugs-ant.jar artifact anymore.
1. Some of the test have a hard file reference which need to be changed to remove coupling to a file system

Unused Jar
-----------
1. asm-xml-3.3.jar
1. findbugs-ant.jar
1. yjp-controller-api-redist.jar



