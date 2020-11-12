# NAME

example/file - example of a beakerlib library

# DESCRIPTION

This is a trivial example of a BeakerLib library. It's main goal
is to provide a minimal template which can be used as a skeleton
when creating a new library. It implements function fileCreate().
Please note, that all library functions must begin with the same
prefix which is defined at the beginning of the library.

# VARIABLES

Below is the list of global variables. When writing a new library,
please make sure that all global variables start with the library
prefix to prevent collisions with other libraries.

- fileFILENAME

    Default file name to be used when no provided ('foo').

# FUNCTIONS

## fileCreate

Create a new file, name it accordingly and make sure (assert) that
the file is successfully created.

    fileCreate [filename]

- filename

    Name for the newly created file. Optionally the filename can be
    provided in the FILENAME environment variable. When no file name
    is given 'foo' is used by default.

Returns 0 when the file is successfully created, non-zero otherwise.

# EXECUTION

This library supports direct execution. When run as a task, phases
provided in the PHASE environment variable will be executed.
Supported phases are:

- Create

    Create a new empty file. Use FILENAME to provide the desired file
    name. By default 'foo' is created in the current directory.

- Test

    Run the self test suite.

# AUTHORS

- Petr Splichal <psplicha@redhat.com>
