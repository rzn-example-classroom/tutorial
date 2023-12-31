# Getting Started with GitHub Classroom
## For Instructors
### Why use GitHub Classroom?
GitHub is an industry standard platform for repository management, and Git is likewise the standard in version control. Introducing students to Git and GitHub as soon as possible will allow them to better track their own projects, work more effectively on group programming projects associated with classes, and better prepare them for software development in industry. 

From an instructor perspective, GitHub Classroom makes distributing, monitoring, collecting, and grading programming assignments much easier. By creating a template repository for an assignment, you can create a link that will allow each student to clone this repository, work on a private version of it, and turn it in when complete. Depending on the assignment, testing and grading can even be partially or fully automated. Furthermore, applying for education benefits allows students to use GitHub Codespaces (which provides online development environments for assignments). Overall, leveraging an environment designed for code makes managing computer science or engineering assignments far smoother.

### Note about these instructions
The [student guide](https://github.com/rzn-example-classroom/git-and-github-intro) is designed to correspond directly to the results of the these instructions. If you change something here, you may need to update the information you provide your students.

### Your GitHub Account
If you do not already have an existing GitHub account, you will first need to [sign up](https://github.com/signup) for one. Even if you have an existing professional account, if you intend to use GitHub classroom for more than one class or for more than one semester, you may want to create a new account, since your account may become crowded over time if you have existing organizations.

### Creating a GitHub Organization
#### Note about organizations
It is strongly recommended to create a separate GitHub Organization for each class and for each semester the class is offered. This makes it far easier to keep track of which assignments belong to which class, and to better manage student assignments, as there will be a repository added to the organization for *each* student for *each* assignment. 

More importantly, TAs must be added as an administrator/owner to the organization that they are to assist with; therefore, academic integrity issues can arise if the TA is added as an admin to an organization containing a class and assignments they have not yet taken. However, multiple class sections of the same class during the same semester should be grouped together unless you have a good reason not to do so. This has the added benefit of allowing cross-collaboration between class sections on group assignments.

It is also strongly recommended to first create a "main" or "template" organization holding the latest version of class files and assignments which you can then fork or "reuse" to create a new semester's organization and Classroom. 

#### Steps
1. Go to [github.com/settings/organizations](https://github.com/settings/organizations).
2. At the top right, select `New organization`.
	- Alternatively, you can also transform an existing account into an organization if you are not a member of any other organization, but this is generally not recommended unless you created a new account with an email specifically for that organization.
3. Select the `Free` plan.
4. Give your organization a unique and appropriate name, and provide a contact email (the email associated with your existing GitHub account will do).
	- An example name format is: `[university-abbreviation]-[course-id]-20XX` (or replace `20XX` with `main` or similar)
		- If your university offers the course more than once per academic year, you may wish to add a semester abbreviation as well (ex. `SP-20XX` for spring, instead of just `20XX`).
5. You can choose whether to declare the GitHub organization as belonging to either your personal account or a business or institution. 
	- The choice makes no functional difference, but it does make a legal difference in the form of the Terms of Service agreement used - read carefully if you select the latter option. 
	- If you are uncertain, choose the personal option - you can [upgrade to the corporate ToS](https://docs.github.com/en/organizations/managing-organization-settings/upgrading-to-the-corporate-terms-of-service) later, but currently there does not appear to be a way to downgrade to standard ToS or change the company name. However, the corporation name is not published anywhere on the organization page unless you manually add it, nor is any confirmation required from the corporate side for that option.
6. For now, you can skip adding members unless you already have the account details of any other instructors or TAs you would like to add. This is covered in more detail in the "Adding other instructors or TAs to your Classroom" section.
7. **Important:** Assuming you want student assignments to be private (invisible to other students and the wider internet), continue to the next subsection "Changing organization base permissions." Otherwise, skip this subsection.

##### Changing organization base permissions
To keep students from viewing each others' assignments, you will need to modify the default/base permissions granted by the organization to members. Later, when students accept their first assignment, they will be prompted to join your organization as a member. If they do so, they will by default be granted *read access* to *all* repositories under the organization, including those corresponding to other students' assignments. To resolve this:

1. Navigate to the main organization homepage, then to its `Settings` tab.
2. Under the `Access` submenu on the left, navigate to `Member privileges`.
3. The first setting here specifies the base permissions. By default, this is `Read`. **Change this to `No permission`.**
4. If your organization has existing repositories, GitHub will ask you to confirm the changes. Do so.
5. You may need to wait or refresh the page for the changes to take effect. At that point, your organization base permissions are properly configured.

### Creating template repositories
#### For assignment starter code or a course syllabus
You may want to create a repository in the GitHub Organization associated with your classroom for a variety of reasons - most likely either starter code for an assignment, or a syllabus/informational repository for all class students to view. Both can (and should) be started as template repositories in your main organization. To do so, follow the steps below.

You may not want to create template repositories until you have created a Classroom (and associated semester-specific organization). In that case, return to this section after the "Adding students to your Classroom" section.

For informational repositories like a syllabus, extra steps are required for students to view it. This isn't necessary in your "main" repository, because there shouldn't be any students there, but will be required for semester-specific repositories. However, these steps require an existing classroom, so visit the "Allowing students to access private repositories" section after you've created the prerequisite semester-specific organization and classroom.

#### Basic repository creation
1. Navigate to your organization's main page, and to the `Repositories` tab.
2. Create a `New repository` via the button in the top right.
3. Provide a suitable name, for instance, `syllabus`.
4. It is recommended to choose **Private** visibility unless you want this repository to be publicly accessible.
	- If creating a template, in almost all cases you will want to use a private repository since GitHub Classroom can access it regardless.
5. You will likely want to add a `README` file. This will make it easier to edit the repository via the GitHub web interface, but you are of course free to do things manually.

#### Marking a repository as a template
See also [GitHub's documentation on this subject](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository).

1. If not already on the main page of the repository you wish to use as a template, navigate there, then proceed to the `Settings` tab.
2. You should be on the `General` settings page - if not, navigate there with the sidebar.
3. Under the repository name field, check the `Template repository` box. 
	- GitHub will let you know if there are any issues with making the repository a template, but unless you are using Git LFS, it should be fine.
	
After this, you can use the template repository as starter code for an assignment. When creating an assignment, GitHub Classroom notes the following:

> All starter code must use a [template repository.](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-template-repository) Your starter code repository must be either in the same organization as this classroom or a public repository if elsewhere. Learn about [transferring your repositories.](https://docs.github.com/en/rest/reference/repos#transfer-a-repository)

### Creating a GitHub Classroom
Once you have created a GitHub Organization to house a classroom and associated repositories, you can then create the classroom itself. You should also create a classroom in your main organization from which you can "reuse" assignments - that is, copy them and their template code to another organization and classroom.[^1] However, you should not add any students to a classroom in your main organization - only trusted instructors and TAs.

[^1]: Previous versions of this guide recommended against creating a GitHub Classroom in your main organization - this is because I was unaware that the `Reuse assignment` feature in the assignment dashboard was capable of this functionality.

1. Navigate to [classroom.github.com/classrooms](https://classroom.github.com/classrooms).
2. Click the `+ New Classroom` icon in the top right or the boxed plus icon below.
3. Select the organization you just created (or the appropriate one, if you created multiple). Then click `Create classroom`.
	- You can also create a new organization from this menu.
	- Note that the full name of your organization may be cut off. If you have multiple organizations (as recommended) you may want to set a different icon for each to differentiate them when creating classrooms.
4. Give your classroom a humanized display name.
	- Suggested format: `[course-id] [full-course-name] [semester] 20XX`

### Adding other instructors or TAs to your Classroom
Immediately after the last step in the previous section, GitHub Classroom will prompt you to add TAs or admins to your newly created classroom. If you skip this panel, a functionally identical menu can be accessed later from the classroom dashboard, under the `TAs and Admins` tab. The steps provided are elaborated upon below.

1. Invite the TA or other instructor to your GitHub *organization*. Clicking the provided link will take you to the organization page's `People` tab, where you can invite a member by username, full name, or email address.
2. Once they accept, promote them to `Owner` status (unlike Google Docs, this does *not* remove your owner status - it is equivalent to administrator status.)
	- This can be also done from the organization page's `People` tab. A member must accept the invitation before you can change their ranking.
3. Invite them to the GitHub *classroom* using the provided URL. Copy this link and share it with your TA, but do *not* post it publicly or provide it to students. They should not be able to gain administrator status solely through accessing this link, but an abundance of caution is always best.
- If you no longer have your dashboard open, you can open it again from [classroom.github.com/classrooms](https://classroom.github.com/classrooms).

![GitHub Classroom Guide Fig1](https://github.com/rzn-example-classroom/.github/assets/16062019/7a1e959c-3ddd-43b0-b170-7947f5e491b4)


### Adding students to your Classroom
If you still have the original window open from the classroom creation, it should next prompt you to add students. Similar to before, you can access a functionally identical panel from the `Students` tab on your classroom dashboard. There are two ways to add students: via an LMS or manually. Both methods are fairly straightforward - for the former, just follow the guided wizard, and for the latter, enter students manually or upload a file with names.

![GitHub Classroom Guide Fig2](https://github.com/rzn-example-classroom/.github/assets/16062019/7a77c139-6a76-420c-ab55-464e36524992)

#### Notes about student access
- **By default, when students accept an assignment for the first time, they are invited to the organization. They should join as soon as possible.** This will allow you to provide them with syllabus information and other documents via private repositories inside your organization.
- Students cannot access the classroom panel you see on `classroom.github.com` in any capacity.
	- If they visit `classroom.github.com`, they will not see your classroom listed - the website only lists classes that *they* have created.
- The only pages related to `classroom.github.com` they can interact with are:
	- the assignment invite links provided by you or your TAs.
	- a page denoting the deadline of the assignment, if you set one (accessible via a button/link at the top of their repository's `README` file).
- All other interaction is done via the main GitHub webpage through your classroom organization and its repositories.
- Student assignment repositories are *not* located in their individual GitHub accounts, but in the account of the organization with which the classroom is associated.
	- However, if you enable *private repository forking* in your semester-specific organization (see the subsection "Forking private repositories" of "Copying, templating, and 'reusing' assignments"), students *can* fork their assignment repos to their personal profile to showcase them later. Though, this may not be desirable until after the class concludes.

### Creating assignments
Once you have imported your full student roster, you should then create an assignment for your students via the `Assignments` tab of your dashboard. If you are currently working on your "main" organization, you can ignore mention of students in this section for now, and focus on creating the assignments that you'll later copy to the semester-specific organization and classroom (see "Copying, templating, and 'reusing' assignments").

The easiest way for a student to join on their end is by accepting an assignment, where they will be prompted to pick an identifier (ID or name as declared in the roster). From there, the GitHub account they sign in with to accept the assignment will be linked to the appropriate entry in your classroom roster.

![GitHub Classroom Guide Fig3](https://github.com/rzn-example-classroom/.github/assets/16062019/f4294ff7-f853-4df3-9b96-c1b4ba2b8f57)

#### Creating an assignment
1. Under the `Assignments` tab in your classroom dashboard, click the `Create an assignment` button. 
	- This is located near the left center of the screen if you have not created an assignment, or at the top right if you have already created one or more assignments.
2. Give your assignment a descriptive yet concise title that can be easily identified by you, TAs, and students. 
	- You can use spaces in this field as this is a display name. Any spaces will be replaced by dashes in relevant repositories by default.
3. Assignment repository names are generated as follows: `[prefix]-[student username]`. By default, the prefix is a lower kebab case version of the assignment title. This can quickly become problematic if your title is long (hence the recommendation for conciseness). Thus long titles should be shortened if possible.
	- It is also recommended to use lexically ordered prefixes so the order of assignments is chronologically consistent (ex. using 01 for the first assignment and so on).
	- As of 2023-07-26, a UI update broke the custom prefix field - see [this discussion thread](https://github.com/orgs/community/discussions/60453). For now, the only possible prefix is the full title, so keep it short.
4. A deadline is technically optional, but should be set for most assignments. This can be changed later and is viewable by students via a link placed in the repository's `README.md`.
	- You can also set the deadline as a cutoff date, in which case the student will no longer be able to edit the repository after the due date. For most assignments, this is desirable.
5. You may also set the assignment as [individual](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/create-an-individual-assignment) (default) or [group](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/create-a-group-assignment). See the subsection below for more details about group assignments, as there are some idiosyncrasies.
6. **It is strongly recommended to set repository visibility to private.** This will prevent students from being able to view other students' repositories unless it is a group assignment and they are on the same team.
7. For most assignments, granting students admin rights to their repository is unnecessary. By default, repository administrators can change visibility of, transfer, or delete the repository, but these privileges can be disabled in the Organization Settings page under Member Privileges. [More information about admin privileges can be found here](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization).
8. **It is strongly recommended to provide students with starter code** via a [template repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository) (unless your assignment requires students to build the project from scratch). To do so, see the previous section "Creating template repositories".
	- Once created, you can select the new template repository as the starter code for your assignment. Student repositories will be initialized with a clone of the template repository. This is an easy way to distribute files to all students working on an assignment.
	- Note that if the template repository is updated or the starter code is changed by editing the assignment, **student repositories will not be changed retroactively**. However, new student repositories will use the new starter code.
9. You can optionally add a supported editor such as Visual Studio Code. This adds a button to the `README` (and assignment confirmation page) that opens VSCode, installs the GitHub Classroom extension, and configures the assignment locally. Students may have to sign into GitHub.
	- Note: the aforementioned extension [currently seems to be broken](https://github.com/orgs/community/discussions/47269) as of 2023-08-03. 
10. You can add automatic grading tests using GitHub Actions, which allows far easier grading, as GitHub Classroom will tell you if a submission has passed or failed tests.
11. **It is strongly recommended** to enable pull requests for feedback. This makes it very easy for instructors or TAs to provide feedback on a repository, as GitHub Classroom provides a direct link to the PR from the assignment dashboard. The PR can also be easily found from the repository (on the student side).
	- Alternatively, feedback could be provided via an issue raised on the repository, but this requires further manual intervention, whereas PR creation is mostly automatic.
	- Note that by default, you will be automatically subscribed to all changes in repositories you have push access to, which will be all student repositories. See "Managing feedback pull request notifications" for more details.

Once you have created the assignment, you should be prompted to share the invitation link with students. This is required for them to accept and access the assignment. It is recommended to distribute this through your LMS, if applicable. 

#### Group assignments
- You can set a name for the set of teams that will be created which will allow you to reuse these groups for multiple assignments or throughout a semester.
	- You can also optionally set a maximum number of group members and/or teams. 
- Note that teams are created as part of the organization housing the classroom. Thus, **unique names for each team for each assignment are strongly recommended.**
- **Teams can only be created by a student who is accepting the assignment.** Thus, the easiest way to create a team is to separately assign students to a team with a given name (ex. Team 1), and inform them that the first student to accept the assignment on their team should create the team with the assigned name. Additional team members can then find and join their team by name.
	- Alternatively, instructors or TAs can create a team by adding themselves to the student roster and accepting the assignment. This can be repeated by removing themselves from the team and re-visiting the assignment link. However, this can be tedious with multiple teams, so it's best to stick with the first method.
- Instructors and TAs *are* able to add and remove members of existing teams by clicking on the team name link on the page for the assignment, or visiting the "Teams" tab on the organization page.
	- Members can be added with the green `Add a member` button.
		- If a student is added directly this way, the assignment will be automatically accepted for them and they will be informed of their team name and corresponding repository when visiting the assignment link.
	- Members can be removed by selecting them via the checkboxes, and clicking "Remove from team..." in the dropdown menu labeled `# member(s) selected`.
		- Regardless of if the student was added manually or joined a team voluntarily, if removed and not added to another team, the student will be forced to pick a new team upon re-visiting the assignment link.
	- If a student is switched between two persistent teams (for instance, one spanning an entire semester), they will lose access to repositories associated with their previous team, and gain access to all of their new team's repositories, including those from before the student joined their new team.
- Students will be notified when they are added or removed from a team, regardless of if it was done automatically by GitHub Classroom when they accepted the assignment, or manually by an administrator.
- Teams created by GitHub Classroom are marked as secret, meaning only administrators and the members of the team can see it.
	- Students can view their teammates by navigating to the classroom organization page's `Teams` tab. They will only be able to see the teams they are currently on (including those from past assignments if they have not been removed - another good reason to have unique team names per assignment).
	- Instructors and TAs can view the teams similarly, but can also easily view which users (by username, not roster ID) have joined a team from the assignment page accessible via the classroom dashboard.

### More on assignments
#### Updating assignments
Unlike forks, repositories for assignments that are generated by GitHub Classroom cannot be updated based on upstream changes once they are created. Thus, it is strongly recommended to have the template repository finalized before distributing the assignment link to students. If you must make changes after the assignment has been disseminated, you can either delete all student repos (at the risk of destroying their work) or create a new assignment (which would allow students to manually move over their changes). Alternatively, for small changes, you could also just inform students of the changes to be made.

#### Disabling assignments
You can disable or deactivate an assignment at any time. This will prevent students from accepting or accessing the assignment. If you wish to prepare an assignment ahead of time, doing this directly after assignment creation is wise. There are two ways to enable or disable an assignment:

1. From the assignment list in your classroom dashboard, via the "Enable assignment invitation URL" checkbox: ![Disabling Assignments 1](https://github.com/rzn-example-classroom/tutorial/assets/16062019/02b33aaf-8473-4b89-8b8c-1a6befc6da3f)
2. From the assignment-specific dashboard by editing the assignment and setting it to "Active" or "Inactive" (respectively) in the dropdown: ![Disabling Assignments 2](https://github.com/rzn-example-classroom/tutorial/assets/16062019/5bb8390c-8533-4dc9-9f86-f9da031cef26) ![Disabling Assignments 3](https://github.com/rzn-example-classroom/tutorial/assets/16062019/ff11ffef-59f0-4c00-8cb2-b7a4cfbfb477)

Note that you can also view assignment status (whether it is enabled/active or disabled/inactive) from the assignment dashboard, as shown in the first image of option 2 above.

#### Deleting assignments
Assignments can be deleted from their specific dashboard, under the `Edit` dropdown. **Be warned that deleting an assignment will also delete all student repositories for that assignment**.

It appears that deletion from the main assignment list under the classroom dashboard is currently broken, as clicking "I have read and understand these effects" does nothing, whereas in the assignment dashboard, it proceeds to the deletion confirmation prompt as expected.

#### Deadline extensions
Sometimes it is necessary to provide a student with an extension on an assignment. Manual intervention in GitHub Classroom is only necessary if your assignment deadline is set as a *cutoff date*, where the student loses write access after the deadline. To give an extension, simply navigate to the assignment dashboard, click the three dots on the right of the entry of the student in question, and click "Extend deadline" as shown below:

![Disabling Assignments 3](https://github.com/rzn-example-classroom/tutorial/assets/16062019/ff11ffef-59f0-4c00-8cb2-b7a4cfbfb477)

Note that deadline extensions currently *cannot be set with a timeframe*. Once extended, the student will have write access to the repository until you revoke the extension. However, since commits are timestamped, if a student makes a commit after the extended deadline, you can manually revert the commit and grade the work as it was at the time of the deadline. Because of this, you can also evaluate late assignments without the deadline set as a cutoff date.

#### Introductory assignments
It is strongly recommended to introduce students gradually to the Git, GitHub, and GitHub Classroom ecosystem. Thus, it is a good idea to provide a simple introductory assignment related to the class syllabus or Git/GitHub fundamentals. [This introduction to Git and GitHub is strongly recommended](https://github.com/rzn-example-classroom/git-and-github-intro).[^2] It is based upon [GitHub Education's official GitHub starter course](https://github.com/education/github-starter-course), but is tailored more specifically towards student use alongside GitHub Classroom, and also focuses more on the differences between Git and GitHub. 

[^2]: Disclaimer: I made this guide, but it is tailored specifically for students getting started with GitHub Classroom, and in my opinion is better suited to that task.

##### Using the example assignment
The official course is also available as an example assignment in GitHub Classroom if you have not yet created any other assignments. The steps are a subset of those for creating your own assignment as in the previous subsection, with most of the same primary features. If you wish to use this repository as the template code for a subsequent assignment, simply search for `education/github-starter-course` when setting the assignment starter code.

#### Mobile Access
While students can accept assignments on their mobile devices, be warned that the interface may not behave as expected, especially when accepting the first assignment. At that time, students will be asked to select their name or identifier from the roster, but this menu can blank out on some mobile devices. Thus, usage of mobile devices for accepting assignments is not recommended. However, the GitHub app is quite useful for both instructors and students to provide, receive, and manage feedback via pull request. Note that LaTeX formatting does not currently work on mobile, but Markdown codeblocks do.

#### Managing feedback pull request notifications
The default notification settings for a GitHub account automatically subscribe you to any repository you have push access to. Assuming you are an administrator of your classroom organization, this will likely result in you (and any other admin) receiving an email each time a student repository is created or committed to. Obviously this can quickly become a severe annoyance. Thus, it is recommended to disable the "Automatically watch repositories" option in your account's Notifications settings: 

![GitHub Disabling Watch Notifications](https://github.com/rzn-example-classroom/tutorial/assets/16062019/cc0c58be-4897-4f92-9efd-a8b0dff5d497)


To unwatch repositories that may have been watched before you disabled this setting, scroll down slightly and click "View watched repositories" as shown below.

![GitHub Disabling Watch Notifications 2](https://github.com/rzn-example-classroom/tutorial/assets/16062019/e3feeddc-595d-4d17-9391-5364e5b0317f)


Then, once you click "Unwatch all" you can select an *owner* (including an organization) to unwatch repositories from. By selecting the organization associated with your classroom, you can unsubscribe from any student repositories you may be subscribed to. This will prevent you from receiving an email for every change made in each student repository.

![GitHub Disabling Watch Notifications 3](https://github.com/rzn-example-classroom/tutorial/assets/16062019/354dc301-6f08-4b5e-a686-f252eb8ed01a)


While messages for every change are excessive and unnecessary, your students should still be able to attract your attention. The best way for them to do this is by *mentioning* you in the feedback pull request. This is accessible from the student repository's `Pull requests` tab. There, a student can make a comment mentioning your username (ex. `@RyzenFromFire`). 

To learn more about managing notifications, visit [GitHub's documentation here](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications). The email notifications are easily filterable via various header data. See the documentation for more details.

### Assignment Submissions
- **There is no "submit button" in GitHub Classroom.** Assignments will appear as "submitted" to the instructor or TAs once a commit has been pushed to the repository.
	- Thus, instructors and TAs should be careful to avoid prematurely grading a student's work. Waiting until the deadline has passed is the best way to do so. 
	- Alternatively, you can ask students to specify in their last commit that this is the final version of their assignment.
		- This may be useful especially in cases where no assignment deadline is set.
	- Note that the commit does not have to be from the owner of the repository - any admin or member with access to the student's repository (which should only be the student, unless it is a group project) can push a commit and "submit" the assignment.

### Grading Assignments
In the assignment page, the green Download button allows instructors or TAs to download auto-grading results. It also provides a command to download all student repositories using [Classroom CLI](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/using-github-classroom-with-github-cli). Instructions on setting up GitHub CLI and Classroom CLI are in the subsection below.

Note that per [this discussion thread](https://github.com/orgs/community/discussions/55285), the CLI currently does not support overwriting existing student repositories or downloading new ones when any already exist in a given directory. You can update repositories individually, as they are fully functional, but this can quickly become tedious. Thus, it is recommended to wait until after the deadline before downloading repositories. Manual updating may be reserved for cases of deadline extension or similar.

#### Setting up GitHub Classroom CLI
First, install the GitHub CLI with the appropriate command for your OS. Some examples are given below, but [the full array of options is available here](https://github.com/cli/cli#installation).

```shell
# Windows
winget install --id GitHub.cli

# MacOS
brew install gh
```

Linux instructions vary by distribution, and there are multiple methods both officially and unofficially supported, [available here](https://github.com/cli/cli/blob/trunk/docs/install_linux.md). 

Once installed, restart the shell. Then, run `gh auth login`. The example below is for Windows, but will be similar for other platforms.

```
C:\Users\user\Desktop\Code\Projects\GHClassroom>gh auth login
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: XXXX-XXXX
Press Enter to open github.com in your browser...
✓ Authentication complete.
- gh config set -h github.com git_protocol https
✓ Configured git protocol
✓ Logged in as User
```

Then, install the GitHub Classroom extension to the GitHub CLI using `gh extension install github/gh-classroom`:

```
C:\Users\User\Desktop\Code\Projects\GHClassroom>gh extension install github/gh-classroom
✓ Installed extension github/gh-classroom
```

Finally, your assignment dashboard will provide a command you can paste into your terminal of choice to clone all student assignment repositories to your working directory (be sure to `cd` to a suitable directory first):

![[GitHub Classroom DL Student Repos Command.png]]

After the download completes, a folder with a name corresponding to the assignment will be created containing all student repositories, which you can then grade.

Further instructions available [here](https://github.com/cli/cli#installation) and [here](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/using-github-classroom-with-github-cli). 

### Copying, templating, and 'reusing' assignments
While individual repositories can be marked as a template, entire organizations or classrooms cannot be. However, a feature in GitHub Classroom makes this problem easier to solve. By creating a Classroom in your main organization, you can create the primary working version of your assignments there, and copy them to other organizations and classrooms using the "Reuse assignment" feature. 

At this point, you need at least two organizations: a source (likely your main organization) and a destination (your semester-specific organization). If you need to create another organization, return to the "Creating a GitHub Organization" section for instructions. Once you've created your assignments in the source organization, for each one, do the following:

1. Navigate to the assignment-specific dashboard (from the classroom assignment list).
2. In the top right, click `Edit`, then `Reuse assignment`. ![Reuse assignment 1](https://github.com/rzn-example-classroom/tutorial/assets/16062019/ef9fcbb8-453f-4fca-8f93-835426125d8c)
3. You will then be prompted to choose an organization and classroom to copy to. You cannot copy the assignment to the source classroom. 
	- You can copy it to another classroom in the same organization, but you shouldn't have more than one classroom in the same organization anyways. 
		
		![Reuse assignment 2](https://github.com/rzn-example-classroom/tutorial/assets/16062019/d7bc3445-72a8-4b2c-82d3-1d925e786bf9)
4. You will be taken to the destination classroom and assignment dashboard. It may take some time for the assignment and template repository to be copied, and you will likely need to refresh the page to see updates. 

#### Forking private repositories
While the `Reuse assignment` feature of GitHub Classroom bypasses this requirement, other (template) repositories that are not associated with an assignment must be copied manually.

1. Ensure you have a source and destination organization. 
2. In the source organization (the one you wish to copy repos from), navigate to the `Settings` tab.
3. Under the `Access` submenu on the left, navigate to `Member privileges`.
4. Scroll down to `Repository forking`. Check the box to allow forking private repositories, then `Save`.
5. If the destination organization is your "main" organization, repeat steps 2-4 for it as well. This will be necessary when you want to copy repositories from it for future semesters.
6. Now, you'll copy the repositories from the source organization to the destination organization. For each repository you wish to copy, you will need to repeat the following steps (7-10).
7. Navigate to the main page of a (template) repository in the source organization.
8. Create a new fork in the top right. This will take you to a new page where you can select a name (by default, the same as the original repository). 
	- If the upstream repo has any branches other than `main`, make sure to uncheck the box on the bottom if you want them to be copied.
9. **Change the `Owner` of the new fork to the destination organization**. By default, GitHub will fork the repo to your personal account. Click the name/dropdown to change this, and select the appropriate organization. 
	- Be careful when selecting the organization if you change the repository name. You can clone to the same organization if you do so (which may be desirable, but not in this case).
10. Wait for the fork to complete. The page should load automatically - if not, refresh.

Repeat steps 7-10 for each repository you wish to copy. Note that assignment template repositories can also be copied manually this way, but this is not recommended.[^3]

[^3]: Previous versions of this guide used this method to copy repositories from the main organization, but the `Reuse assignment` feature makes it much easier to do so. Thus, this is no longer recommended for template repositories associated with an assignment.

### Allowing students to access private repositories
Assuming you are restricting visibility of student assignments and other class materials to their respective domains, you may want to create certain private repositories that should be published to the class only but not the entire internet. For instance, a syllabus, assignment or report formatting guidelines, example code, or some common code usable across multiple assignments. Again, assuming you are *not* setting assignment visibility to public, you will need to do some more work to allow students to view these resources. 

Note: be careful not to set the organizational base permission to `Read` as a means of achieving this. As mentioned previously, that will allow students to view *all* private repositories, which means other students' work *cannot* be hidden from them. This setting should be set to `No permission`, so that students can only access repositories either created for them by GitHub Classroom or those which they or a team they are on has been explicitly granted permission by an administrator or owner (i.e. instructor or TA).

The correct way of allowing students to view a specific private repository while also keeping them from viewing *all* private repositories, is to add them to a **team**, which can be given read access to a particular repository. Fortunately, creating a team of all students is only necessary once - it can be reused for subsequent repositories or assignments.

As previously mentioned, by default, when students accept an assignment for the first time, they are invited to the organization. Until they accept the invitation, they are listed as an "outside collaborator" and are given access only to repositories corresponding to assignments they accept. It is more difficult to add this type of member to teams that are not created through GitHub Classroom.

There are two ways of doing this: one is very tedious, while the other is rather hacky, but much quicker. The former requires students to join the GitHub organization, while the latter allows them to remain as outside collaborators. However, if you're using private repositories for everything, it should not make any functional difference. 

#### The quick and hacky way
##### Make GitHub Classroom and the students do the work for you
1. Navigate to your classroom dashboard, then the `Assignments` tab.
2. Create a new assignment with the following characteristics (see the "Creating assignments" section):
	- Title: `Syllabus` or other as appropriate.
	- Deadline: As desired. If you want to make students commit and push something to submit this assignment, modify the assignment description/starter code as such. This tutorial will assume no deadline.
	- **Group Assignment**
		- Name the set of teams "All Students" or similar (it may be wise to avoid doubling the "Students" name.
		- **Set maximum teams to 1.**
	- Visibility: Private
	- No admin access
	- Unless you decided to add a submission requirement, do not add any starter code, autograding, or feedback.
3. **Before distributing this link to the students,** copy the link to the assignment and go there with your own GitHub account (which should be an organization owner).
4. Create a new team with your desired name (`Students`).
	- If you already created a team with this name, GitHub Classroom will fail to create the team. Either delete the existing team or choose a different name.
	- You can optionally remove yourself from the team later, as described in the "Group assignments" subsection of the "Creating assignments" section. A team *can* have zero members, so that is not a concern.
5. Accept the assignment. Refresh the page if necessary, until the repository link appears. Since only one team is allowed, only one repository should be created. Navigate to the repository.
6. Unless you want students to "sign in" or attest to reading the syllabus somehow, do the following:
	- Navigate to the repository `Settings`.
	- Go to the `Collaborators and teams` panel.
	- For the `Students` team, set the role to `Read` instead of `Write`.
7. Optional, but recommended: Return to the organization homepage. Navigate to the Teams, then Students, then Settings for the Students team. Change visibility to Visible.
8. Follow steps 7 through 11 of the next subsection (the alternate method) to add the `Students` team to the `syllabus` repository (the one *you* created to publish to students, *not* `syllabus-students`, the repo GitHub Classroom created for the assignment).
9. **Finally, provide students with the assignment link created earlier.** They will be forced to join your existing team, since the team limit is set to 1. They also cannot rename the team. Students will now be given access to the `syllabus` repository as they join.

Ultimately, this is a more distributed method of student team creation, which distributes the work among the students instead of forcing the instructor or TA to do everything.

##### Additional Notes
Optionally, instead of creating a separate `syllabus` repository and adding students to it, you can make your original syllabus a template repository and use it as starter code for the assignment. Then, you can manually modify the student team permissions to read-only in the repository settings. This may reduce confusion, however, Classroom may change your repository in unexpected ways. It seems that students joining does not reset permissions, but other problems could arise. Furthermore, deleting the assignment **will** remove the repository generated by Classroom. If you do not pursue this option, you can also delete the `syllabus-students` repository after all students have joined the team, to reduce repository clutter.

#### The tedious way
##### Creating a team and adding students manually
First, you'll likely want to have all students accept an assignment to get them registered in the classroom. They 

After students join the organization, you will need to gather them into a **team**, which you can then give read access to the repository you just created.

1. Have all students register in the classroom. The easiest way to do this is by creating and distributing the link to an introductory assignment. Once they accept, they should automatically receive an invitation to the repository - **have all students join the organization as soon as possible.** You will not be able to add them to the team manually until they do.
2. Navigate to your organization's main page, and to the `Teams` tab.
3. Create a `New team` via the green button on the right.
4. Name the team `Students` or similar.
5. Leave the other options as default: visibility - visible and team notifications enabled.
6. If not already there, navigate from your organization page to the `Teams` tab, then enter the `Students` team.
7. From here, you will need to add each student individually using the green `Add a member` button in the top right.
8. Next, navigate back to the repository you created (ex. `syllabus`), then its `Settings` tab.
9. On the sidebar, switch to the `Collaborators and teams` page.
10. Under the `Manage access` header, click the green `Add teams` button and add the `Students` team (you will have to start typing the name before it autofills).
11. Assign the `Students` team the default `Read` role/permission.
12. The students added to the team will now be able to view the `syllabus` repository. For additional repositories, only steps 7 through 11 of this subsection are needed, since the Students team already exists.

### Supplementary Materials
- https://www.youtube.com/playlist?list=PLIRjfNq867bewk3ZGV6Z7a16YDNRCpK3u
- https://github.com/jfiksel/github-classroom-for-teachers
- https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/using-github-classroom-with-github-cli
- https://faculty-web.msoe.edu/hasker/resources/github-classroom.html

## For Students
[A full guide for students providing an introduction to Git, GitHub, and their use with GitHub Classroom can be found here](https://github.com/rzn-example-classroom/git-and-github-intro). It includes a video on how to accept and complete their first assignment.
