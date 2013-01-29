findbugs-2.0.2
==============

Refactor build to use Maven instead of ANT


TODO
----

1. <del>Remove IDE project files</del>
1. <del>Create Master POM</del>
1. Create Modules POMs (leave source where it currently is located). <b>...In Progress</b>
1. Remove jar files that are in the Central repository. <b>...In Progress</b>
1. Get jsr305.jar into central repository
1. Get jFormatString setup as a standalone project or module to deploy to Central repository.
1. Get updated bcel as a separate module and deployed to central repository (i.e. findbugs-bcel-5.1.jar)
1. Remove unused jar files. <b>...In Progress</b>
1. Remove ANT Build files
1. Move Source code to correct modules and directory structure. <b>...In Progress</b>
1. Combine findbugs-ant.jar into findbugs.jar and update scripts and documentation to reflect changes.
1. Create Eclipse plugin Maven POMs using Tycho. <b>...In Progress</b>
1. Update Findbugs AntTask to use classpath setting instead of findbugs home setting.
1. Create findbugs AntTask tests.
1. Create findbugs scripts tests.
1. Create Maven module to generate site.


 

[Sonatype OSS Maven Repository Usage Guide](https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide)
[Sonatype Tycho Maven Plugin](http://www.sonatype.org/tycho/)



[Research from TattleTale](http://gleclaire.github.com/findbugs-2.0.2/tattle-findbugs/index.html)
------------------------

1. jsr305.jar, annotations.jar, and jcip-annotations.jar all get merged into annotations.jar
This is messy and the resulting artifact should be a different name like findbugs-annotations.jar
1. annotations.jar and findbugs.jar both contain the package  edu.umd.cs.findbugs.annotations.*  The package should be removed from on of the jars.
1. findbugs-ant.jar and findbugs.jar both contain the edu.umd.cs.findbugs.anttask.* package. It looks like there is not a need to create the findbugs-ant.jar artifact anymore.
1. Some of the test have a hard file reference which need to be changed to remove coupling to a file system.
1. findbug anttask uses a start up that depends on a set directory structure and file names for the dependency jar.  This does not allow for classes being on classpath not does it allow for versioned dependencies without changing source code (i.e. commons-lang-2.4.jar vs commons-lang-2.5.jar). 

Unused Jar
-----------
1. asm-xml-3.3.jar
1. findbugs-ant.jar
1. yjp-controller-api-redist.jar



