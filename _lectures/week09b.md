---
title: "Week 09b - Wed 05/27"
lecture_date: 2026-05-27
description: "Merging PRs, Release Notes, Videos"
ready: true
layout: default
parent: lectures
---

# {{page.title}} - {{page.descripion}}


Clarifications:

* Tuesday of week 9 was the last day that you can submit *new* PRs to be reviewed by staff.
* By today, PRs need to be *already in a mergeable state*
  * Passing all CI/CD checks
  * Meeting all of the criteria in the PR checklist
  * Already reviewed/approved by a team member

Any PRs that are not in a reviewable/mergable state are subject to being closed without further review by the staff. 

Throughout week 9, we will continue to review PRs that are already in the queue, with the goal of having all of the PR queues empty by the start of week 10.

## What to work on after last PR is merged

* Release Notes
* Videos

You can read more about those below.

## But first

* If your team still has open PRs, get them mergable!
* If your team is done with PRs: Your "prod" site is linked in the table here in the `Dokku Prod` column.
* Make sure that all of the features work!
* Look for bugs. If you find bugs, create issues for them, and make new PRs to fix them.   Bug fix PRs may be submitted at any time, and *might* be reviewed and merged by the staff.
* *This is not a loophole to add new features*.  These are only bug fixes, and they *do not earn additional points* for the team.  They just help you present a better user experience in your video and release notes.
* Please create the qa dokku instance if your team hasn't done that yet; those are linked in the `Dokku qa` column below.
* We will be using both the `dokku prod` and the `dokku qa` instances during the final product reviews.

| Team <br ><span style="font-size:80%">Links to Slack</span>| Project <br ><span style="font-size:80%">Links to Legacy Repo</span> | Team Repo | PRs | Github Pages | Kanban | Dokku Prod | Dokku qa |
|------|----|------|-----|--------------|--------|------------|----------|{% for team in site.teams %}{% capture repoName %}proj-{{team.legacy_project}}-{{team.team}}{% endcapture %}
|  [{{team.team}}]({{team.slack}}) | [{{team.legacy_project}}](https://github.com/ucsb-cs156/proj-{{team.legacy_project}}) | [ team repo ]({{page.githubOrgUrl}}/{{repoName}}) |   [ PRs ]({{page.githubOrgUrl}}/{{repoName}}/pulls) |  [ github pages ]({{page.githubPagesUrl}}/{{repoName}}) | [ kanban ]({{page.githubProjectsUrl}}/{{team.legacy_kanban}}) | [ dokku prod ](https://{{team.legacy_project}}.dokku-{{team.dokku}}.cs.ucsb.edu) | [ dokku qa ](https://{{team.legacy_project}}-qa.dokku-{{team.dokku}}.cs.ucsb.edu) |{% endfor %}


# Final Class Meeting

{% include final_class_meeting.md %}

# Release Notes

{% include release_notes.md %}

# Final Presentation

{% include final_presentation.md %}

# Example Videos

{% include example_videos.md %}

# Final Exam

{% include final_exam.md %}
