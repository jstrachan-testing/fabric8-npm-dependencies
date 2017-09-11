#!/usr/bin/groovy
@Library('github.com/fabric8io/fabric8-pipeline-library@master')
def utils = new io.fabric8.Utils()
if (utils.isCI()){
  echo 'no CI enabled'
} else if (utils.isCD()){
  clientsNode {
    ws {
      checkout scm
      npmUpdateOrganisationDependencies{
        organisation = 'fabric8-ui'
      }
    }
  }
}

