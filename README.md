# Software Engineer (Laravel) Assessment

**Already Developed on Laravel?**  If you have already developed a project or plugin or theme on Laravel, you can use it as a work sample. Just make sure your code is complaint with the rules of the game.

As BRT is mainly into Laravel, plugins, customization, migrations & more, we have plenty of interesting work in every aspect of Laravel. Keeping that in mind, we have created a challenge for Laravel. Choose one which you like more!

## Rules of the Game
-   Some challenges have multiple parts. You must complete all parts.
-   Use of Google is allowed & encouraged (However, you are not allowed use readymade project/repository).  😉
-   You are also free to use 3rd party libraries. But please mention if you use them.

### Web Hosting for Demo purpose

For all coding challenges below, you will need a web host to showcase your working demo. You can use a free web hosting for your demo. Microsoft Azure, Google Cloud, Amazon AWS – all offers free trial plan. You can use any of these cloud providers or simply any free web hosting.


### Coding Guidelines

Before you choose a challenge, please note down our common minimum requirements applicable to all challenges.

1.  **UI Framework**  - Use Bootstrap version 5 for CSS/JS. Make sure what you create looks nice!
2.  **Responsive**  - Your code must work on mobile devices like iPhone/Android.
3.  **Code Organisation**  - All 3rd party codes, library must be inside  `public`  folder. No unwanted files e.g. IDE files, temporary files should be committed on git-repo.  _(Hint: Write a nice  `.gitignore`)_
4.  **Coding Standard**  - Your code must pass Laravel coding standard. You can use PHP Code Sniffer and JSHint on localhost. Additionally, you can should configure  [scrutinizer-ci](https://scrutinizer-ci.com/)  so your code quality can be seen easily.
5.  **Unit Testing**  - Submissions without unit tests will not be accepted. 
6. **Github Readme**  - Write a nice Github Readme using markdown syntax. Make sure you include demo link and links to libraries used in readme.

Failure to meet any of above guidelines will result in disqualification.

## List of Challenges

We have two kinds of challenges for Laravel:

1.  Laravel Ticket System
2.  Laravel Plugin

You need to complete any one. If you wish to complete two, we won't mind. 😉

### Challenge-1: Laravel Ticket System
#### The Task
A system to manage support tickets. customers register as users and can create tickets, then admins assign them to agents, and all parties can view ticket statuses. On each status update, respective user and agent and admin should get the email notification.

A few screenshots from the example solution:
![Laravel support tickets 01](https://laraveldaily.com/uploads/2022/11/laravel-support-tickets-01.png)
![Laravel support tickets 02](https://laraveldaily.com/uploads/2022/11/laravel-support-tickets-02.png)

#### Database structure
Every ticket needs to have:

-   title (required)
-   text description (required)
-   multiple files attached (optional)
-   priority (choose from a few options)
-   status (choose from a few options like open/closed)
-   assigned user agent (foreign key to users table)
-   multiple categories (belongsToMany relationship with categories table)
-   multiple labels (belongsToMany relationship with labels table)

#### Auth
There should be login and register functionality, they may come from starter kit like Laravel Breeze or other one of your choice.

Every user needs to have one of three roles:

-   Regular user (default)
-   Agent
-   Administrator

New users can register and they are assigned Regular articles role.

There should be one Administration user created with database seeds.

After registration or login, users get inside the system which would look like a typical adminpanel to manage data: menus, tables, CRUDs for administrator.

#### Regular users: manage THEIR tickets
After registration/login, user sees the only menu item "Tickets" with a table of tickets only created by themselves.

Table of tickets needs to have dropdown filters: by status, priority and category.

They can add a new ticket, but can't edit/delete tickets.

They can click the ticket title in the table to open the page to see more details and ticket activity log and comments, also may add a comment there (more on that later).

#### Agent users: manage THEIR tickets
Similar to regular users, agents see only tickets, and only their tickets, but "their" has different meaning - not that they created the tickets, but are assigned to them (by admin, more on that later).

They can edit tickets and add comments.

#### Admin users: manage everything
Admins see not only tickets table, but also can view more menu items:

-   Dashboard with the amount of tickets per status (total / open / closed, etc.)
-   Manage Labels, Categories, Priorities and Users, in CRUD way

Also, when editing the ticket, admins can assign Agent user to it - other users shouldn't see that field.

Also, admins should see the menu item called "Logs" which lists all changes that happened to all tickets, like history: who created/updated the ticket and when.

#### Ticket Comments
After clicking on ticket, any user can get to its page, and there should be a form to add a comment, and that page shows the list of comments, like on a typical blogpost page.

#### Email Notifications
When the new ticket is created, admin should get an email with the link to the Edit form of the ticket.

For visual design, you can use any design template, starter kit, or custom design.

---
### Challenge-2: Laravel Plugin (Laravel Audit Trail Plugin)

#### The Task
The Laravel Audit Trail plugin provides an easy way to track and monitor changes made to your application's data. It helps you keep a detailed record of all modifications, providing accountability, traceability, and compliance with auditing requirements.

#### Features
1.  Database Change Tracking: The plugin hooks into Laravel's database query events and captures any changes made to the data. It records the before and after values, the user who made the change, and the timestamp of the modification.
    
2.  Model Integration: The plugin integrates seamlessly with Laravel's Eloquent ORM. You can define which models and fields should be audited by adding a simple configuration to your model classes.
    
3.  User Tracking: The plugin automatically captures the authenticated user responsible for each change, making it easy to track who made specific modifications.
    
4.  Flexible Configuration: The plugin allows you to configure the level of auditing required for each model and field. You can choose to track all changes or only specific types of modifications, such as create, update, or delete actions.
    
5.  Audit Log Viewer: The plugin provides a user-friendly interface to view and search the audit logs. You can easily filter the logs by user, model, date range, or specific fields, making it convenient to review and analyze the history of changes.
    
6.  Notifications: The plugin supports notifications to alert administrators or specific users whenever certain predefined events occur, such as critical changes or unauthorized access attempts.
    
7.  Data Export: The plugin allows you to export audit logs to various formats, such as CSV or JSON, for further analysis or integration with external systems.

## Challenge Completed?
Share the Demo working link and the GitHub repository link with us.
