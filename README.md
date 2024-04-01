# Jobcacher Artifactory storage Extension plugin

![Build](https://ci.jenkins.io/job/Plugins/job/jobcacher-artifactory-storage-plugin/job/main/badge/icon)
[![Coverage](https://ci.jenkins.io/job/Plugins/job/jobcacher-artifactory-storage-plugin/job/main/badge/icon?status=${instructionCoverage}&subject=coverage&color=${colorInstructionCoverage})](https://ci.jenkins.io/job/Plugins/job/jobcacher-artifactory-storage-plugin/job/main)
[![LOC](https://ci.jenkins.io/job/Plugins/job/jobcacher-artifactory-storage-plugin/job/main/badge/icon?job=test&status=${lineOfCode}&subject=line%20of%20code&color=blue)](https://ci.jenkins.io/job/Plugins/job/jobcacher-artifactory-storage-plugin/job/main)
![Contributors](https://img.shields.io/github/contributors/jenkinsci/jobcacher-artifactory-storage-plugin.svg?color=blue)
[![GitHub release](https://img.shields.io/github/release/jenkinsci/jobcacher-artifactory-storage-plugin.svg?label=changelog)](https://github.com/jenkinsci/jobcacher-artifactory-storage-plugin/releases/latest)
[![GitHub license](https://img.shields.io/github/license/jenkinsci/jobcacher-artifactory-storage-plugin)](https://github.com/jenkinsci/jobcacher-artifactory-storage-plugin/blob/main/LICENSE.md)

This plugin is an extension of the [jobcacher-plugin](https://plugins.jenkins.io/jobcacher/) that allows you to store the caches in JFrog Artifactory generic repository.

> [!NOTE]
> This plugin is maintained by the Jenkins Community and not by JFrog.

<p align="center">
  <img src="docs/artifactory_logo.png">
</p>

The plugin support both OSS and Pro versions of Artifactory, but Pro version is recommended due to missing REST API on OSS edition.

> [!IMPORTANT]
> Limitations of OSS edition.

- Not able to move caches to another location when a job is renamed. Moving must be done manually from Artifactory UI (which is supported on OSS edition).

## Introduction

## Getting started

You only need to configure the extension to use Artifactory under System Configuration.

![](docs/artifactory_config.png)

## Configuration as Code

```yaml
unclassified:
  globalItemStorage:
    storage:
      artifactory:
        prefix: "jenkins/"
        repository: "my-generic-repo"
        serverUrl: "http://localhost:7000"
        storageCredentialId: "the-credentials-id"
```

Caches will be stored artifactory with the following structure:

![](docs/artifactory_caches.png)

See [jobcacher-plugin](https://plugins.jenkins.io/jobcacher/) for usage in jobs and pipelines.

## CONTRIBUTING

See [CONTRIBUTING](CONTRIBUTING.md)

## LICENSE

Licensed under MIT, see [LICENSE](LICENSE.md)

