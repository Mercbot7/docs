Roles and Permissions
=====================

There are different ways to access and interact with playbooks, and access is controlled in the System Console in the form of permissions. Permissions can be granted in a variety of ways, to allow for different combinations of access, visibility, and roles. Two permission schemes are provided in Mattermost:

* **System Scheme:** Applies permissions universally across all teams, channels, and playbooks.
* **Team Override Schemes:** Allow admins to customize permissions for each team (available in Mattermost Enterprise and Professional).

You can set the default permissions granted to System Admins, Team Admins, Channel Admins, Playbook Admins, Guests (if enabled), and All Members. The permissions granted in the System Scheme apply system-wide, meaning:

* **Guests:** If Guest Accounts are enabled, permissions apply to guest users in all channels, in all teams.
* **All Members:** Permissions apply to all members, including Admins, in all channels, in all teams.
* **Channel Administrators:** Permissions apply to all Channel Admins in all channels, in all teams.
* **Playbook Admins:** Permissions apply to all Playbook Admins in all channels, in all teams.
* **Team Administrators:** Permissions apply to all Team Admins, in all teams.

For more information about System and Team Override Schemes, refer to the `Advanced Permissions <https://docs.mattermost.com/onboard/advanced-permissions.html>`__ documentation.

In the context of Playbooks, members are assigned a role and based on the selected permissions, this determines how they interact with Playbooks. A member can be a member of one playbook, and an admin of another. This allows for granular permissions across teams and departments.

.. note::

  Permissions are applied across Playbooks as a whole, so it's important to set your roles up first before editing permissions. To ensure that you don't lose access to playbooks, navigate to the playbook you're a member of. Select the **Manage Access** icon and change your role from **Member** to **Admin** 

Playbook roles
---------------

**Member**

In the context of Playbooks, members are users of Mattermost who belong to a playbook or are a Playbook Admin.

**Participant**

In the context of Playbooks, participants belong to or take part in a run. They can be a member or a Playbook Admin.

**Playbook Admin**

In the context of Playbooks, Playbook Admins are also members, and may have elevated permissions to change playbook and run visibility as well as functional settings. They do not have access to the System Console and their privileges are managed by the System Admin. Members need to be promoted to the role from within Playbooks. The Playbook Admin role is applied per playbook.

Playbooks permissions
---------------------

The default Playbooks settings are completely open which enable all members to participate in runs, edit playbooks, view runs and playbooks, remove other members from runs, edit actions, and make other changes. Permissions provide better control over confidential runs and playbooks, as well as member management.

Create read-only playbooks
~~~~~~~~~~~~~~~~~~~~~~~~~~

In the following example, only Playbook Admins can edit playbooks. Team members can view Public and Private playbooks and runs, but can't edit playbooks, check off tasks, or remove members from runs. They also can't create Public or Private playbooks.

1. Go to **System Console > User Management > Permissions**.
2. In the **All Members** section, uncheck **Manage Public Playbooks** and uncheck **Manage Private Playbooks**.
3. Scroll down to the **Playbook Admin** section and confirm that **Manage Public Playbooks** and **Manage Private Playbooks** are checked.
4. Select **Save**.

You can also set permissions for read-only playbooks that do allow members to create new public or private playbooks.

1. Go to **System Console > User Management > Permissions**.
2. In the **All Members** section, uncheck **Manage Public Playbooks** and uncheck **Manage Private Playbooks**.
3. Then, check **Create Public Playbook** and **Create Private Playbook**.
4. Select **Save**.

Manage how playbooks are accessed
---------------------------------

A Public playbook and its associated runs can be viewed by any member of the team. Playbooks can be converted from Public to Private, but once a playbook is Private it can't be converted back to Public.

Restrict who can convert playbooks from Public to Private
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can control whether Members can convert playbooks from public to private.

1. Go to **System Console > User Management > Permissions**.
2. In the **All Members** section, check **Convert Playbooks**.
3. Select **Save**.

To restrict this action so only Playbook Admins can convert playbooks from Public to Private:

1. Go to **System Console > User Management > Permissions**.
2. Scroll down to **Playbook Admin**.
3. Uncheck **Convert Playbooks**.
4. Select **Save**.

Control who can start runs
--------------------------

By default, all Members can start a run using a playbook. This setting restricts that action to Playbook Admins.

1. Go to **System Console > User Management > Permissions**.
2. In the **All Members** section, uncheck **Manage Runs**. This also unchecks **Create Runs**.
3. Scroll down to **Playbook Admin** and ensure that **Manage Runs** and **Create Runs** are checked.
4. Select **Save**.
