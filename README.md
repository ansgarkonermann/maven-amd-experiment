maven-amd-experiment
====================

Experimental Maven multi-module project illustrating limitations of `mvn -amd` command line switch.

Run

    mvn clean verify -amd -pl dependency-management

Expected outcome: `dependency-management` gets build, then `java-librar` and `gui` (since both import
`dependency-management`).

Actual outcome: only `dependency-management` gets build.

