
# Azure Boards

DevOps is all about delivering value; while continuous integration and continuous delivery are key practices, teams also need continuous planning. As the saying software development is a team sport - it is vital that everyone stays on the same page. In addition to GitHub issues that help teams manage work artifacts such as issues and bugs teams can take advantage of Azure Boards which provides a wealth of project management functionality that spans Kanban boards, backlogs, team dashboards, and custom reporting. 

In this demo I am going to show you how we leverage the integration between Azure Boards and GitHub to link and track work items with code changes. I will start with Azure Boards - Azure Boards  provides a wealth of project management functionality that spans Kanban boards, backlogs, team dashboards, and custom reporting. Here I am in my Azure Boards backlog view - this view gives me a list of work items such as user stories, bugs, tasks which are arranged in the order of priority. So, I know this is the work item I need to work on next. Let me open the work item to see the details. 

This is a user story to sort the airports listed in the booking form in alphabetical order by city.Let's take a look at our deployed site to see what the current booking experience is like. As you can see, the airports appear to be sorted by airport code, which isn't the behavior we want our users to see. So, I am going to get this fixed.

I will switch to the Kanban board view which provides me with a visual interactive space for everyone in the team to plan and show progress. With it, we track the critical information we need to see which work items are in progress, where the bottlenecks are, who work is assigned to, and more.

Just like sticky notes on a physical whiteboard, each work item is presented as cards and support quick status updates through drag-and-drop. 

I will move this user story onto the Active column - this will assigns it to me and sets its State to Active. I am going to make a note of the task ID for reference later during a future commit and pull request.

At Contoso, as a best practice we would create the user story at a higher level and add tasks to define how the story is to be implemented, but for our demo purposes here we'll leave it as a single work item. Also, we link the work items to our code commits in GitHub so we can track the progress of our development. As you can see here there is nothing in here yet. To link to GH,  we'll need to wire up a connection between this project and the GitHub repo.

I use Visual Studio code for my development. Here I have my Git repo cloned to my local machine. I'll start off by creating a new branch for this task. The work itself is pretty straightforward. I know the place where airports are provided to the user experience and I am going to change this so that they're being sorted by city name.

I will save my change and I will make a commit. I'll commit it using a comment that includes special syntax to link it to the Azure Boards task that I am working on. Now this commit will become trackable from project management, as long as it includes the phrase "Fixes AB#ID".

With the commit pushed, I'll create a pull request to drive those changes back into the master branch. I will inheriting the title from the commit, and also ahve the pull request mention "Fixes AB#ID" to link and complete the target work item when the pull request is merged.

Now we'll switch to the other side of the pull request and take on the role of reviewer. Assuming we trust the fix, we can merge the pull request to update master and kick off the CI/CD. Once the deployment works its way through build and release, we can confirm the new functionality. 

Return to the booking page (you'll need to log in again) and confirm the airports are sorted by city now (scroll down past the airports with no city name).

Since the user story we were working on was linked in a pull request that was approved, Azure DevOps will automatically transition the state of the work item to "Closed". You can also see that the related GitHub commits and pull request are linked to the work item.

Azure DevOps and GitHub provides teams a complete overview - they can trace how a user feedback or a user experience turned into a work item, how it was addressed in the code, how the code got built and tested and how the build got deployed to the customer. 

[closing]
