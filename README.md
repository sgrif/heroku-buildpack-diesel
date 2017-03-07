This is a heroku buildpack for Rust applications built using Diesel. It simply
installs Diesel CLI as part of the build phase. The resulting binary will be in
a folder called `bin` in the root of your project.

The binary will be built with PostgreSQL support only.

Specifying Diesel Versions
--------------------------

If you need to specify a specific version of Diesel CLI, you can do so by adding
a file called `.diesel_version` to the root of your project, which contains
exactly the version string you want to use. For example

```
0.11.0
```

If this file is not present, the latest version will be installed. The version
of Diesel CLI used does not need to match the version of Diesel used by your
application, as Diesel CLI is generally backwards compatible.
