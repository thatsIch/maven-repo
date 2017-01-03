# Maven

## Install Library

Tutorial from http://kwebble.com/blog/2014/02/19/use-github-to-host-your-own-maven-repo

Full documentation of the `install` plugin with the `install-file` target http://maven.apache.org/plugins/maven-install-plugin/install-file-mojo.html

```
mvn install:install-file
 -DgroupId=[group-id]
 -DartifactId=[artifact-id]
 -Dversion=[version]
 -Dpackaging=[packaging-format]
 -Dfile=[path-to-file]
 -DlocalRepositoryPath=[path-to-git-repo]
```

where `group-id` is generally the namespace of the user on Github,
`artifact-id` the resulting artifact name or repository name on Github,
`version` the build number of the artifact,
`packaging-format` if it is a `jar`, `war`, etc.
`path-to-file` in Maven generally a `jar` in the `target/` folder,
`path-to-git-repo` the local git repository you install it into

## Setup Repository
```maven
<project>
    ...
    <repositories>
        ...
        <repository>
            <id>git-thatsIch</id>
            <name>thatsIch's Git based repo</name>
            <url>https://github.com/thatsIch/maven-repo/raw/master/</url>
        </repository>
        ...
    </repositories>
    ...
</project>
```

## Library Listing

* `ddf:minim:2.2.2` A Java audio library, designed to be used with Processing.
* `nok:soundcloud-java-library:0.2.1` Unofficial Java library, which simplifies the use of the official SoundCloud Java API wrapper.
* `eustas:CafeUndZopfli:1.0.0` GZip compatible compressor.
