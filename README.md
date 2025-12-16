To reproduce:

`./.gradle`


```
Isolated projects is an incubating feature.
Calculating task graph as no cached configuration is available for tasks: 

> Task :help

Welcome to Gradle 9.2.0.

To run a build, run gradlew <task> ...

To see a list of available tasks, run gradlew tasks

To see more detail about a task, run gradlew help --task <task>

To see a list of command-line options, run gradlew --help

For more detail on using Gradle, see https://docs.gradle.org/9.2.0/userguide/command_line_interface.html

For troubleshooting, visit https://help.gradle.org

[Incubating] Problems report is available at: file:///Users/rafael/sources/repros/duplicated-problems/build/reports/problems/problems-report.html

FAILURE: Build failed with an exception.

* Where:
Build file '/Users/rafael/sources/repros/duplicated-problems/child/build.gradle' line: 2

* What went wrong:
Configuration cache problems found in this build.

5000 problems were found storing the configuration cache, only the first 4096 were considered, 1 of which seems unique.
- Build file 'child/build.gradle': line 2: Project ':child' cannot dynamically look up a property in the parent project ':'

See the complete report at file:///Users/rafael/sources/repros/duplicated-problems/build/reports/configuration-cache/3xwrxnd5eps05xji7wwu1q61d/3qbqxso2hbs5yrli2axfbcghm/configuration-cache-report.html
> Project ':child' cannot dynamically look up a property in the parent project ':'

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to generate a Build Scan (powered by Develocity).
> Get more help at https://help.gradle.org.

BUILD FAILED in 1s
1 actionable task: 1 executed
Configuration cache entry discarded with 5000 problems.
```
