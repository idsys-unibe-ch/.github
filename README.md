# .github

## Community Health Files

This repository currently features three different issue templates and one pull request template. When creating a new issue the template chooser is presented
and a template has to be chosen for the new issue. Nevertheless is still possible to start from a blank issue.  
For pull requests only one template is available for all kinds of PRs.

The templates are rather extensive and shall help its user to not forget certain aspects of an issue or a PR. **Sections that are not applicable can be freely deleted!**

**Regarding the role of the task template:** This template should only be used for issues, for which none of the other two is applicable. Examples for such cases might be

* An epic describing a bigger task where the subtasks might become new issues
* Task to create a dump of a database
* Action plan for a maintenance window
* Creating a report for somebody

## Scripts

### `massage_repo.sh`

Use this script on newly created repositories to update various settings to team
standards. Instead of clicking through the GUI over at GitHub, this is handled
by this nice script. Things currently manged by the script include:

- Setting up autolink reference to Service Now (SNOW)[^1]

[^1]: Links to Service Now tickets are automatically created when entered in the
  form SNOW-???, i.e.  SNOW-INC98973422
