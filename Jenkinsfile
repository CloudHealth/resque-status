#!/usr/bin/env groovy
@Library('cht-jenkins-pipeline@vk/CLHC-220243') _

properties([
    [$class: 'BuildDiscarderProperty', strategy: [$class: 'LogRotator', artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '15']]
]);

def gemHooks = [versionFilePath: 'resque-status.gemspec']

// NODE FOR RUBY2.5.5-RAILS3.2
node('management-testing') {
    stgGemPublish(gemHooks) // Added for Gem build & publish
}
