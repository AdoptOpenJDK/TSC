This release checklist based on the [release doc](https://github.com/AdoptOpenJDK/openjdk-build/blob/master/RELEASING.md) captures what activities must happen during a release.  

The target release date is: _______
The release champion for this release is: _________

The role of the release champion is to ensure that all release activities listed in this checklist get completed (by delegation to the broader team or by the release champion themselves).  The final task of the release champion during a release is to confirm that all items in the checklist were completed satisfactorily and the release can be declared complete. 

Everyone participating in a release, including the release champion are requested to provide feedback into the release retrospective so that the release process can be continuously improved (through simplification and/or automation).

One Week Prior to Release:
- [ ] **Release Champion named** whose responsibility is to ensure every item in this checklist gets completed
- [ ] **Disable nightly testing** to free up resources and ensure no competing jobs during release week
- [ ] **Run a trial release pipeline** to ensure less surprises on release day (typically against a milestone build)

Release Week Checklist:
- [ ] **Add website banner** (_automate_* via github workflow in website repository) - Announce that we target releases to be available within 48 hours of the GA tags being available
- [ ] **Launch build pipelines** for each version being released [(as per release doc](https://github.com/AdoptOpenJDK/openjdk-build/blob/master/RELEASING.md#steps-for-every-version)) once release tags are available via [launch page](https://ci.adoptopenjdk.net/job/build-scripts/job/openjdk8-pipeline/build) in Jenkins.  Provide links in this issue to each version's pipeline build(s). There may be multiple pipelines per version if primary and secondary platforms are separated to expedite the release.
  - jdk8 pipeline(s): 
  - jdk11 pipeline(s): 
  - jdkxx pipeline(s): 
- [ ] **Summarize test results**.  Find each launched build pipeline in [TRSS](https://trss.adoptopenjdk.net/) to view a summary of test results.  Can use the Release Summary Report feature in TRSS to generate a summary of failures, history and possible issues in markup format to be added to this issue as a comment.  (_automate_* via github workflow or Jenkins job trigger or TRSS report to add a comment/table to this release issue)
- [ ] **Triage** each build and test failure in the release summary report (following the [Triage guidelines](https://github.com/AdoptOpenJDK/openjdk-tests/blob/master/doc/Triage.md)) and determine blocking or non-blocking.  
  - jdk8 triage summary:
  - jdk11 triage summary:
  - jdkxx triage summary:
- [ ] **Fix** blocking failures if they exist and confirm others are non-blocking.
- [ ] **Get TSC 'ready to publish' approval**, once no blocking failures exist.
- [ ] **Publish the release** (run the restricted access [release tool job](https://ci.adoptopenjdk.net/job/build-scripts/job/release/job/refactor_openjdk_release_tool/) on Jenkins)
- [ ] **Verify binaries published successfully** to github releases repo and website (_automate_*, this could also be an automated test)
- [ ] **Update support page** (_automate_* github workflow to create a PR to update [support.handlebars](https://github.com/AdoptOpenJDK/openjdk-website/blob/master/src/handlebars/support.handlebars))
- [ ] **Update release notes** (_automate_* - github workflow to create update for [release notes page](https://adoptopenjdk.net/release_notes.html))
- [ ] **Run homebrew-cask_updater** (via [Jenkins homebrew-cask_updater job link](https://ci.adoptopenjdk.net/job/homebrew-cask_updater/)) once binaries published successfully (this can be automated / triggered by a test for published artifacts)
- [ ] **Trigger linux installers pipeline** currently it is part of the build pipelines (will eventually be updated to run independently)
- [ ] **Publicize the release** via Slack #release channel and Twitter (can be partially automated)
- [ ] **Trigger docker images pipeline** and confirm they are published correctly
- [ ] **Declare the release complete** and close this issue