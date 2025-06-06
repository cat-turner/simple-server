Hello, World
============

A simple program, and an example of how to structure a python project. Demonstrates a basic package
file structure (using [flat layout]) and a way to define a [single package version] shared between
package metadata and program runtime.

See also: the Python Packaging User Guide at https://packaging.python.org/ offers more complete
examples and explanations.

[flat layout]: https://packaging.python.org/en/latest/discussions/src-layout-vs-flat-layout/
[single package version]: https://packaging.python.org/en/latest/guides/single-sourcing-package-version/

Basic usage
-----------

To start the server using Docker, run the following commands:

```shell
$ docker build -t simple-server .
$ docker run -p 8000:8000 simple-server
```

The server will be available at http://localhost:8000

Submitting to ShapesWorld
------------------------

To submit to ShapesWorld, you need to create a zip file containing your project files. Use the following command to create a flat zip file (without creating a subdirectory):

```shell
$ zip -r submission.zip . -x ".*" -x "__pycache__/*" -x "*.pyc"
```

This command:
- Creates a zip file named `submission.zip`
- Includes all files in the current directory (`.`)
- Excludes hidden files and directories (`-x ".*"`)
- Excludes Python cache files (`-x "__pycache__/*" -x "*.pyc"`)
- Creates a flat structure (files appear at the root of the zip, not in a subdirectory)
