---
title: Using work item form controls
titleSuffix: Azure Boards 
description: Use work item form controls to update status, link work items, and more in Azure Boards 
ms.custom: work-items, seodec18  
ms.technology: devops-agile
ms.assetid: A9AB9B95-61B4-41E7-AE7A-B96CD4AF9B33  
ms.topic: conceptual
ms.author: kaelli
monikerRange: '>= tfs-2017'
ms.date: 07/09/2020
---

# Work item form  

[!INCLUDE [temp](../includes/version-vsts-tfs-2017-on.md)]

Different types of work items track different data. Each work item form contains some standard fields&mdash;such as title, assigned to, and area and iteration path&mdash;as well as fields specific to the type. You can link work items to one another, as well as to changesets and source code files. 

### Web portal form 

As the following image shows, each work item form comes with a number of controls, fields, and tabs. Keep in mind that the work item tracking experience and forms that appear in Visual Studio won't show several of the features that the web portal makes available. 

![Work item form to track features or user stories](../backlogs/media/add-work-item-vsts-user-story-form.png)


::: moniker range=">= azure-devops-2019"

> [!NOTE]    
> Depending on the process chosen when the project was created&mdash;
[Agile](./guidance/agile-process.md), [Basic](../get-started/plan-track-work.md), [Scrum](./guidance/scrum-process.md), or [CMMI](./guidance/cmmi-process.md)&mdash;the types of work items you can create will differ. For example, backlog items may be called user stories (Agile), product backlog items (Scrum), or requirements (CMMI). All three are similar: they describe the customer value to deliver and the work to be performed.
>
> For an overview of these processes, see [Choose a process](./guidance/choose-process.md). 

::: moniker-end

::: moniker range="< azure-devops-2019"

> [!NOTE]    
>Depending on the process chosen when the project was created&mdash;
[Agile](./guidance/agile-process.md), [Scrum](./guidance/scrum-process.md), or [CMMI](./guidance/cmmi-process.md)&mdash;the types of work items you can create will differ. For example, backlog items may be called user stories (Agile), product backlog items (Scrum), or requirements (CMMI). All three are similar: they describe the customer value to deliver and the work to be performed.
>
> For an overview of the three default processes, see [Choose a process](./guidance/choose-process.md). 

::: moniker-end


<a id="wi-controls"></a>  

### Form controls

| Control                  | Function                      |
|--------------------------|-------------------------------|
| ![Copy to clipboard icon](../backlogs/media/icon-copy-to-clipboard.png) | Copy URL of work item to clipboard (appears on hover over work item title)  |
| ![Discussions icon](../media/icons/icon-discussions-wi.png) | Go to Discussions section  |
|   :::image type="icon" source="../media/icons/actions-icon.png" border="false":::  | Open Actions menu for additional work item tasks           |
| ![Refresh icon](../media/icons/icon-refresh-wi.png) | Refresh work item with latest changes  |  
| ![Undo icon](../media/icons/icon-undo-changes-wi.png) | Revert changes to work item           |  
| ![History tab icon](../media/icons/icon-history-tab-wi.png) | Open History tab        |
| ![Links tab icon](../media/icons/icon-links-tab-wi.png) | Open Links tab     |
| ![Attachment tab icon](../backlogs/media/icon-attachments-tab-wi.png) | Open Attachments tab   |
| ![full screen icon](../media/icons/fullscreen_icon.png) / ![exit full screen icon](../media/icons/exitfullscreen_icon.png)     | Enter or exit full display mode of a section within the form   |
|![Collapse section icon](../media/icons/collapse-wi-section.png)/![Expand section icon](../media/icons/expand-wi-section.png) | Collapse or expand a section within the form   |  
| ![New linked work item icon](../media/icons/new-linked-work-item.png) | Add new work item and link to existing work item (May appear under   :::image type="icon" source="../media/icons/actions-icon.png" border="false":::  Actions menu)  |  
| ![Change work item type icon](../media/icons/change-type-icon.png) | [Change work item type](../backlogs/remove-delete-work-items.md) (Appears under   :::image type="icon" source="../media/icons/actions-icon.png" border="false":::  Actions menu)  | 
| ![Change project icon](../media/icons/change-team-project-icon.png) | [Move work item to a different project](../backlogs/remove-delete-work-items.md) (Appears under   :::image type="icon" source="../media/icons/actions-icon.png" border="false":::  Actions menu)  | 
| ![Clone icon](../media/icons/clone-icon.png) | [Copy work item and optionally change work item type](../backlogs/copy-clone-work-items.md#copy-clone) (Appears  under   :::image type="icon" source="../media/icons/actions-icon.png" border="false":::  Actions menu)  |  
| ![Email icon](../media/icons/email-icon.png) | [Email work item](email-work-items.md)  (Appears  under   :::image type="icon" source="../media/icons/actions-icon.png" border="false":::  Actions menu)  |  
| ![Delete icon](../media/icons/delete_icon.png) | [Recycle work item](../backlogs/remove-delete-work-items.md)  (Appears  under   :::image type="icon" source="../media/icons/actions-icon.png" border="false":::  Actions menu)  | 
| ![Storyboard icon](../media/icons/storyboard-icon.png) | [Storyboard with PowerPoint](/previous-versions/azure/devops/boards/backlogs/office/storyboard-your-ideas-using-powerpoint)  (Appears  under   :::image type="icon" source="../media/icons/actions-icon.png" border="false":::  Actions menu)  | 

<a id="update-work-status">  </a>

## Update work status  

As work progresses, team members can update the state and reassign it as needed. 

<img src="../backlogs/media/add-work-item-vsts-update-state.png" alt="Product backlog item workflow, Scrum process" style="border: 1px solid #C3C3C3;" />  

While the workflow states differ for different work item types, they usually follow a progression from New or Active to Closed or Done. The following image shows the work flow states for the Agile process user story. If you want to discard a work item, change the state to Removed.  

<table>
<tbody valign="top">
<tr>
<td>
<p><b>Typical workflow progression:</b> </p> 
<ul>
<li>Create a user story in the default state, New.</li>
<li>Change the state from New to Active.</li>
<li>Change the state from Active to Resolved.</li>
<li>Change the state from Resolved to Closed.</li>
</ul>
<br/>
<p><b>Atypical transitions:</b> </p> 
<ul>
<li>Change the state from New to Removed.</li>
<li>Change the state from Removed to New.</li>
<li>Change the state from Active to Removed.</li>
<li>Change the state from Resolved to Active.</li>
<li>Change the state from Closed to Resolved.</li>
</ul>
</td>
<td>
<img src="./guidance/media/ALM_PT_Agile_WF_UserStory.png" alt="Work flow states for the Agile process user story."/><br/></td>
</tr>
</tbody>
</table>

Removed work items remain in the data store and can be reactivated by changing the State. If you want to permanently remove a work item, you can [delete it](../backlogs/remove-delete-work-items.md). 

With each update, the Reason field also updates and changes are recorded in the History field which you can view through the ![history tab icon](../media/icons/icon-history-tab-wi.png) **History** tab. To find work items based on their history, see [History & auditing](../queries/history-and-auditing.md).   

<img src="../backlogs/media/add-work-item-history.png" alt="View change history" style="border: 1px solid #C3C3C3;" />  



<a id="link-wi">  </a>

## Link items to support traceability  

By linking work items using Related or Dependent link types, you can track work that is dependent on other work. Each work item contains one or more tabs with link controls. These controls support linking the work item to one or more objects.  

There are three links controls provided on most forms. The Development and Related Work scoped links controls appear on the Details tab. The ![Links page icon](../media/icons/icon-links-tab-wi.png) Links tab provides access to all links made to the work item.  

<img src="../../reference/xml/media/linkscontrol-bug-form-dev-related-links.png" alt="Bug work item form, Agile process, Development and Related links controls" style="border: 1px solid #C3C3C3;" />  


## Add links  

From each links control, you can perform these actions:  

- To open an associated item or object, click the linked item  
- To delete a link, highlight it and click the ![delete icon](../media/icons/delete_icon.png) delete icon   
- To link to an existing item, or create and link a new work item, select one of the menu options.  

<img src="../../reference/xml/media/linkscontrol-related-work-menu-options.png" alt="Links control menu of options" style="border: 1px solid #C3C3C3;" />  

To learn more, see [Add links to work items](../backlogs/add-link.md).

<a id="git-development">  </a>

### Development scoped links control  

The Development links control displays all of your development links, whether based on a git or Team Foundation version control (TFVC) repository. It displays links in a set order, and provides calls-to-action that support users to [drive development from a work item](../backlogs/connect-work-items-to-git-dev-ops.md).  

Team Foundation version control (TFVC) lets you link work items to version control changesets or versioned source code files by using the Changeset and Versioned Item link types. When you check in pending changes or use My Work to check in changes, [work items are automatically linked to your changes](../../repos/tfvc/check-your-work-team-codebase.md).  

Git lets you link work items to commits by using the Commit link type. To learn how, see [Manage and commit your changes](../../repos/git/commits.md).  

### Related scoped links control 

The Related Work links control displays links to other work items in a set order on the front page of the form. It supports these link types: Duplicate/Duplicate of, Parent/Child, Predecessor/Successor, Related, and Tests/Tested by. To learn more about different link types, see [Linking, traceability, and managing dependencies](../queries/link-work-items-support-traceability.md).

### Links control tab 

In addition, the Links control tab provides access to all links made to the work item&mdash;both work items and external objects. 

<img src="../backlogs/media/add-work-item-links.png" alt="Agile process, User Story work item form, Links control tab" style="border: 1px solid #C3C3C3;" />   

<a id="discussion">  </a>

[!INCLUDE [temp](../includes/discussion-tip.md)]

<a id="copy-url">  </a>

## Copy the URL

From the web portal, simply copy the URL from the web browser address or hover over the title and then click the :::image type="icon" source="../../media/icons/copy-clone-icon.png" border="false"::: copy icon. For other copy options, see [Copy or clone work items](../backlogs/copy-clone-work-items.md). 

![Copy hyperlink for a work item from web portal](../backlogs/media/add-work-item-copy-URL.png) 



<a id="start-storyboarding">  </a>

## Start storyboarding  

> [!IMPORTANT]  
> Starting with Visual Studio 2019, the Azure DevOps Office Integratoin plug-in has deprecated support for Storyboarding with PowerPoint and Microsoft Project. Also, the Visual Studio Gallery for PowerPoint Storyboarding has been deprecated.  
 
The **Start storyboarding** menu option is only available from the new web form. However, from the old web form, you can choose the **Start Storyboarding** link from the **Storyboard** tab from a backlog item, or simply open PowerPoint. See [Storyboard your ideas using PowerPoint](/previous-versions/azure/devops/boards/backlogs/office/storyboard-your-ideas-using-powerpoint) for requirements and usage.    

You can storyboard your ideas using PowerPoint to bring your ideas to life with storyboard shapes, text, animation, and all the other features that PowerPoint Storyboarding provides. From any work item, you can open PowerPoint by choosing the Start storyboarding menu option.    
![Work item form, Start storyboarding menu option](../backlogs/media/add-work-item-start-storyboarding.png)



## Related articles

- [Perform a semantic or ad hoc work item search](../queries/search-box-queries.md)
- [Keyboard shortcuts](../../project/navigation/keyboard-shortcuts.md)
- [Customize your work tracking experience](../../reference/customize-work.md)
- [Bulk add or modify work items using Excel](../backlogs/office/bulk-add-modify-work-items-excel.md)

