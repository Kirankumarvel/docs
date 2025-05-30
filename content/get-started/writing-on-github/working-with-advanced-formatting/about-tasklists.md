---
title: About tasklists
intro: 'You can use tasklists to break the work for an issue or pull request into smaller tasks, then track the full set of work to completion.'
product: '{% data reusables.gated-features.markdown-ui %}'
redirect_from:
  - /github/managing-your-work-on-github/managing-your-work-with-issues-and-pull-requests/about-task-lists
  - /articles/about-task-lists
  - /github/managing-your-work-on-github/about-task-lists
  - /issues/tracking-your-work-with-issues/creating-issues/about-task-lists
  - /issues/tracking-your-work-with-issues/about-task-lists
  - /get-started/writing-on-github/working-with-advanced-formatting/about-task-lists
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - Pull requests
  - Issues
---

## About tasklists

> [!IMPORTANT]
> Tasklists are {% data variables.release-phases.retired %}. You can read more about this on the [GitHub Blog](https://github.blog/changelog/2025-04-29-closing-down-code-scanning-alerts-tracked-in-tasklists/).
>
> {% ifversion sub-issues %} You can use sub-issues as the replacement for tasklist blocks. Sub-issues provide a dedicated section within each issue, making it easier to track related work without relying on Markdown. For more information about sub-issues, see [AUTOTITLE](/issues/tracking-your-work-with-issues/using-issues/adding-sub-issues). {% endif %}

A tasklist is a set of tasks that each render on a separate line with a clickable checkbox. You can select or deselect the checkboxes to mark the tasks as complete or incomplete.

You can use Markdown to create a tasklist in any comment on {% data variables.product.github %}. {% ifversion fpt or ghec %}If you reference an issue, pull request, or discussion in a tasklist, the reference will unfurl to show the title and state.{% endif %}

{% ifversion not fpt or ghec %}
You can view tasklist summary information in issue and pull request lists, when the tasklist is in the initial comment.
{% else %}

## About issue tasklists

If you add a tasklist to the body of an issue, the list has added functionality.

* To help you track your team's work on an issue, the progress of an issue's tasklist appears in various places on {% data variables.product.github %}, such as a repository's list of issues.
* If a task references another issue and someone closes that issue, the task's checkbox will automatically be marked as complete.
* If a task requires further tracking or discussion, you can convert the task to an issue by hovering over the task and clicking {% octicon "issue-opened" aria-label="The issue opened icon" %} in the upper-right corner of the task. To add more details before creating the issue, you can use keyboard shortcuts to open the new issue form. For more information, see [AUTOTITLE](/get-started/accessibility/keyboard-shortcuts#issues-and-pull-requests).
* Any issues referenced in the tasklist will specify that they are tracked in the referencing issue.

![Screenshot of an issue showing a tasklist under the header "Features." Three list items link to other issues.](/assets/images/help/writing/task-list-rendered.png)

{% endif %}

## Creating tasklists

{% data reusables.repositories.task-list-markdown %}

> [!NOTE]
> You cannot create tasklist items within closed issues or issues with linked pull requests.

## Reordering tasks

You can reorder the items in a tasklist. First, click or hover to the left of a task's checkbox until a grid of six dots appears. Then, drag and drop the grid to move the task to a new location.

You can reorder tasks across different lists in the same comment, but you cannot reorder tasks across different comments.

{% ifversion fpt or ghec %} ![Screenshot of a {% data variables.product.prodname_dotcom %} issue showing two tasks in a tasklist. A grid of six dots to the left of the second task is outlined in dark orange.](/assets/images/help/writing/task-list-reorder.png){% endif %}

{% ifversion fpt %}

## Converting tasks into issues

You can also convert tasks into issues. First, hover over one of the items in your tasklist and then click {% octicon "issue-opened" aria-label="Convert to issue" %}.

  ![Screenshot of an issue showing two tasks. The "Convert to issue" icon is highlighted with an orange outline.](/assets/images/help/writing/convert-task-lists-into-issues.png)

## Navigating tracked issues

Any issues that are referenced in a tasklist specify that they are tracked by the issue that contains the tasklist. To navigate to the tracking issue from the tracked issue, click on the tracking issue number in the **Tracked by** section next to the issue status.

![Screenshot of issue 3 showing the issue status of "Open" and the text "Tracked by issue #2", which is outlined in orange.](/assets/images/help/writing/task-list-tracked.png)

{% endif %}
