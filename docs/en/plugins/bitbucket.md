Plugin Bitbucket
=========================

This plugin notify you in Bitbucket about the build status with comments, tasks and build info.

Configuration
-------------

### Options

* **url** [string, required] - URL to Bitbucket.
* **token** [string, required] - $URL/plugins/servlet/access-tokens/manage Your API token.
* **project_key** [string, required] - Your Project Key ($URL/projects/$PROJECT_KEY/repos/$REPOSITORY_SLUG/).
* **respository_slug** [string, required] - Your Respository Slug ($URL/projects/$PROJECT_KEY/repos/$REPOSITORY_SLUG/).
* **create_task_per_fail** [bool, optional] - Create a task per "failed" plugin.
* **create_task_if_fail** [bool, optional] - Create one task if at least one plugin "failed".
* **update_build** [bool, optional] - Update build status in Bitbucket.
* **message** [string, optional] - Overwrite the default message.

### Examples

```yaml
complete:
    bitbucket:
      url: "https://bitbucket.yourhost.de"
      token: "123456"
      project_key: "test"
      respository_slug: "test-service"
      create_task_per_fail: true
      create_task_if_fail: false
      update_build: true
      message: ""
```