# Gemini Admin Console Configuration & Deployment

## The Gemini App

### Generative AI Navigation Menu

![Generative AI menu showing Gemini app navigations](./images/gemini-app-menu.png)

* Everyone should see **all** of these navigation items
* If you do not see "Gemini in Workspace" open a Google Support Ticket
* "Gemini Enterprise" is an additional paid add-on everyone will see

### Enabling the Gemini App Core Service

1. Navigate to the Google Admin Console
1. Navigate to **Generative AI** menu item and then click on **Gemini App**
1. Click **service status**
1. Select an OU or use an Access group

> [!NOTE]
> Configure by OU or Access Group

Step by Step guide: [Help Center article](https://knowledge.workspace.google.com/admin/generative-ai/gemini-app/turn-the-gemini-app-on-or-off)

![Gemini app service status setting with a red rectangle over the ON and OFF status](./images/enable-gemini.png)

### Configuring Gemini App Settings: Connected Apps

1. **Workspace apps:** Allows Gemini to interact with services like Docs and Calendar.
1. **Classroom app:** Allows the Gemini app to find information from Google Classroom
   and return responses in the Gemini app *(users 18+ only)*.
1. **Other apps:** Allows Gemini to interact with services like YouTube and Maps.

![Apps table of settings for workspace, classroom, and other](./images/connected-apps.png)

End users can enable/disable “Connected Apps” in their Gemini settings

![a blue toggle on for gmail google workspace connected apps](./images/ca-enduser.png)


### Configuring Gemini Conversation History

* If you choose for conversation history to be on, select how long conversations
  are stored before they’re automatically deleted: 3, 18, or 36 months. The default is ON and 18 months.
* Gemini chats use rolling deletion for retention. However, interacting with a chat thread keeps it alive.
  For example, if you have retention set to 3 months but interact with a Gemini chat thread on the 89th day,
  that chat thread will continue.
* Vault now supports separate Gemini retention for admins.

![Gemini conversation history setting with a checked enable gemini conversation history box](./images/gemini-convo-history.png)

### Configuring Gemini Conversation Management

* Even if users delete chats, they are still retained by Vault based on your retention rules, just like Gmail.
* Temporary chats are retained in Vault but do not get saved to the end user’s history in the Gemini App.
* The default is ON for both options. Consider adjusting for students.

![Gemini temporary chats setting with a blue checkbox checked](./images/gemini-convo-manage.png)

### Configuring Gemini App Settings: Conversation Sharing

* [Controls whether users can share conversations they create within the Gemini app](https://knowledge.workspace.google.com/admin/generative-ai/gemini-app/turn-conversation-sharing-on-or-off)
* When enabled, users can create **public links** or **Drive links** to conversations,
  media created in Canvas, or Deep Research reports. *Other users can then read the
  conversation and copy it into their own Gemini app.* 

> **Limitations**
> * Users under 18 can view conversations but cannot copy/import them
> * Conversations with attached files can’t be shared

![conversation sharing setting with a blue bubble in the allow option](./images/convo-sharing.png)


### Configuring Gemini App Settings: Gem Sharing

* [Controls whether users can share Gems they create within the Gemini app](https://knowledge.workspace.google.com/admin/generative-ai/gemini-app/turn-gem-sharing-on-or-off)
* When enabled, shared Gems are managed and stored in Google Drive, similar to other Drive files.

![gem sharing setting with a blue checked box](./images/gem-sharing.png)

## Gemini in Google Vault

### Gemini and Google Vault Retention Information

| App/Service         | Retention | Searches/Holds/Exports |
| ------------------- | :-------: | :--------------------: |
| Gemini App          | YES       | YES                    |
| Gemini Notebook     | NO        | NO                     |
| Gemini in Workspace | NO        | NO                     |






