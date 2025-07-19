# SharePointUtilityToolkit
This is my first ever repo on Github, so if something seems off or weird. Well, get over it. 

## What this toolkit can do currently
For my own sake, I will use the word "lists" for both lists and libraries in SharePoint Online. This toolkit aims to help where SharePoint Online lists are being used as a database for Power Apps and Power Automate. A good application lifecycle management includes not only different Power Platform environments but also different SharePoint site collections.

## A short history
It was born from an app template I found a few years ago. I started using it to copy lists within customers tenants when I was developing Power Platform solutions for them. With this tool I was able to speed up the time it took me deploy solutions from DEV to PROD without having to use PNP PowerShell or other premium features.
I sadly cannot find the original template and creator anymore. Before I started customizing it, it was called "LCP - List Copy Paste".

## Copy and paste lists
You can copy one or many NEW lists from one or many SharePoint site collections to one or many other site collections. You **cannot** use this tool to copy over changes you made to a list and you **cannot** copy existing lists or default lists like Documents or SitePages since they already exist on all site collections.

The copy and paste process includes the following elements: 
- List columns (by default)
- Column formatting (by default)
- Views (by default)
- Read and write security (lists only added on top)
- NoCrawl flag (added on top)
- Offline Available (added on top)
- enableAttachments flag (lists only added on top)

![Screenshot of the SharePoint Utility Toolkit and the copy screen.](https://github.com/rooobeert/SharePointUtilityToolkit/blob/main/assets/images/SUT_CopyingListsExample.png)

## Setting permissions on lists
You can set the permissions on one or many lists (in many site collection) by adding users and/or groups and assigning them existing permission levels.
1. First enter a site url, then click on "Get lists"
2. You can then specify permissions for each list by applying group or user permissions. The tool will read the site collections permission levels.
3. After specifying all wanted permissions, a workflow will set them on the lists.

![Screenshot of the SharePoint Utility Toolkit and the permission screen.](https://github.com/rooobeert/SharePointUtilityToolkit/blob/main/assets/images/SUT_CopyingListsExample.png)

# Planned future features
- Copy just the columns from on to another list. Useful, if you want to update a list.
- Continue with permission setting after lists have been copied

# Behind the scenes
I will explain this a little more later on, but essentially the tool is using Power Apps Canvas as a front end with a lot of Power Automate workflows in the back. The workflows read lists, permission levels, groups and so on and pass them to the canvas app. The copy is done using the Design API of SharePoint Online. Setting the permissions is done by utilizing the default SharePoint API as well.
