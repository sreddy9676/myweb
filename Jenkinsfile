pipeline{
    agent any
    stages{
        stage("Fortis-Development-server"){
            when {
                // This works only in multi branch pipeline
                branch 'dev-1'
            }
            steps{
                sshPublisher(publishers: [sshPublisherDesc(configName: 'Fortis-Development-server', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/var/www/jenkins', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
        stage("Fortis-Staging-server"){
            when {
                branch 'master'
            }
            steps{
                sshPublisher(publishers: [sshPublisherDesc(configName: 'Fortis-Staging-server', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/var/www/jenkins', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}
