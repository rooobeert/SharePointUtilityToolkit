# SharePointUtilityToolkit

This toolkit aims to help where SharePoint Online lists are being used as a database for Power Apps and Power Automate. 

# What this toolkit can do currently
For my own sake, I will use the word lists for both lists and libraries in SharePoint.

## Copy and paste lists
You can (initally) copy one or many lists from one or many SharePoint site collections to one or many other site collections. You can use this tool to copy over changes you made to a list and you cannot copy default lists like Documents or SitePages since they already exist on all site collections.

The copy and paste process includes the following elements: 
- List columns (by default)
- Column formatting (by default)
- Views (by default)
- Read and write security (added on top)
- The NoCrawl flag (added on top)

