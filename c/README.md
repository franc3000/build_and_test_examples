C, CUnit and Make
=================

Prerequisites
-------------

**gcc**:

To check if it is installed already:

    $ gcc -v
    gcc version 4.4.7 20120313 (Red Hat 4.4.7-3) (GCC) 

**CUnit 2.1-2**:

To download, build and install see [CUnit](http://cunit.sourceforge.net/).

After installing ensure that the `bin`, `include` and `lib`
directories holding the CUnit files are in your paths e.g.

    $ export C_INCLUDE_PATH=/home/user/bin/include:$C_INCLUDE_PATH
    $ export LIBRARY_PATH=/home/user/bin/lib:$LIBRARY_PATH
    $ export LD_LIBRARY_PATH=/home/user/bin/lib:$LD_LIBRARY_PATH

**xsltproc**:

To check if it is installed already:

    $ xsltproc -version
    Using libxml 20706, libxslt 10126 and libexslt 815
    xsltproc was compiled against libxml 20706, libxslt 10126 and libexslt 815
    libxslt 10126 was compiled against libxml 20706
    libexslt 815 was compiled against libxml 20706

**CUnit to JUnit XSL transform**:

This is provided.

* Files: `cunit-to-junit.xsl`.
* Version: Unspecified.
* Licence: Unspecified. Written by Oliver van Porten.
* Web site: http://www.van-porten.de/2009/05/cunit-tests-in-hudson/. 
* Web site: https://bitbucket.org/mcdeck/cunit-to-junit

Usage
-----

Compile:

    $ make fibonacci

Run:

    $ ./fibonacci 30

Compile tests:

    $ make tests

Run tests:

    $ ./tests

View results as XML:

    $ CUnitAutomated-Results.xml 

Make and view an xUnit-style test report:

    $ make report
    $ cat Test-Results.xml

Clean up:

    $ make clean