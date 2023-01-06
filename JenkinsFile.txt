pipeline{
    post{
        success{
            script{
                /* def sourceFile = "release-pipeline/project/dist/myFile.js"

                if (fileExists(file: sourceFile)) {
                    def newFile = "release-pipeline/project/dist/myFile-1.0.js"

                    writeFile(file: newFile, encoding: "UTF-8", text: readFile(file: sourceFile, encoding: "UTF-8"))
                } */
                archiveArtifacts '/app/build/outputs/apk/debug/*.apk'
            }
        }
    }
}