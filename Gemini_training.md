# Gemini Admin Console Configuration & Deployment

## The Gemini App

### Generative AI Navigation Menu

Every Google Workspace for Education Super Admin will see a **Generative AI** main menu item with
additional GenAI menu items. It's important to know this is where admins turn **ON and OFF**
Gemini, Gemini Notebook, and Gemini in Workspace. It's also where additional Gemini settings
and usage reports are found.

![Generative AI menu showing Gemini app navigations](./images/gemini-app-menu.png)

* Everyone should see *all* of these menu items
* If you do not see **"Gemini in Workspace"** open a Google Support Ticket
* **"Gemini Enterprise"** is an additional paid add-on everyone will see

### Enabling the Gemini App Core Service

Google Admins need to be aware of where and how to **enable** and **disable** Gemini services. Along
with being able to turn ON Gemini with an Organization Unit (OU) it is also possible to
enable Gemini with an **Access Group**. All admins need to double check their ON/OFF status, 
especially for their students.

1. Navigate to the Google Admin Console
1. Navigate to **Generative AI** menu item and then click on **Gemini App**
1. Click **service status**
1. Select an **Organizational Unit (OU)**
1. Turn **ON or OFF**

> [!NOTE]
> Configure by OU or Access Group

Step by Step guide: [Help Center article](https://knowledge.workspace.google.com/admin/generative-ai/gemini-app/turn-the-gemini-app-on-or-off)

![Gemini app service status setting with a red rectangle over the ON and OFF status](./images/enable-gemini.png)

### Configuring Gemini App Settings: Connected Apps

One powerful but potentially problematic feature are **Connected Apps**. Connected Apps
allow the user to integrate to other workspace apps while staying within the Gemini App.
For example: a user would be able to query their Google Drive documents and allow the
Gemini App to use that data to help with its response.

**Why is this potentially problematic?** Schools often have an oversharing problem, which means
users may have access to Google Documents they shouldn't. This feature, while powerful, could
turn *current passive data leaks into **active** data leak*s.

**Break glass fix:** If an admin finds their organization in the scenario where users are
finding overshared documents, the connected apps setting could be disabled.

1. **Workspace apps:** Allows Gemini to interact with services like Docs and Calendar.
1. **Classroom app:** Allows the Gemini app to find information from Google Classroom
   and return responses in the Gemini app.
1. **Other apps:** Allows Gemini to interact with services like YouTube and Maps.

![Apps table of settings for workspace, classroom, and other](./images/connected-apps.png)

End users can enable/disable **“Connected Apps”** in their Gemini settings

![a blue toggle on for gmail google workspace connected apps](./images/ca-enduser.png)


### Configuring Gemini Conversation History

End users are able to decide when their Gemini app conversations get purged but
just what exactly they can modify depends on the Admin Console settings. Google Admins
need to confirm their settings with other key stakeholders. 

* If you choose for conversation history to be on, select how long conversations
  are stored before they’re automatically deleted: *3, 18, or 36 months*. The default is ON and 18 months.
* Gemini chats use **rolling deletion** for retention. However, interacting with a chat thread keeps it alive.
  For example, if you have retention set to 3 months but interact with a Gemini chat thread on the 89th day,
  that chat thread will continue.
* **Vault now supports separate Gemini retention for admins.**

![Gemini conversation history setting with a checked enable gemini conversation history box](./images/gemini-convo-history.png)

### Configuring Gemini Conversation Management

One end user feature that helps with organization is the ability to **delete** Gemini app chats.
Organizations can decide whether it's allowed for different sets of users (ie staff vs students).

* Even if users delete chats, *they are still retained by Vault* based on your retention rules, just like Gmail.
* Temporary chats *are* retained in Vault but do not get saved to the end user’s history in the Gemini App.
* The default is **ON** for both options. Consider adjusting for students.

![Gemini temporary chats setting with a blue checkbox checked](./images/gemini-convo-manage.png)

### Configuring Gemini App Settings: Conversation Sharing

The Gemini App allows for sharing of chats in a two ways: **public links** or **drive links**.
General best practice is to select Drive links and allow the sharing permissions to
work like Google Docs. Since the Drive links options came after public links, Admins
may need to go into the admin console and configure this setting.

* [Controls whether users can share conversations they create within the Gemini app](https://knowledge.workspace.google.com/admin/generative-ai/gemini-app/turn-conversation-sharing-on-or-off)
* When enabled, users can create **public links** or **Drive links** to conversations,
  media created in Canvas, or Deep Research reports. *Other users can then read the
  conversation and copy it into their own Gemini app.* 

> **Limitations**
> * Users under 18 can view conversations but cannot copy/import them
> * Conversations with attached files can’t be shared

![conversation sharing setting with a blue bubble in the allow option](./images/convo-sharing.png)

### Configuring Gemini App Settings: Gem Sharing

One way to further Gemini adoption is to enable Gem Sharing for users. By default
this feature is **ON** but admins should confirm their setting.

* [Controls whether users can share Gems they create within the Gemini app](https://knowledge.workspace.google.com/admin/generative-ai/gemini-app/turn-gem-sharing-on-or-off)
* When enabled, shared Gems are managed and **stored in Google Drive**, similar to other Drive files.

![gem sharing setting with a blue checked box](./images/gem-sharing.png)

## Gemini in Google Vault

### Gemini and Google Vault Retention Information

It can get confusing regarding what services does **"Gemini"** refer to and what gets saved
for potential FOIA. **Google Vault only covers the Gemini App**, check out the
table below for guidance:

| App/Service         | Retention | Searches/Holds/Exports |
| ------------------- | :-------: | :--------------------: |
| Gemini App          | YES       | YES                    |
| Gemini Notebook     | NO        | NO                     |
| Gemini in Workspace | NO        | NO                     |




