[![Build Status](https://travis-ci.org/fulcrumgenomics/fgbio.svg?branch=master)](https://travis-ci.org/fulcrumgenomics/fgbio)
[![codecov](https://codecov.io/gh/fulcrumgenomics/fgbio/branch/master/graph/badge.svg)](https://codecov.io/gh/fulcrumgenomics/fgbio)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/fc4f5fe8dbe34bf784114435b202fab4)](https://www.codacy.com/app/contact_32/fgbio?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=fulcrumgenomics/fgbio&amp;utm_campaign=Badge_Grade)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.fulcrumgenomics/fgbio_2.11/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.fulcrumgenomics/fgbio_2.11)
[![Dependency Status](https://www.versioneye.com/user/projects/57a1584c3d8eb6002dc1e812/badge.svg)](https://www.versioneye.com/user/projects/57a1584c3d8eb6002dc1e812#dialog_dependency_badge) 
[![License](http://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/fulcrumgenomics/fgbio/blob/master/LICENSE)
[![Language](http://img.shields.io/badge/language-scala-brightgreen.svg)](http://www.scala-lang.org/)

# fgbio

fgbio is a command line toolkit for working with genomic and particularly next generation sequencing data.

## Getting Started

Releases of fgbio are available from the [GitHub Releases](https://github.com/fulcrumgenomics/fgbio/releases) page for the project.  Start by downloading the `.jar` file for the latest release.

To run fgbio you will need [Java 8](https://java.com/en/download/) (aka Java 1.8) or later installed.  To see the version of Java currently installed run the following in a terminal:

```
java -version
```

If the reported version on the first line starts with `1.8` or higher, you are all set.

Once you have Java installed and a release downloaded you can run:

* Run `java -jar fgbio-0.1.4.jar` to get a list of avaiable tools
* Run `java -jar fgbio-0.1.4.jar <Tool Name>` to see detailed usage instructions on any tool

When running tools we recommend the following set of Java options as a starting point though individual tools may need more or less memory depending on the input data:

```
java -Xmx4g -XX:+AggressiveOpts -XX:+AggressiveHeap -jar fgbio.jar ...
```

To save typing this every time you may wish to setup a shell alias, for example:

```
alias fgbio="java -Xmx4g -XX:+AggressiveOpts -XX:+AggressiveHeap -jar /path/to/fgbio.jar
```

## Documentation

Each tool has detailed uage and argument documentation that can be viewed at the command line by running the tool in question with no arguments.

[Online Documentation](tools/latest) of all the tools is also available.

For developers, API documentation is available through [javadoc.io](http://www.javadoc.io/doc/com.fulcrumgenomics/fgbio_2.12).

## Getting Help

The primary mechanism for getting help is to log an issue on the project's [GitHub Issues](https://github.com/fulcrumgenomics/fgbio/issues) page.

### Before Logging An Issue

* Make sure you are running the latest release of fgbio
* Search both open and closed issues for similar problems
* Ensure that your input files are valid (for BAM files we kindly request you run [Picard's ValidateSamFile](https://broadinstitute.github.io/picard/command-line-overview.html#ValidateSamFile) before logging issues)

### When Logging An Issue

If requesting help with a tool that is failing or producing undesirable results, please include:

* The full command line used to invoke the tool
* The terminal output produced by the tool while running
* Information on the operating system you are running, using `uname -a`
* Information on the version of Java you are running, using `java -version`

## License

`fgbio` is open source software released under the [MIT License](https://github.com/fulcrumgenomics/fgbio/blob/master/LICENSE).
