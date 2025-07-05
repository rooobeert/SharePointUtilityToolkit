# SharePointUtilityToolkit

This toolkit aims to help where SharePoint Online lists are being used as a database for Power Apps and Power Automate. 

# What this toolkit can do currently
For my own sake, I will use the word lists for both lists and libraries in SharePoint.

## Copy and paste lists
You can (initally) copy one or many lists from one or many SharePoint site collections to one or many other site collections. You **cannot** use this tool to copy over changes you made to a list and you **cannot** copy default lists like Documents or SitePages since they already exist on all site collections.

The copy and paste process includes the following elements: 
- List columns (by default)
- Column formatting (by default)
- Views (by default)
- Read and write security (lists only added on top)
- NoCrawl flag (added on top)
- Offline Available (added on top)
- enableAttachments flag (lists only added on top)

## Setting permissions on lists
You can set the permissions on one or many lists by adding users and/or groups and assigning them existing permission levels. 

## Create lists
You can create lists (without columns) on one or many site collection.

## Copy columns
You can copy columns from a list to one or many other lists.
