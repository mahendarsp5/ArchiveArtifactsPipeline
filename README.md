# ArchiveArtifactsPipeline
  When there are test failures, it is often useful to grab built artifacts from Jenkins for local analysis and investigation. This is made practical by Jenkins’s built-in support for storing "artifacts", files generated during the execution of the Pipeline.  This is easily done with the archiveArtifacts step and a file-globbing expression, as is demonstrated in the example:
  
  If more than one parameter is specified in the archiveArtifacts step, then each parameter’s name must explicitly be specified in the step code - i.e. artifacts for the artifact’s path and file name and fingerprint to choose this option. If you only need to specify the artifacts' path and file name/s, then you can omit the parameter name artifacts - e.g.
archiveArtifacts 'build/libs/**/*.jar'
