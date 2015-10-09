# Pest Control Process

This is an important part of our developer role here. It allows us time to catch and resolve bugs and issues which we would not otherwise see or prioritised. This creates a better development environment for us all as well as improving the customers experience on our site. 

No one likes a buggy application, so why should we build one?

## tl;dr
- Check bug reporting systems regularly
- One developer responsible on a daily basis
- Group meetings once a sprint.

## Process

Expedited issues are not covered here, please see the expedited proceed for details.

The most important part of Bugsnag is communication. You should be talking to people about what you're seeing and updating on things you're working on etc. Don't suffer in silence on a tough bug, ask for help. And don't assume an issue is being looked at, check!

* Developer rotated on a weekly basis.
  * Handled by SE's which are able to delegate as they see fit.
  * Spends ~1 hour a day on this work.
  * Organises the raising of new bugs,
    * Add customer impact to description
    * Found via reporting systems (currently Bugsnag and HxMetrics)
  * Remains in sprint.
  * Time spent will vary, but should not be influenced by pod/sprint deadlines.
* Use the general web project on JIRA (not bugsnag queue).
  * Use type of `bug`.
* Bugs will be completed during normal sprint work by pods like all other work.

## Working Group

A member of each pod is encouraged to attend to assist in the assignment of bugs and contribute to improving this process.

* Chaired by developer on rotation.
* Triage current bugs.
* Assign bugs to pod backlogs.
* What’s happened since last time?
  * Monitor progress of bug completion.
  * Recurring themes.
* Review current process.
* Send email update.

## Systems used

### Bugsnag

You'll require our Bugsnag credentials. Ask the last person on bugsnag for these.

#### How do I find bugs?
Errors on our site are reported to [Bugsnag](https://bugsnag.com/holiday-extras/trip-app-js/errors) and are visible in the dashboard.

The errors are split by project and you can switch between these using the menu in the top left corner.

![](/images/pest-control-process/project-selector.png)

Errors can be viewed in either a grouped or ungrouped state.

![](/images/pest-control-process/grouping.png)

Most people prefer the ungrouped view as the grouping isn't always accurate.

##### Grouped View
When viewing grouped errors you can however get an idea of the bugs importance.

![](/images/pest-control-process/dashboard-bug-view.png)

The stats show you:
- occurrences (how many times has the happened)
- users (how many individual people has it happened to)
- last 2 weeks (instance graph of last two weeks)
- stage (what environment is this happening in)
- severity (how important do we think this is).

You can use the search form on the left hand side to limit what bugs you see:

![](/images/pest-control-process/bug-filter.png)

##### Ungrouped View
Ungrouped view shows you a live error by error view of the project. It also shows you more information regarding each bug such as user and device settings.

As with the grouped view you can click on a bug to view more information.

##### Bug detail view
To get more info on a bug you click on it from the dashboard view. This takes you to more information on that specific bug. 

You can use the stats on this screen (such as the event count, user count, metrics and history) to figure out if the bug is affecting a lot of our users.

![](/images/pest-control-process/stats.png)

You can use the information available in the tabs to find the cause and attempt to replicate the issue.

![](/images/pest-control-process/tabs.png)

_The information and tabs available will change depending on the bug type and project._

#### What do I do if I find a bug?
Any bug worth mentioning is worth raising as a JIRA. There's a handy button on the Bugsnag detail view that will do this for you:

![](/images/pest-control-process/create-jira.png)

Add as much detail about the bug as you can. E.g. how can you duplicate it? Who is it affecting? If it's something which should be expedited then let people know and get working on it.

### hxMetrics

The [metrics system](https://metrics.holidayextras.com/) is a graph based tool which allows us to monitor the error rates on our systems. You will have to be on our WIFI or Junos to access this.

Clicking in the search bar shows all the available systems. You should mostly be concerned about production systems in your Bugsnag duties. Checking "HTTP responses" and "controllers" are the main focus points for HAPI and Render production. That doesn't mean don't check the others, just that these are the main concern.

#### HTTP responses
Clicking on "HTTP responses" for a system shows you a live view of the HTTP responses that aren't good. These are listed in their count order, summarised at the top and then divided among the different urls below. 

You can change the duration and times of search at the top in the navigation bar.

![](/images/pest-control-process/timeframe.png)

Generally speaking, the higher a number is above the "error" and "error rate" graphs - the worse things are.

Be advised though, a lot of these errors will be from user error. Use common sense when looking at an error to figure out if it's a problem with the systems/our code or a user that can't type their card number out properly.

#### controllers
This shows errors at a controller and method level. The metrics displayed are the same as above, but the grouping is different.

### FAQ
Q. I've found a bug, is it important?

A. It's mostly down to stats and your gut feeling. Is it affecting people and preventing bookings? If in doubt, ask! It's better that we catch a bug that is causing problems then assume it's not an issue and let it slide.

Q. I have a question regarding pest control, what should I do?

A. Write your question on the working group agenda and attend the meeting. The chances are if you're thinking it, then someone else will be as well. Be courageous and ask the question no one else does. There are no stupid questions.

Q. Bugsy?

A. Don't ask.
