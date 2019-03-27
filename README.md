# AdoptOpenJDK Buildpack

This [buildpack](https://devcenter.heroku.com/articles/buildpacks) will install the [AdoptOpenJDK](https://adoptopenjdk.net/) runtimes.

## Usage

This buildpack can be used with the [Heroku Java buildpack](https://github.com/heroku/heroku-buildpack-java/blob/master/bin/compile) to replace the default JDK by running:

```
$ heroku buildpacks:set jdk/adoptopenjdk
$ heroku buildpacks:add heroku/java
```

## Customizing

You can customize the version of AdoptOpenJDK by setting the following config vars:

* `ADOPTOPENJDK_VERSION` (default: 8)
* `ADOPTOPENJDK_IMPL` (default: hotspot)
* `ADOPTOPENJDK_RELEASE` (default: latest)
* `ADOPTOPENJDK_CHECKSUM` (no default)

Alternatively, you can codify these in your app by creating a `system.properties` file with contents like this:

```
adoptopenjdk.version=8
adoptopenjdk.impl=hotspot
adoptopenjdk.release=latest
```
For more information on acceptable values, see the [AdoptOpenJDK API docs](https://api.adoptopenjdk.net/).

## License

MIT
