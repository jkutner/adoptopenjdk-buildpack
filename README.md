# AdoptOpenJDK Buildpack

This [buildpack](https://devcenter.heroku.com/articles/buildpacks) will install the [AdoptOpenJDK](https://adoptopenjdk.net/) Community Edition.

## Usage

This buildpack can be used with the [Heroku Java buildpack](https://github.com/heroku/heroku-buildpack-java/blob/master/bin/compile) to replace the default JDK by running:

```
$ heroku buildpacks:set jdk/adoptopenjdk
$ heroku buildpacks:add heroku/java
```

## Customizing

You can customize the version of AdoptOpenJDK by setting the `ADOPTOPENJDK_URL` and `ADOPTOPENJDK_CHECKSUM` config variables thusly:

```
$ heroku config:set ADOPTOPENJDK_URL="https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.2%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.2_9.tar.gz"
$ heroku config:set ADOPTOPENJDK_CHECKSUM="d02089d834f7702ac1a9776d8d0d13ee174d0656cf036c6b68b9ffb71a6f610e"
```

The URLs and checksums can be obtained from the [AdoptOpenJDK archive](https://adoptopenjdk.net/archive.html).

## License

MIT
