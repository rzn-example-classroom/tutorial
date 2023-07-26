# Getting Started with GitHub Classroom
## For Instructors
### Why use GitHub Classroom?
GitHub is an industry standard platform for repository management, and Git is likewise the standard in version control. Introducing students to Git and GitHub as soon as possible will allow them to better track their own projects, work more effectively on group programming projects associated with classes, and better prepare them for software development in industry. 

From an instructor perspective, GitHub classroom makes distributing, monitoring, collecting, and grading programming assignments much easier. By creating a template repository for an assignment, you can create a link that will allow each student to clone this repository, work on a private version of it, and turn it in when complete. Depending on the assignment, testing and grading can even be partially or fully automated. Furthermore, applying for education benefits allows students to use GitHub Codespaces (which provides online development environments for assignments). Overall, leveraging an environment designed for code makes managing computer science or engineering assignments far smoother.

### Note about these instructions
The student instructions are designed to correspond directly to the results of the these instructions. If you change something here, you will likely need to update the information you provide your students.

### Your GitHub Account
If you do not already have an existing GitHub account, you will first need to [sign up](https://github.com/signup) for one. Even if you have an existing professional account, if you intend to use GitHub classroom for more than one class or for more than one semester, you may want to create a new account since having a separate organization is strongly recommended for each class and for each semester each class is offered. If you have existing organizations, your account may become crowded.

### Creating a GitHub Organization
#### Note about organizations
It is strongly recommended to create a separate GitHub Organization for each class and for each semester the class is offered. This makes it far easier to keep track of which assignments belong to which class, and to better manage student assignments, as there will be a repository added to the organization for *each* student for *each* assignment. More importantly, because TAs must be added as an administrator to the organization that they are to assist with, therefore academic issues can arise if the TA is added as an admin to an organization containing a class and assignments they have not yet taken. However, multiple class sections of the same class during the same semester should be grouped together unless you have a good reason not to do so. Furthermore, it is also advisable to create a "template" organization holding the latest version of class files and assignments which you can copy or fork to create a new semester's classroom organization.

#### Steps
1. Go to [github.com/settings/organizations](https://github.com/settings/organizations).
2. At the top right, select `New organization`.
	- Alternatively, you can also transform an existing account into an organization if you are not a member of any other organization, but this is generally not recommended unless you created a new account with an email specifically for that organization.
3. Select the `Free` plan.
4. Give your organization a unique and appropriate name, and provide a contact email (the email associated with your existing GitHub account will do).
	- An example name format is: `[university-abbreviation]-[course-id]-20XX`
5. You can choose whether to declare the GitHub organization as belonging to either your personal account or a business or institution. 
	- The choice makes no functional difference, but it does make a legal difference in the form of the Terms of Service agreement used - read carefully if you select the latter option. 
	- If you are uncertain, choose the personal option - you can [upgrade to the corporate ToS](https://docs.github.com/en/organizations/managing-organization-settings/upgrading-to-the-corporate-terms-of-service) later, but currently there does not appear to be a way to downgrade to standard ToS or change the company name. However, the corporation name is not published anywhere on the organization page unless you manually add it, nor is any confirmation required from the corporate side for that option.
6. For now, you can skip adding members unless you already have the account details of any other instructors or TAs you would like to add. This is covered in more detail in a later section.

### Creating a GitHub Classroom
Once you have created a GitHub Organization to house the classroom and associated repositories, you can then create the classroom itself.

1. Navigate to [classroom.github.com/classrooms](https://classroom.github.com/classrooms).
2. Click the `+ New Classroom` icon in the top right or the boxed plus icon below.
3. Select the organization you just created (or the appropriate one, if you created multiple). Then click `Create classroom`.
	- You can also create a new organization from this menu.
4. Give your classroom a humanized display name.
	- Suggested format: `[course-id] [full-course-name] 20XX`

### Adding TAs to your Classroom
Immediately after the previous step in the previous section, GitHub Classroom will prompt you to add TAs or admins to your newly created classroom. If you skip this panel, a fuinc identical menu can be accessed later from the classroom dashboard, under the `TAs and Admins` tab. The steps provided are elaborated upon below.

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

### Creating assignments
Once you have imported your full student roster, you should then create an assignment for your students via the `Assignments` tab of your dashboard. The easiest way for a student to join on their end is by accepting an assignment, where they will be prompted to pick an indentifier (ID or name as declared in the roster). From there, the GitHub account they sign in with to accept the assignment will be linked to the appropriate entry in your classroom roster.

![GitHub Classroom Guide Fig3](https://github.com/rzn-example-classroom/.github/assets/16062019/f4294ff7-f853-4df3-9b96-c1b4ba2b8f57)

#### Creating an assignment
1. Under the `Assignments` tab in your classroom dashboard, click the `Create an assignment` button. 
	- This is located near the left center of the screen if you have not created an assignment, or at the top right if you have already created one or more assignments.
2. Give your assignment a descriptive yet concise title that can be easily identified by you, TAs, and students. 
	- You can use spaces in this field as this is a display name. Any spaces will be replaced by dashes in relevant repositories by default.
3. Assignment repository names are generated as follows: `[prefix]-[student username]`. By default, the prefix is a lower kebab case version of the assignment title. This can quickly become problematic if your title is long (hence the recommendation for conciseness). Thus long titles should be shortened if possible.
	- It is also recommended to use lexically ordered prefixes so the order of assignments is chronologically consistent (ex. using 01 for the first assignment and so on).
	- As of 2023-07-26, a UI update broke the custom prefix field - see [this discussion thread](https://github.com/orgs/community/discussions/60453). Thus, the only plausible prefix is the full title, so keep it short for now.
4. A deadline is technically optional, but should be set for most assignments. This can be changed later and is viewable by students via a link placed in the repository's `README.md`.
	- You can also set the deadline as a cutoff date, in which case the student will no longer be able to edit the repository after the due date. For most assignments, this is desirable.
5. You may also set the assignment as [individual](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/create-an-individual-assignment) (default) or [group](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/create-a-group-assignment). See the subsection below for more details about group assignments, as there are some idiosyncrasies.
6. **It is strongly recommended to set repository visibility to private.** This will prevent students from being able to view other students' repositories unless it is a group assignment and they are on the same team.
7. For most assignments, granting students admin rights to their repository is unnecessary. [More information about admin privileges can be found here](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization).
8. **It is strongly recommended to provide students with starter code** via a [template repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository) from your classroom organization (unless your assignment requires students to build the project from scratch). To do so, follow the instructions on [this page](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository). Once created, you can select the new template repository as the starter code for your assignment. Student repositories will be initialized with a clone of the template repository. This is an easy way to distribute files to all students working on an assignment.
9. You can optionally add a supported editor such as Visual Studio Code. This adds a button to the README (and assignment confirmation page) that opens VSCode, installs the GitHub Classroom extension, and configures the assignment locally. Students may have to sign into GitHub.
	- Note: I wasn't quite able to get this to work - YMMV.
10. Finally, you can add automatic grading tests using GitHub Actions, or enable pull requests for feedback if desired. The former option allows far easier grading as GitHub Classroom will tell you if a submission has passed or failed tests, while the latter option allows better feedback options. Feedback could also be provided via an issue raised on the repository.

#### Using the example assignment
GitHub Classroom also provides a starter assignment for Git and GitHub fundamentals - if your students have little to no experience with either, this can be a useful first assignment to get them used to the ecosystem. The steps are a subset of those for creating your own assignment as in the previous subsection, with most of the same primary features. However, this assignment can only be created from GitHub Classroom when you have not created any other assignments. However, can be manually recreated.

#### Group assignments
- You can set a name for the set of teams that will be created which will allow you to reuse these groups for multiple assignments or throughout a semester.
	- You can also optionally set a maximum number of group members and/or teams. 
- Note that teams are created as part of the organization housing the classroom - so unique names are a good idea if you intend to have different teams for each assignment.
- **Teams can only be created by a student who is accepting the assignment.**
	- However, instructors or TAs can add themselves to the student roster, accept the assignment, and create a team that way. This can be repeated by removing themselves from the team and re-visiting the assignment link.
- Instructors and TAs *are* able to add and remove members of existing teams by clicking on the team name link on the page for the assignment, or visiting the "Teams" tab on the organization page.
	- Members can be added with the green `Add a member` button.
		- If a student is added directly this way, the assignment will be automatically accepted for them and they will be informed of their team name and corresponding repository when visiting the assignment link.
	- Members can be removed by selecting them via the checkboxes, and clicking "Remove from team..." in the dropdown menu labeled `# member(s) selected`.
		- Regardless of if the student was added manually or joined a team voluntarily, if removed and not added to another team, the student will be forced to pick a new team upon re-visiting the assignment link.
- Students will be notified when they are added or removed from a team, regardless of if it was done automatically by GitHub Classroom when they accepted the assignment, or manually by an administrator.
- Teams created by GitHub Classroom are marked as secret, meaning only administrators and the members of the team can see it.
	- Students can view their teammates by navigating to the classroom organization page's `Teams` tab. They will only be able to see the teams they are currently on (including those from past assignments if they have not been removed - another good reason to have unique team names per assignment).
	- Instructors and TAs can view the teams similarly, but can also easily view which users (by username, not roster ID) have joined a team from the assignment page accessible via the classroom dashboard.

### Assignment Submissions
- **There is no "submit button" in GitHub Classroom.** Assignments will appear as "submitted" to the instructor or TAs once a commit has been pushed to the repository.
	- Thus, instructors and TAs should be careful to avoid prematurely grading a student's work. Waiting until the deadline has passed is the best way to do so. Otherwise, ask students to specify in their last commit that this is the final version, but this is not recommended.
	- Note that the commit does not have to be from the owner of the repository - any admin or member with access to the student's repository (which should only be the student, unless it is a group project) can push a commit and "submit" the assignment.

### Grading Assignments
In the assignment page, the green Download button allows instructors or TAs to download auto-grading results. It also provides a command to download all student repositories using [Classroom CLI](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/using-github-classroom-with-github-cli). Instructions on setting up GitHub CLI and Classroom CLI are available at [this link](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/using-github-classroom-with-github-cli). Note that per [this discussion thread](https://github.com/orgs/community/discussions/55285), the CLI currently does not support overwriting existing student repositories or downloading new ones when any already exist in a given directory.

### Creating a repository in your organization
You may want to create a repository in the GitHub Organization associated with your classroom for a variety of reasons - most likely either a template repository for an assignment, or a syllabus/informational repository for all class students to view. The basic steps here are applicable to both, but this section will focus primarily on the latter, as there are certain requirements to do so.

#### Basic repository creation
1. Navigate to your organization's main page, and to the `Repositories` tab.
2. Create a `New repository` via the button in the top right.
3. Provide a suitable name, for instance, `syllabus`.
4. It is recommended to choose **Private** visibility unless you want this repository to be publicly accessible.
	- If creating a template, in almost all cases you will want to use a private repository since GitHub Classroom can access it regardless.
5. You will likely want to add a `README` file. This will make it easier to edit the repository via the GitHub web interface, but you are of course free to do things manually.

### Allowing students to access your new repository
Assuming you are creating a syllabus or other document/repository that should be published to the class only but not the entire internet, you will need to do some more work to allow students to view it. As previously mentioned, by default, when students accept an assignment for the first time, they are invited to the organization. Until they accept the invitation, they are listed as an "outside collaborator" and are given access only to repositories corresponding to assignments they accept. It is more difficult to add this type of member to teams that are not created through GitHub Classroom. Thus, you should **encourage all students to join the organization as soon as possible.**

After students join the organization, you will need to gather them into a **team**, which you can then give read access to the repository you just created. There are two ways to accomplish this. One is very tedious and the other is rather hacky, but much quicker.

#### The quick and hacky way
##### Make GitHub Classroom and the students do the work for you
1. Navigate to your classroom dashboard, then the `Assignments` tab.
2. Create a new assignment with the following characteristics (see the previous section on creating an assignment)
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
	- You can optionally remove yourself from the team later, as described in the previous section. A team *can* have zero members, so that is not a concern.
5. Accept the assignment. Refresh the page if necessary, until the repository link appears. Since only one team is allowed, only one repository should be created. Navigate to the repository.
6. Unless you want students to "sign in" or attest to reading the syllabus somehow, do the following:
	- Navigate to the repository `Settings`.
	- Go to the `Collaborators and teams` panel.
	- For the `Students` team, set the role to `Read` instead of `Write`.
7. Optional, but recommended: Return to the organization homepage. Navigate to the Teams, then Students, then Settings for the Students team. Change visibility to Visible.
8. Follow steps 7 through 11 of the next subsection (the alternate method) to add the `Students` team to the `syllabus` repository (the one *you* created to publish to students, *not* `syllabus-students`, the repo GitHub Classroom created for the assignment).
9. **Finally, provide students with the assignment link created earlier.** They will be forced to join your existing team, since the team limit is set to 1. They also cannot rename the team. Students will now be given access to the `syllabus` repository as they join.
	- Optionally, instead of creating a separate `syllabus` repository and adding students to it, you can modify the repository created by GitHub Classroom to suit your needs and/or make a template syllabus repository. This may reduce confusion, however, there is the chance that Classroom will change your repository in unexpected ways. Furthermore, deleting the original assignment may also remove the repository generated by Classroom.
	- If you do not pursue the option above, you can also delete the `syllabus-students` repository after all students have joined the team, to reduce repository clutter.

#### The tedious way
##### Creating a team and adding students manually
1. Navigate to your organization's main page, and to the `Teams` tab.
2. Create a `New team` via the green button on the right.
3. Name the team `Students` or similar.
4. Leave the other options as default: visibility - visible and team notifications enabled.
5. If not already there, navigate from your organization page to the `Teams` tab, then enter the `Students` team.
6. From here, you will need to add each student individually using the green `Add a member` button in the top right.
7. Next, navigate back to the repository you created (ex. `syllabus`), then its `Settings` tab.
8. On the sidebar, switch to the `Collaborators and teams` page.
9. Under the `Manage access` header, click the green `Add teams` button and add the `Students` team (you will have to start typing the name before it autofills).
10. Assign the `Students` team the default `Read` role/permission.
11. The students added to the team will now be able to view the `syllabus` repository. For additional repositories, only steps 7 through 11 of this subsection are needed.

### Supplementary Materials
- https://www.youtube.com/playlist?list=PLIRjfNq867bewk3ZGV6Z7a16YDNRCpK3u
- https://github.com/jfiksel/github-classroom-for-teachers
- https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/using-github-classroom-with-github-cli

## For Students
### Your GitHub account
- It is recommended to create a GitHub account using your university email or a professional email incorporating your name.
	- You can also use an existing account, but this may make it more difficult for instructors to identify you.

### Joining your classroom's GitHub Organization
- Your primary interaction with the class will be through its GitHub Organization.
	- This is where the course syllabus and/or other pertinent information will be located.
	- This is also where you can find your copy of the repository for assignments you have accepted.

### Accepting assignments
- Your instructor will provide you with a link to each assignment via one of the following mediums:
	- your class's GitHub Organization
	- your learning management system (Canvas, Moodle, Google Classroom, etc.)
	- email

### Submitting assignments
- **There is no "submit button" in GitHub Classroom.** Assignments will appear as "submitted" to your instructor or TA(s) once a commit has been pushed to the repository.
	- Thus, remember to save your work by creating and pushing commits often. Make sure to use a descriptive message.

### Supplementary Resources
- https://www.youtube.com/watch?v=jXpT8eOzzCM
- https://www.youtube.com/watch?v=ObaFRGp_Eko
- https://github.com/jfiksel/github-classroom-for-students
