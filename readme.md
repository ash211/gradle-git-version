Git-Version Gradle Plugin
=========================
[![Build Status](https://circleci.com/gh/palantir/gradle-git-version.svg?style=shield)](https://circleci.com/gh/palantir/gradle-git-version)
[![Gradle Plugins Release](https://img.shields.io/github/release/palantir/gradle-git-version.svg)](https://plugins.gradle.org/plugin/com.palantir.git-version)

When applied, Git-Version adds a method to the target project called `gitVersion()` that
runs the JGit equivalent of `git describe` to determine a version string. It behaves exactly 
as the JGit `git describe` method behaves, except that when the repository is in a dirty 
state, appends `.dirty` to the version string.

Usage
-----
Apply the plugin using standard Gradle convention:

    plugins {
        id 'com.palantir.git-version' version '<current version>'
    }

Set the version of a project by calling:

    version gitVersion()

Tasks
-----
This plugin adds a `printVersion` task, which will echo the project's configured version
to standard-out.

License
-------
This plugin is made available under the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0).
