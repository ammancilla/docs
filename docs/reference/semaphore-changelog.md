# Semaphore Changelog

Thank you for using Semaphore!
We continuously deploy changes that improve the product for you.
This page is updated on a weekly basis.

### Week of September 2, 2019

- New feature: Visual Workflow Builder, now in public beta. Build your Semaphore
  pipeline with a point-and-click interface.
- New users can choose between giving access to only public, or both public and
  private GitHub repositories.
- Organization admins can change their organization URL.

### Week of August 19, 2019

- New feature: [`parallelism`
  property](https://docs.semaphoreci.com/article/50-pipeline-yaml#parallelism)
  to easily generate parallel jobs.
- Docker-based agents can now [use private container images from any
  registry](https://docs.semaphoreci.com/article/127-custom-ci-cd-environment-with-docker#pulling-private-docker-images-from-generic-docker-registries).

### Week of August 12, 2019

- Updates to the [Ubuntu 18.04 VM
  image](https://docs.semaphoreci.com/article/32-ubuntu-1804-image): 
  - Chrome and ChromeDriver updated to version 76
  - docker-ce updated to 19.03.1
  - git-lfs updated to 2.8.0
  - heroku updated to 7.27.1
  - java 8 updated to u222
  - java 11 updated to 11.0.4
  - phpunit updated to 7.5.14
  - pip updated to 19.2.1
  - yarn updated to 1.17.3

### Week of August 5, 2019

- New feature: [Global job
  configuration](https://docs.semaphoreci.com/article/50-pipeline-yaml#global_job_config).
  Define common configuration and apply it across all blocks in a pipeline.
- You can now whitelist contributors for which your organization will run
  Semaphore workflows when they submit a pull request from a fork.
  You can also whitelist secrets to be exposed. See your project's Settings in
  web UI.
- Docker-based agents can now use [private container images from Google
  Container
  Registry](https://docs.semaphoreci.com/article/127-custom-ci-cd-environment-with-docker#pulling-private-docker-images-from-google-gcr).
- [Dependency caching](https://docs.semaphoreci.com/article/149-caching) is now
  much simpler. Just write `cache restore` and `cache store` and Semaphore will
  do the right thing for common language dependencies.
- macOS platform:
  - Flutter version update to v1.8.3
  - New image spec - [macOS Mojave](https://docs.semaphoreci.com/article/120-macos-mojave-image)

### Week of July 29, 2019

- New features: [Pull request and Git tag
  support](https://docs.semaphoreci.com/article/152-project-workflow-tigger-options).
  Have full control over which GitHub trigger new workflows.
  Choose from default branch only, any push to any branch, push to pull
  requests, and push to pull requests from forked repositories.
    - As a bonus, you can turn off exposure of secrets in forked pull requests.
    - The project page can now show activity from branches, pull requests and
      tags separately.
- New feature: [Auto-cancel pipeline
  strategies](https://docs.semaphoreci.com/article/153-auto-cancel).  Stop
  running a pipelines when there are newer commits in the repo.  Use the new
  [`auto_cancel`
  property](https://docs.semaphoreci.com/article/50-pipeline-yaml#auto_cancel)
  in your pipeline configuration.
- macOS platform:
  - Xcode 11 Beta version update 5 (11M382q).
  - Xcode 10.3 with default simulators preinstalled on Mojave image.
  - Flutter version update to v1.7.8+hotfix.4.
  - Fastlane version update to 2.128.1.
  - Cocoapods version update to 1.7.5.
  - New image spec - [macOS Mojave](https://docs.semaphoreci.com/article/120-macos-mojave-image)
- New [environment variables available in Semaphore
  jobs](https://docs.semaphoreci.com/article/12-environment-variables):
  - `SEMAPHORE_GIT_REPO_SLUG`
  - `SEMAPHORE_GIT_REF_TYPE`
  - `SEMAPHORE_GIT_REF`
  - `SEMAPHORE_GIT_COMMIT_RANGE`
  - `SEMAPHORE_GIT_TAG_NAME`
  - `SEMAPHORE_GIT_PR_SLUG`
  - `SEMAPHORE_GIT_PR_SHA`
  - `SEMAPHORE_GIT_PR_NUMBER`
  - `SEMAPHORE_GIT_PR_NAME`
  - `SEMAPHORE_ORGANIZATION_URL`

### Week of July 22, 2019

- New feature: model complex workflows with pipeline dependencies. Learn more
  about what you can do in the
  [blog post](https://semaphoreci.com/blog/introducing-cicd-pipeline-dependencies).
- New feature: [fail-fast on the first
  failure](https://docs.semaphoreci.com/article/151-fail-fast-stop-running-tests-on-the-first-failure).
  Now you can stop everything in your pipeline as soon as a failure is detected,
  or stops only the jobs and blocks in your pipeline that haven't yet started.
- A new global sidebar. It uses less screen real estate and you can star
  projects and dashboards to appear on top of the list. Also, it loads really
  fast.

### Week of July 15, 2019

- New feature: Scheduled CI/CD workflows, aka cron jobs.
  Open your project, and find the new "Project Settings" button at the top-right.
  From there you can create and edit your scheduled workflows using
  the standard cron syntax.
- Also on the new Project Settings screen, you can rename and delete your
  project.

### Week of July 1, 2019

- AWS ECR support for Docker-based environment: Host your private Docker images
  on AWS and use them to define your
  [custom CI/CD environment](https://docs.semaphoreci.com/article/127-custom-ci-cd-environment-with-docker)
  on Semaphore.
- [Skip CI](https://docs.semaphoreci.com/article/146-skip-building-some-commits-with-ci-skip):
  If you add `[skip ci]` or `[ci skip]` to your Git commit message,
  Semaphore will not trigger a new workflow.
- Context of a [Github Status checks](https://developer.github.com/v3/repos/statuses/)
  has been changed to include information about a build source, which
  can be one of the following:
  - `ci/semaphoreci/push`
  - `ci/semaphoreci/pr`
  - `ci/semaphoreci/tag`

[Please update your settings on GitHub](https://help.github.com/en/articles/enabling-required-status-checks)
if you are using protected branches with required status checks.

### Week of June 24, 2019

- macOS platform:
  - Xcode 11 Beta with default simulators preinstalled on Mojave image.
  - [macOS Mojave](https://docs.semaphoreci.com/article/120-macos-mojave-image) updated to 10.14.5.

### Week of June 10, 2019

- The workflow page got a fresh new look. It shows the elapsed time
  of each job, letting you spot inefficiencies easily.
  It also prepares the ground for some new features we'll announce
  soon.
- Reduced the time it takes a task to complete after the last job.

### Week of May 27, 2019

- [Custom Docker-based CI/CD environments are in GA](https://semaphoreci.com/blog/define-your-cicd-with-docker)
  Semaphore now supports custom CI/CD environments based on Docker containers.
  Get started with [Custom CI/CD environment with Docker](https://docs.semaphoreci.com/article/127-custom-ci-cd-environment-with-docker).

- Launched support for skipping blocks based on conditions, e.g. `branch != 'master'`.
  Read more about [skipping blocks](https://docs.semaphoreci.com/article/50-pipeline-yaml#skip-in-blocks)
  and the introduction of [Conditions domain specific language](https://docs.semaphoreci.com/article/142-conditions-reference)
  that allows the expression of complex conditional rules in your pipelines.

- Owners and admins can now set [Budget Alerts](https://docs.semaphoreci.com/article/104-billing#budget-alert).

- New Semaphore approved convenience Docker images released:
  - [Alpine](https://hub.docker.com/r/semaphoreci/alpine)
  - [Android](https://hub.docker.com/r/semaphoreci/android)
  - [Clojure](https://hub.docker.com/r/semaphoreci/clojure)
  - [Elixir](https://hub.docker.com/r/semaphoreci/elixir)
  - [Golang](https://hub.docker.com/r/semaphoreci/golang)
  - [Haskell](https://hub.docker.com/r/semaphoreci/haskell)
  - [Node](https://hub.docker.com/r/semaphoreci/node)
  - [Openjdk](https://hub.docker.com/r/semaphoreci/openjdk)
  - [Php](https://hub.docker.com/r/semaphoreci/php)
  - [Python](https://hub.docker.com/r/semaphoreci/python)
  - [Ruby](https://hub.docker.com/r/semaphoreci/ruby)
  - [Rust](https://hub.docker.com/r/semaphoreci/rust)
  - [Ubuntu](https://hub.docker.com/r/semaphoreci/ubuntu)

- Version `v0.13.0` of the Semaphore CLI has been released.
  - `sem debug job` works without configuring the CLI with an SSH key.
    Keys are now generated server side.
  - `sem attach` can attach to any running job without the need to inject
    public SSH keys as part of your Pipeline configuration.
  - Debugging and attaching to jobs works for Docker based CI/CD environments
  - Read the updated documentation about [Debugging with SSH Access](https://docs.semaphoreci.com/article/75-debugging-with-ssh-access).

Upgrade to the latest CLI version:

``` bash
curl https://storage.googleapis.com/sem-cli-releases/get.sh | bash
```

### Week of May 13, 2019

- [iOS support is in GA](https://semaphoreci.com/blog/introducing-ios-cicd):
  Semaphore now supports building, testing and deploying applications for any
  Apple device.
  Get started with [Xcode tutorial](https://docs.semaphoreci.com/article/124-ios-continuous-integration-xcode)
  and [example Swift project](https://github.com/semaphoreci-demos/semaphore-demo-ios-swift-xcode).
- macOS platform:
  - Xcode upgraded to 10.2.1
- New feature: [schedule CI/CD workflows](https://docs.semaphoreci.com/article/52-projects-yaml-reference#schedulers)
  using standard Cron syntax.

### Week of Apr 22, 2019

- [Fastlane plugin](https://github.com/semaphoreci/fastlane-plugin-semaphore) is
  now available.
- Platform updates:
  - Chrome 74, ChromeDriver 74
  - Heroku 7.24.1
  - Git-lfs 2.7.2
  - Pip 19.1
  - Phpunit 7.5.9
  - Removed Oracle Java 7,9,10; Java 8 and 11 are now based on OpenJDK.

### Week of Apr 15, 2019

- Docker-based environment is now available to all organizations as a public beta.
- New feature: [epilogue has `on_pass` and `on_fail`
  properties](https://docs.semaphoreci.com/article/50-pipeline-yaml#the-epilogue-property)
  which run commands based on the job's result.
- sem CLI v0.10.0 released, with an option to [create a secret based on
  environment variables](https://docs.semaphoreci.com/article/53-sem-reference#sem-create-secret-with-environment-variables-and-files)
  in a single command.
- Jobs now export `TERM=xterm`. This allows running tools that depend on
  exported `TERM` settings, such as psql.
- Jobs now export `PAGER=cat`. This prevents some commands from infinitely
  waiting for user input, such as `git log`.
- Job logs are now fully UTF-8 compliant.


### Week of Apr 8, 2019

- New feature: [Run jobs inside a custom Docker
  container](https://docs.semaphoreci.com/article/127-custom-ci-cd-environment-with-docker) (beta).
- Organization owners can promote members to an [Admin
  role](https://docs.semaphoreci.com/article/106-user-management-and-permissions),
  to delegate billing, people and project management.
  See the `/people` page within your organization.
- Slack notifications can be created and managed in the UI.

### Week of Mar 25, 2019

- Platform updates:
  - Chrome 73
  - Elixir 1.8.1
  - Go 1.12.1
  - Ruby versions >=2.6.0 have bundler 2.0.1 and rubygems>3 preinstalled
  - Scala 2.12.7

### Week of Mar 18, 2019

- macOS, iOS support is in open beta: see
  [tutorial](https://docs.semaphoreci.com/article/124-ios-continuous-integration-xcode).

### Week of Mar 12, 2019

- Platform updates:
  - Heroku 7.22.4
  - Libvirt, qemu, virsh are now part of the Ubuntu VM image with virtual network `192.168.123.0/24`

### Week of Feb 25, 2019

- You can now create and manage secrets in the UI.
- You can create multiple projects from the same screen by selecting any number
  of Git repositories.
- The screen should be a little more pleasant while your dashboard is loading.
- In case of misconfigured YAML file, the error message is now nicely wrapped in
  a red box.
- Fixed an issue with sliders on Linux/Chrome.
- Platform additions:
  - Go 1.12
  - libvirt-bin, qemu-kvm and virtinst
- Platform updates:
  - git 2.21
  - git-lfs 2.7.1
  - gradle 5.2
  - heroku to 7.22.2
  - sbt 0.13.17
- Introduced [Tutorials and example projects](https://docs.semaphoreci.com/article/123-tutorials-and-example-projects),
  a handy portal to practical examples of CI/CD pipelines, with links to open
  source repositories that you can copy.

### Week of Feb 18, 2019

- Added contextual CLI widgets to the top-right corner of all pages. The `>_`
  widget shows CLI commands that you can run to perform the same actions that
  you see in the UI.
- Slack notifications can be [filtered by pipeline result](https://docs.semaphoreci.com/article/91-slack-notifications#filtering-by-pipeline-result).
- [macOS Mojave](https://docs.semaphoreci.com/article/120-macos-mojave-image)
  image introduced, as iOS / macOS support enters
  [closed beta](https://semaphoreci.com/product/ios).
- Syntax highlighting in docs.

### Week of Feb 11, 2019

- New feature: Add project from UI. The much-loved feature of Semaphore Classic
  is now available in Semaphore 2.0 as well. Using the command-line interface
  remains an option, of course.
- Platform:
  - Added new APT mirrors for faster apt-get installations in Ubuntu1804 image.
  - Chrome updated to 72.
  - Heroku CLI updated to 7.21.

### Week of Feb 4, 2019

- Platform:
  - ChromeDriver updated to 2.46.
  - Added Ruby 2.6.0, 2.6.1.
  - If repository contains `.ruby-version` file, Semaphore automatically fetches
    a pre-built version of the specified Ruby.

### Week of Jan 28, 2019

- Platform:
  - Added Java 11.

### Week of Jan 7, 2019

- New feature: Billing insights. Organization owners can now see
  the top spending projects and daily spending charts which contain
  spending per machine type. Data is available for any selected period.
- Launching a promotion manually now shows a confirmation dialog.
- Fixed: checkout command doesn't fail on git reference tags.

### Week of Dec 17, 2018

- New feature: Restart workflow.
  Available via “Restart" button on the workflow page,
  or `sem rebuild workflow <id>` in CLI.
- [checkout](https://docs.semaphoreci.com/article/54-toolbox-reference#libcheckout)
  runs faster by doing a shallow git clone.
- We improved the speed and stability of the UI, most notably on pages
  that load workflows and jobs.
- Changelog initiated. 🚀