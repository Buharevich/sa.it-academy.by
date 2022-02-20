# 04.GitOps

## My Repo

[GitHub](https://github.com/RomikBY/test_repo/actions)

## Pipeline Log
```
2022-01-27T18:47:30.0408778Z Waiting for a runner to pick up this job...
2022-01-27T18:47:31.8593001Z Job is waiting for a hosted runner to come online.
2022-01-27T18:47:36.9634445Z Job is about to start running on the hosted runner: Hosted Agent (hosted)
2022-01-27T18:47:41.4838244Z Current runner version: '2.286.1'
2022-01-27T18:47:41.4864193Z ##[group]Operating System
2022-01-27T18:47:41.4864670Z Ubuntu
2022-01-27T18:47:41.4865054Z 20.04.3
2022-01-27T18:47:41.4865326Z LTS
2022-01-27T18:47:41.4865561Z ##[endgroup]
2022-01-27T18:47:41.4865897Z ##[group]Virtual Environment
2022-01-27T18:47:41.4866220Z Environment: ubuntu-20.04
2022-01-27T18:47:41.4867109Z Version: 20220123.1
2022-01-27T18:47:41.4867593Z Included Software: https://github.com/actions/virtual-environments/blob/ubuntu20/20220123.1/images/linux/Ubuntu2004-Readme.md
2022-01-27T18:47:41.4868262Z Image Release: https://github.com/actions/virtual-environments/releases/tag/ubuntu20%2F20220123.1
2022-01-27T18:47:41.4868733Z ##[endgroup]
2022-01-27T18:47:41.4869041Z ##[group]Virtual Environment Provisioner
2022-01-27T18:47:41.4869603Z 1.0.0.0-main-20211214-1
2022-01-27T18:47:41.4870155Z ##[endgroup]
2022-01-27T18:47:41.4871080Z ##[group]GITHUB_TOKEN Permissions
2022-01-27T18:47:41.4871659Z Actions: write
2022-01-27T18:47:41.4872156Z Checks: write
2022-01-27T18:47:41.4872484Z Contents: write
2022-01-27T18:47:41.4872802Z Deployments: write
2022-01-27T18:47:41.4873056Z Discussions: write
2022-01-27T18:47:41.4873321Z Issues: write
2022-01-27T18:47:41.4873649Z Metadata: read
2022-01-27T18:47:41.4873950Z Packages: write
2022-01-27T18:47:41.4874190Z Pages: write
2022-01-27T18:47:41.4874479Z PullRequests: write
2022-01-27T18:47:41.4874758Z RepositoryProjects: write
2022-01-27T18:47:41.4875127Z SecurityEvents: write
2022-01-27T18:47:41.4875394Z Statuses: write
2022-01-27T18:47:41.4875687Z ##[endgroup]
2022-01-27T18:47:41.4879846Z Secret source: Actions
2022-01-27T18:47:41.4880435Z Prepare workflow directory
2022-01-27T18:47:41.5909014Z Prepare all required actions
2022-01-27T18:47:41.6116782Z Getting action download info
2022-01-27T18:47:41.8654224Z Download action repository 'jitterbit/get-changed-files@v1' (SHA:b17fbb00bdc0c0f63fcf166580804b4d2cdc2a42)
2022-01-27T18:47:42.3142426Z Download action repository 'actions/upload-artifact@v2' (SHA:82c141cc518b40d92cc801eee768e7aafc9c2fa2)
2022-01-27T18:47:42.9169577Z ##[group]Run jitterbit/get-changed-files@v1
2022-01-27T18:47:42.9170139Z with:
2022-01-27T18:47:42.9170468Z   format: json
2022-01-27T18:47:42.9171039Z   token: ***
2022-01-27T18:47:42.9171403Z ##[endgroup]
2022-01-27T18:47:43.1710822Z Base commit: 7c303798ca782562cd51ceb1af8276dfdd462dea
2022-01-27T18:47:43.1711948Z Head commit: 2a3c81b6c1709addc1308725a21d8352fec8742c
2022-01-27T18:47:43.6291658Z All: ["test1.txt","test2.txt","test3.txt","test5.txt"]
2022-01-27T18:47:43.6334365Z Added: ["test2.txt","test3.txt"]
2022-01-27T18:47:43.6335748Z Modified: ["test1.txt"]
2022-01-27T18:47:43.6336899Z Removed: ["test5.txt"]
2022-01-27T18:47:43.6337813Z Renamed: []
2022-01-27T18:47:43.6338878Z Added or modified: ["test1.txt","test2.txt","test3.txt"]
2022-01-27T18:47:43.6578328Z ##[group]Run readarray -t added_file <<<"$(jq -r '.[]' <<<'["test2.txt","test3.txt"]')"
2022-01-27T18:47:43.6579200Z [36;1mreadarray -t added_file <<<"$(jq -r '.[]' <<<'["test2.txt","test3.txt"]')"[0m
2022-01-27T18:47:43.6579730Z [36;1mfor added_file in ${added_file[@]}; do[0m
2022-01-27T18:47:43.6580159Z [36;1m  echo "Added files: ${added_file}." >> check_file_report.log[0m
2022-01-27T18:47:43.6580583Z [36;1mdone[0m
2022-01-27T18:47:43.6640288Z shell: /usr/bin/bash -e {0}
2022-01-27T18:47:43.6640830Z ##[endgroup]
2022-01-27T18:47:44.0961975Z ##[group]Run readarray -t changed_file <<<"$(jq -r '.[]' <<<'')"
2022-01-27T18:47:44.0962446Z [36;1mreadarray -t changed_file <<<"$(jq -r '.[]' <<<'')"[0m
2022-01-27T18:47:44.0962827Z [36;1mfor changed_file in ${changed_file[@]}; do[0m
2022-01-27T18:47:44.0963366Z [36;1m  echo "Changed files: ${changed_file}." >> check_file_report.log[0m
2022-01-27T18:47:44.0963680Z [36;1mdone[0m
2022-01-27T18:47:44.1018644Z shell: /usr/bin/bash -e {0}
2022-01-27T18:47:44.1018908Z ##[endgroup]
2022-01-27T18:47:44.1654354Z ##[group]Run readarray -t modified_file <<<"$(jq -r '.[]' <<<'["test1.txt"]')"
2022-01-27T18:47:44.1654816Z [36;1mreadarray -t modified_file <<<"$(jq -r '.[]' <<<'["test1.txt"]')"[0m
2022-01-27T18:47:44.1655332Z [36;1mfor modified_file in ${modified_file[@]}; do[0m
2022-01-27T18:47:44.1655642Z [36;1m  echo "Modified files: ${modified_file}." >> check_file_report.log[0m
2022-01-27T18:47:44.1656653Z [36;1mdone[0m
2022-01-27T18:47:44.1710756Z shell: /usr/bin/bash -e {0}
2022-01-27T18:47:44.1711027Z ##[endgroup]
2022-01-27T18:47:44.2278097Z ##[group]Run readarray -t removed_file <<<"$(jq -r '.[]' <<<'["test5.txt"]')"
2022-01-27T18:47:44.2278620Z [36;1mreadarray -t removed_file <<<"$(jq -r '.[]' <<<'["test5.txt"]')"[0m
2022-01-27T18:47:44.2278998Z [36;1mfor removed_file in ${removed_file[@]}; do[0m
2022-01-27T18:47:44.2279485Z [36;1m  echo "removed files: ${removed_file}." >> check_file_report.log[0m
2022-01-27T18:47:44.2279787Z [36;1mdone[0m
2022-01-27T18:47:44.2335222Z shell: /usr/bin/bash -e {0}
2022-01-27T18:47:44.2335550Z ##[endgroup]
2022-01-27T18:47:44.3164948Z ##[group]Run readarray -t renamed_file <<<"$(jq -r '.[]' <<<'[]')"
2022-01-27T18:47:44.3165340Z [36;1mreadarray -t renamed_file <<<"$(jq -r '.[]' <<<'[]')"[0m
2022-01-27T18:47:44.3165634Z [36;1mfor renamed_file in ${renamed_file[@]}; do[0m
2022-01-27T18:47:44.3165933Z [36;1m  echo "renamed files: ${renamed_file}." >> check_file_report.log[0m
2022-01-27T18:47:44.3166202Z [36;1mdone    [0m
2022-01-27T18:47:44.3217991Z shell: /usr/bin/bash -e {0}
2022-01-27T18:47:44.3218197Z ##[endgroup]
2022-01-27T18:47:44.3783061Z ##[group]Run actions/upload-artifact@v2
2022-01-27T18:47:44.3783348Z with:
2022-01-27T18:47:44.3783546Z   path: check_file_report.log
2022-01-27T18:47:44.3783766Z   name: artifact
2022-01-27T18:47:44.3783970Z   if-no-files-found: warn
2022-01-27T18:47:44.3784192Z ##[endgroup]
2022-01-27T18:47:44.4480026Z With the provided path, there will be 1 file uploaded
2022-01-27T18:47:44.4486070Z Starting artifact upload
2022-01-27T18:47:44.4487501Z For more detailed logs during the artifact upload process, enable step-debugging: https://docs.github.com/actions/monitoring-and-troubleshooting-workflows/enabling-debug-logging#enabling-step-debug-logging
2022-01-27T18:47:44.4491019Z Artifact name is valid!
2022-01-27T18:47:44.6070682Z Container for artifact "artifact" successfully created. Starting upload of file(s)
2022-01-27T18:47:44.8919616Z Total size of all the files uploaded is 70 bytes
2022-01-27T18:47:44.8920152Z File upload process has finished. Finalizing the artifact upload
2022-01-27T18:47:44.9932359Z Artifact has been finalized. All files have been successfully uploaded!
2022-01-27T18:47:44.9932680Z 
2022-01-27T18:47:44.9943359Z The raw size of all the files that were specified for upload is 101 bytes
2022-01-27T18:47:44.9944099Z The size of all the files that were uploaded is 70 bytes. This takes into account any gzip compression used to reduce the upload size, time and storage
2022-01-27T18:47:44.9944493Z 
2022-01-27T18:47:44.9945331Z Note: The size of downloaded zips can differ significantly from the reported size. For more information see: https://github.com/actions/upload-artifact#zipped-artifact-downloads 
2022-01-27T18:47:44.9945662Z 
2022-01-27T18:47:44.9945860Z Artifact artifact has been successfully uploaded!
2022-01-27T18:47:45.0081922Z Cleaning up orphan processes

```