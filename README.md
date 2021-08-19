# gomod-with-subpackage

Go repository with a root package and an independent non-root package. Intended for
testing how Cachito presents non-root Go packages in request metadata.

Note that the root package does not import `some-package`. This is important. Otherwise,
Cachito would identify `some-package` as a dependency of the root package and would
*not* list it as an independent package.
