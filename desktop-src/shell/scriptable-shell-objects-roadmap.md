---
description: La shell di Windows fornisce un potente set di oggetti di automazione che consentono di programmare la shell con Microsoft Visual Basic e linguaggi di scripting, ad esempio Microsoft JScript (compatibile con la specifica del linguaggio ECMA 262) e Microsoft Visual Basic Scripting Edition (VBScript). È possibile usare questi oggetti per accedere a molte delle funzionalità e delle finestre di dialogo della shell. Ad esempio, è possibile accedere alla file system, avviare programmi e modificare le impostazioni di sistema.
title: Oggetti Shell tramite script
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980466"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="33f01-105">Oggetti Shell tramite script</span><span class="sxs-lookup"><span data-stu-id="33f01-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="33f01-106">La shell di Windows fornisce un potente set di oggetti di automazione che consentono di programmare la shell con Microsoft Visual Basic e linguaggi di scripting, ad esempio Microsoft JScript (compatibile con la specifica del linguaggio ECMA 262) e Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="33f01-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="33f01-107">È possibile usare questi oggetti per accedere a molte delle funzionalità e delle finestre di dialogo della shell.</span><span class="sxs-lookup"><span data-stu-id="33f01-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="33f01-108">Ad esempio, è possibile accedere alla file system, avviare programmi e modificare le impostazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="33f01-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="33f01-109">In questa sezione vengono introdotti gli oggetti della shell di scripting.</span><span class="sxs-lookup"><span data-stu-id="33f01-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="33f01-110">Versioni della shell</span><span class="sxs-lookup"><span data-stu-id="33f01-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="33f01-111">Creazione di istanze di oggetti Shell</span><span class="sxs-lookup"><span data-stu-id="33f01-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="33f01-112">Associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="33f01-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="33f01-113">Elemento oggetto HTML</span><span class="sxs-lookup"><span data-stu-id="33f01-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="33f01-114">Oggetto Shell</span><span class="sxs-lookup"><span data-stu-id="33f01-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="33f01-115">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="33f01-115">Security</span></span>](#security)
-   [<span data-ttu-id="33f01-116">Oggetti Folder</span><span class="sxs-lookup"><span data-stu-id="33f01-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="33f01-117">Versioni della shell</span><span class="sxs-lookup"><span data-stu-id="33f01-117">Shell Versions</span></span>

<span data-ttu-id="33f01-118">Molti degli oggetti della shell sono diventati disponibili nella [versione 4,71](versions.md) della shell.</span><span class="sxs-lookup"><span data-stu-id="33f01-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="33f01-119">Altre sono disponibili nella versione 5,00 e successive.</span><span class="sxs-lookup"><span data-stu-id="33f01-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="33f01-120">La versione 5,00 è diventata disponibile con Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="33f01-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="33f01-121">La tabella seguente elenca ogni oggetto Shell sotto la versione della shell in cui l'oggetto è diventato disponibile.</span><span class="sxs-lookup"><span data-stu-id="33f01-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="33f01-122">Versione 4,71</span><span class="sxs-lookup"><span data-stu-id="33f01-122">Version 4.71</span></span>                                            | <span data-ttu-id="33f01-123">Versione 5,00</span><span class="sxs-lookup"><span data-stu-id="33f01-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="33f01-124">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="33f01-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="33f01-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="33f01-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="33f01-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="33f01-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="33f01-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="33f01-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="33f01-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="33f01-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="33f01-129">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="33f01-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="33f01-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="33f01-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="33f01-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="33f01-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="33f01-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="33f01-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="33f01-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="33f01-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="33f01-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="33f01-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="33f01-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="33f01-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="33f01-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="33f01-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="33f01-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="33f01-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="33f01-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="33f01-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="33f01-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="33f01-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="33f01-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="33f01-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="33f01-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="33f01-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="33f01-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="33f01-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="33f01-143">Creazione di istanze di oggetti Shell</span><span class="sxs-lookup"><span data-stu-id="33f01-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="33f01-144">Per creare un'istanza degli oggetti della shell in Visual Basic applicazioni con associazione anticipata, aggiungere i riferimenti alle librerie seguenti nel progetto:</span><span class="sxs-lookup"><span data-stu-id="33f01-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="33f01-145">Microsoft Internet Controls (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="33f01-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="33f01-146">Controlli e automazione della shell Microsoft (Shell32)</span><span class="sxs-lookup"><span data-stu-id="33f01-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="33f01-147">Associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="33f01-147">Late Binding</span></span>

<span data-ttu-id="33f01-148">È anche possibile creare un'istanza di molti oggetti della shell con associazione tardiva.</span><span class="sxs-lookup"><span data-stu-id="33f01-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="33f01-149">Questo approccio funziona nelle applicazioni Visual Basic e nello script.</span><span class="sxs-lookup"><span data-stu-id="33f01-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="33f01-150">Nell'esempio seguente viene illustrato come creare un'istanza dell'oggetto [**Shell**](shell.md) in JScript.</span><span class="sxs-lookup"><span data-stu-id="33f01-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



<span data-ttu-id="33f01-151">Nell'esempio seguente viene illustrato come creare un'istanza dell'oggetto [**Folder**](folder.md) in VBScript.</span><span class="sxs-lookup"><span data-stu-id="33f01-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



<span data-ttu-id="33f01-152">Nell'esempio precedente, *SDIR* è il percorso dell'oggetto [**Folder**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="33f01-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="33f01-153">Si noti che i valori di enumerazione [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) non sono disponibili nello script.</span><span class="sxs-lookup"><span data-stu-id="33f01-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="33f01-154">Il ProgID per ogni oggetto Shell è illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="33f01-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="33f01-155">Oggetto</span><span class="sxs-lookup"><span data-stu-id="33f01-155">Object</span></span>                                                  | <span data-ttu-id="33f01-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="33f01-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="33f01-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="33f01-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="33f01-158">Microsoft. DiskQuota. 1</span><span class="sxs-lookup"><span data-stu-id="33f01-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="33f01-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="33f01-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="33f01-160">Non è possibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="33f01-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="33f01-161">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="33f01-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="33f01-162">Shell. \_Applicazione shell. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="33f01-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="33f01-163">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="33f01-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="33f01-164">Shell. \_Applicazione shell. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="33f01-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="33f01-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="33f01-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="33f01-166">Shell. \_Applicazione shell. Namespace ("..."). Self o Folder. Items. Item o Folder. ParseName</span><span class="sxs-lookup"><span data-stu-id="33f01-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="33f01-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="33f01-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="33f01-168">Folder. Items</span><span class="sxs-lookup"><span data-stu-id="33f01-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="33f01-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="33f01-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="33f01-170">Folder. Items</span><span class="sxs-lookup"><span data-stu-id="33f01-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="33f01-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="33f01-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="33f01-172">Shell. NameSpace ("..."). Self. Verbs. Item ()</span><span class="sxs-lookup"><span data-stu-id="33f01-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="33f01-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="33f01-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="33f01-174">FolderItem. Verbs o Shell. NameSpace ("..."). Verbi autonomi</span><span class="sxs-lookup"><span data-stu-id="33f01-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="33f01-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="33f01-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="33f01-176">Shell. \_Applicazione shell</span><span class="sxs-lookup"><span data-stu-id="33f01-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="33f01-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="33f01-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="33f01-178">Shell. NameSpace ("..."). Self. GetLink o Shell. NameSpace ("..."). Elementi (). GetLink</span><span class="sxs-lookup"><span data-stu-id="33f01-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="33f01-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="33f01-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="33f01-180">Shell. \_Applicazione shell</span><span class="sxs-lookup"><span data-stu-id="33f01-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="33f01-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="33f01-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="33f01-182">Shell. NameSpace ("..."). Self o Shell. NameSpace ("..."). Elementi ()</span><span class="sxs-lookup"><span data-stu-id="33f01-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="33f01-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="33f01-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="33f01-184">Non è possibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="33f01-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="33f01-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="33f01-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="33f01-186">Non è possibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="33f01-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="33f01-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="33f01-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="33f01-188">Shell. NameSpace ("..."). Self. GetLink o Shell. NameSpace ("..."). Elementi (). GetLink</span><span class="sxs-lookup"><span data-stu-id="33f01-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="33f01-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="33f01-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="33f01-190">Non è possibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="33f01-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="33f01-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="33f01-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="33f01-192">Shell. Shell \_ Windows o shellwindows. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="33f01-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="33f01-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="33f01-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="33f01-194">Non è possibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="33f01-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="33f01-195">Elemento oggetto HTML</span><span class="sxs-lookup"><span data-stu-id="33f01-195">HTML OBJECT Element</span></span>

<span data-ttu-id="33f01-196">È anche possibile usare l'elemento [**oggetto**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) per creare un'istanza di oggetti Shell in una pagina HTML.</span><span class="sxs-lookup"><span data-stu-id="33f01-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="33f01-197">A tale scopo, impostare l'attributo **ID** dell'elemento **oggetto** sul nome della variabile che verrà usato negli script e identificare l'oggetto usando il numero registrato (ClassID).</span><span class="sxs-lookup"><span data-stu-id="33f01-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="33f01-198">Il codice HTML seguente crea un'istanza dell'oggetto [**ShellFolderItem**](shellfolderitem-object.md) usando l'elemento **Object** .</span><span class="sxs-lookup"><span data-stu-id="33f01-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="33f01-199">Nella tabella seguente sono elencati tutti gli oggetti Shell e i rispettivi CLASSId.</span><span class="sxs-lookup"><span data-stu-id="33f01-199">The following table lists each Shell object and its respective CLASSID.</span></span>



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="33f01-200">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="33f01-200">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="33f01-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="33f01-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="33f01-202">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="33f01-202">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="33f01-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="33f01-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="33f01-204">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="33f01-204">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="33f01-205">BBCBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="33f01-205">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="33f01-206">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="33f01-206">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="33f01-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="33f01-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="33f01-208">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="33f01-208">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="33f01-209">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="33f01-209">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="33f01-210">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="33f01-210">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="33f01-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="33f01-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="33f01-212">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="33f01-212">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="33f01-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="33f01-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="33f01-214">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="33f01-214">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="33f01-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="33f01-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="33f01-216">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="33f01-216">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="33f01-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="33f01-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="33f01-218">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="33f01-218">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="33f01-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="33f01-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="33f01-220">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="33f01-220">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="33f01-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="33f01-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="33f01-222">**Shell**</span><span class="sxs-lookup"><span data-stu-id="33f01-222">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="33f01-223">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="33f01-223">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="33f01-224">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="33f01-224">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="33f01-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="33f01-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="33f01-226">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="33f01-226">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="33f01-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="33f01-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="33f01-228">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="33f01-228">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="33f01-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="33f01-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="33f01-230">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="33f01-230">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="33f01-231">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="33f01-231">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="33f01-232">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="33f01-232">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="33f01-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="33f01-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="33f01-234">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="33f01-234">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="33f01-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="33f01-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="33f01-236">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="33f01-236">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="33f01-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="33f01-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="33f01-238">Oggetto Shell</span><span class="sxs-lookup"><span data-stu-id="33f01-238">Shell Object</span></span>

<span data-ttu-id="33f01-239">L'oggetto [**Shell**](shell.md) rappresenta gli oggetti nella shell.</span><span class="sxs-lookup"><span data-stu-id="33f01-239">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="33f01-240">È possibile utilizzare i metodi esposti dall'oggetto Shell per:</span><span class="sxs-lookup"><span data-stu-id="33f01-240">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="33f01-241">Aprire, esplorare e cercare le cartelle.</span><span class="sxs-lookup"><span data-stu-id="33f01-241">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="33f01-242">Ridurre a icona, ripristinare, Cascade o affiancare finestre aperte.</span><span class="sxs-lookup"><span data-stu-id="33f01-242">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="33f01-243">Avviare le applicazioni del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="33f01-243">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="33f01-244">Finestre di dialogo del sistema di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="33f01-244">Display system dialog boxes.</span></span>

<span data-ttu-id="33f01-245">È probabile che gli utenti abbiano familiarità con i comandi a cui accedono dal menu **Start** e dal menu di scelta rapida della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="33f01-245">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="33f01-246">Quando gli utenti fanno clic con il pulsante destro del mouse sulla barra delle applicazioni viene visualizzato il menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="33f01-246">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="33f01-247">La seguente applicazione HTML (HTA) produce una pagina iniziale con pulsanti che implementano molti dei metodi dell'oggetto [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="33f01-247">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="33f01-248">Alcuni di questi metodi implementano funzionalità dal menu **Start** e dal menu di scelta rapida della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="33f01-248">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a><span data-ttu-id="33f01-249">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="33f01-249">Security</span></span>

<span data-ttu-id="33f01-250">Come applicazione, una HTA viene eseguita con un modello di sicurezza diverso rispetto a una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="33f01-250">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="33f01-251">Per interagire con una pagina Web che implementa la funzionalità degli oggetti della shell, gli utenti devono abilitare i **controlli ActiveX Initialize e script non contrassegnati come opzione Safe** per l'area di sicurezza in cui stanno visualizzando la pagina.</span><span class="sxs-lookup"><span data-stu-id="33f01-251">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="33f01-252">Oggetti Folder</span><span class="sxs-lookup"><span data-stu-id="33f01-252">Folder Objects</span></span>

<span data-ttu-id="33f01-253">L'oggetto [**Folder**](folder.md) rappresenta una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="33f01-253">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="33f01-254">È possibile utilizzare i metodi esposti dall'oggetto Folder per:</span><span class="sxs-lookup"><span data-stu-id="33f01-254">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="33f01-255">Ottenere informazioni su una cartella.</span><span class="sxs-lookup"><span data-stu-id="33f01-255">Get information about a folder.</span></span>
-   <span data-ttu-id="33f01-256">Creare sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="33f01-256">Create subfolders.</span></span>
-   <span data-ttu-id="33f01-257">Copiare e spostare gli oggetti file nella cartella.</span><span class="sxs-lookup"><span data-stu-id="33f01-257">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="33f01-258">L'oggetto [**FolderItem**](folderitem.md) rappresenta un elemento in una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="33f01-258">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="33f01-259">Le proprietà consentono di recuperare le informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="33f01-259">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="33f01-260">È possibile usare i metodi esposti da questo oggetto per eseguire i verbi di un elemento o per recuperare informazioni sull'oggetto [**folderitemverbs**](folderitemverbs.md) di un elemento.</span><span class="sxs-lookup"><span data-stu-id="33f01-260">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="33f01-261">L'oggetto [**FolderItems**](folderitems.md) rappresenta una raccolta di elementi in una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="33f01-261">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="33f01-262">I metodi e le proprietà consentono di recuperare informazioni sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="33f01-262">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="33f01-263">Nell'esempio di Visual Basic seguente viene illustrata la relazione tra diversi oggetti cartella e il modo in cui possono essere utilizzati insieme.</span><span class="sxs-lookup"><span data-stu-id="33f01-263">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="33f01-264">Quando l'utente fa clic sul pulsante di comando denominato **cmdGetPath**, il programma visualizza una finestra di dialogo che consente all'utente di selezionare una cartella da **computer locale**, dove ssfDRIVES è il valore di enumerazione [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) per **computer locale**.</span><span class="sxs-lookup"><span data-stu-id="33f01-264">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="33f01-265">Quando l'utente sceglie una cartella, il percorso della cartella viene visualizzato nella casella di testo denominata **txtPath**.</span><span class="sxs-lookup"><span data-stu-id="33f01-265">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



<span data-ttu-id="33f01-266">In VBScript questa funzione è leggermente diversa perché i valori di enumerazione [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) non sono disponibili nello script.</span><span class="sxs-lookup"><span data-stu-id="33f01-266">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="33f01-267">Nell'esempio seguente viene illustrato l'equivalente VBScript dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="33f01-267">The following example shows the VBScript equivalent of the previous example.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



<span data-ttu-id="33f01-268">Nell'esempio JScript seguente, che è una traduzione diretta dell'esempio VBScript precedente, si noti come vengono [**usate le parentesi**](folder-items.md) vuote ' ()' per richiamare i metodi [**Items e Item**](folderitems-item.md) .</span><span class="sxs-lookup"><span data-stu-id="33f01-268">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
