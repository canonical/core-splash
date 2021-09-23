# Introduction

This projects contains a snap recipe that builds the `core-splash`
snap. This snap contains the bits needed by a base snap to support
splash screens on boot and shutdown/reboot. To add the functionality,
the `core-splash` snap needs to be staged from the base snap recipe.

The snap contains `plymouth`, its dependencies, and different
configuration files. `plymouth` is built from scratch, being the main
reason for that the desire to compile statically most of its
dependencies to reduce the final size and to avoid exposing too many
non-fundamental libraries in the base snap. Also, it turns out that
static libraries are not available for `libpango`, so this library is
also built from scratch to get them.

# Build

Run

```
$ snapcraft
```

or

```
$ snapcraft --use-lxd
```

as preferred.
