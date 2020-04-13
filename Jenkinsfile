//
// Copyright (c) 2020 Intel Corporation
//
// Licensed under the Apache License, Version 2.0 (the "License");
// you may not use this file except in compliance with the License.
// You may obtain a copy of the License at
//
//      http://www.apache.org/licenses/LICENSE-2.0
//
// Unless required by applicable law or agreed to in writing, software
// distributed under the License is distributed on an "AS IS" BASIS,
// WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
// See the License for the specific language governing permissions and
// limitations under the License.
//

@Library("edgex-global-pipelines@experimental") _

pipeline {
    agent { label 'centos7-docker-4c-2g' }
    stages {
        stage('Test') {
            steps {
                script {
                    def files = findFiles glob: 'snap/snapcraft.yaml'
                    println files.length

                    def notfiles = findFiles glob: 'snap/snapper.snap'
                    println notfiles.length
                }
            }
        }
    }
}
