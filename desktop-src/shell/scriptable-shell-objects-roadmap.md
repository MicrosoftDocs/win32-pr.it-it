---
description: Windows Shell offre un potente set di oggetti di automazione che consentono di programmare la shell con Microsoft Visual Basic e linguaggi di scripting come Microsoft JScript (compatibile con la specifica del linguaggio ECMA 262) e Microsoft Visual Basic Scripting Edition (VBScript). È possibile usare questi oggetti per accedere a molte delle funzionalità e delle finestre di dialogo della shell. Ad esempio, è possibile accedere al file system, avviare programmi e modificare le impostazioni di sistema.
title: Oggetti della shell gestibili da script
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e8685b44d00d3f48e8de2a567218ef08c1cb5070
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581779"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="1ae1c-105">Oggetti della shell gestibili da script</span><span class="sxs-lookup"><span data-stu-id="1ae1c-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="1ae1c-106">Windows Shell offre un potente set di oggetti di automazione che consentono di programmare la shell con Microsoft Visual Basic e linguaggi di scripting come Microsoft JScript (compatibile con la specifica del linguaggio ECMA 262) e Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="1ae1c-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="1ae1c-107">È possibile usare questi oggetti per accedere a molte delle funzionalità e delle finestre di dialogo della shell.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="1ae1c-108">Ad esempio, è possibile accedere al file system, avviare programmi e modificare le impostazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="1ae1c-109">Questa sezione presenta gli oggetti shell gestibili da script.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="1ae1c-110">Versioni della shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="1ae1c-111">Creazione di istanze di oggetti shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="1ae1c-112">Associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="1ae1c-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="1ae1c-113">Elemento OBJECT HTML</span><span class="sxs-lookup"><span data-stu-id="1ae1c-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="1ae1c-114">Oggetto shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="1ae1c-115">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="1ae1c-115">Security</span></span>](#security)
-   [<span data-ttu-id="1ae1c-116">Oggetti cartella</span><span class="sxs-lookup"><span data-stu-id="1ae1c-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="1ae1c-117">Versioni della shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-117">Shell Versions</span></span>

<span data-ttu-id="1ae1c-118">Molti degli oggetti shell sono diventati disponibili [nella versione 4.71](versions.md) della shell.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="1ae1c-119">Altri sono disponibili nella versione 5.00 e successive.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="1ae1c-120">La versione 5.00 è diventata disponibile con Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="1ae1c-121">La tabella seguente elenca ogni oggetto Shell nella versione della shell in cui l'oggetto è diventato disponibile.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="1ae1c-122">Versione 4.71</span><span class="sxs-lookup"><span data-stu-id="1ae1c-122">Version 4.71</span></span>                                            | <span data-ttu-id="1ae1c-123">Versione 5.00</span><span class="sxs-lookup"><span data-stu-id="1ae1c-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="1ae1c-124">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="1ae1c-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="1ae1c-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="1ae1c-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="1ae1c-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="1ae1c-129">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="1ae1c-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="1ae1c-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="1ae1c-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="1ae1c-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="1ae1c-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="1ae1c-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="1ae1c-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="1ae1c-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="1ae1c-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="1ae1c-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="1ae1c-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="1ae1c-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="1ae1c-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="1ae1c-143">Creazione di istanze di oggetti shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="1ae1c-144">Per creare un'istanza degli oggetti shell Visual Basic applicazioni con associazione anticipata, aggiungere riferimenti alle librerie seguenti nel progetto:</span><span class="sxs-lookup"><span data-stu-id="1ae1c-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="1ae1c-145">Microsoft Internet Controls (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="1ae1c-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="1ae1c-146">Controlli e automazione della shell Microsoft (Shell32)</span><span class="sxs-lookup"><span data-stu-id="1ae1c-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="1ae1c-147">Associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="1ae1c-147">Late Binding</span></span>

<span data-ttu-id="1ae1c-148">È anche possibile creare un'istanza di molti oggetti shell con associazione tardiva.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="1ae1c-149">Questo approccio funziona nelle applicazioni Visual Basic e nello script.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="1ae1c-150">L'esempio seguente illustra come creare un'istanza [**dell'oggetto Shell**](shell.md) in JScript.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


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



<span data-ttu-id="1ae1c-151">Nell'esempio seguente viene illustrato come creare un'istanza [**dell'oggetto Folder**](folder.md) in VBScript.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


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



<span data-ttu-id="1ae1c-152">Nell'esempio precedente *sDir è* il percorso [**dell'oggetto**](folder.md) Folder.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="1ae1c-153">Si noti che [**i valori di enumerazione ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) non sono disponibili nello script.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="1ae1c-154">Il ProgID per ogni oggetto Shell è illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="1ae1c-155">Oggetto</span><span class="sxs-lookup"><span data-stu-id="1ae1c-155">Object</span></span>                                                  | <span data-ttu-id="1ae1c-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="1ae1c-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ae1c-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="1ae1c-158">Microsoft.DiskQuota.1</span><span class="sxs-lookup"><span data-stu-id="1ae1c-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="1ae1c-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="1ae1c-160">Impossibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="1ae1c-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="1ae1c-161">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="1ae1c-162">Guscio. Shell \_ Application.NameSpace("...")</span><span class="sxs-lookup"><span data-stu-id="1ae1c-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="1ae1c-163">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="1ae1c-164">Guscio. Shell \_ Application.NameSpace("...")</span><span class="sxs-lookup"><span data-stu-id="1ae1c-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="1ae1c-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="1ae1c-166">Guscio. Shell \_ Application.NameSpace("..."). Self o Folder.Items.Item o Folder.ParseName</span><span class="sxs-lookup"><span data-stu-id="1ae1c-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="1ae1c-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="1ae1c-168">Folder.Items</span><span class="sxs-lookup"><span data-stu-id="1ae1c-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="1ae1c-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="1ae1c-170">Folder.Items</span><span class="sxs-lookup"><span data-stu-id="1ae1c-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="1ae1c-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="1ae1c-172">Shell.NameSpace("..."). Self.Verbs.Item()</span><span class="sxs-lookup"><span data-stu-id="1ae1c-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="1ae1c-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="1ae1c-174">FolderItem.Verbs o Shell.NameSpace("..."). Self.Verbs</span><span class="sxs-lookup"><span data-stu-id="1ae1c-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="1ae1c-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="1ae1c-176">Guscio. Applicazione \_ shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="1ae1c-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="1ae1c-178">Shell.NameSpace("..."). Self.GetLink o Shell.NameSpace("..."). Items(). GetLink</span><span class="sxs-lookup"><span data-stu-id="1ae1c-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="1ae1c-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="1ae1c-180">Guscio. Applicazione \_ shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="1ae1c-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="1ae1c-182">Shell.NameSpace("..."). Self o Shell.NameSpace("..."). Items()</span><span class="sxs-lookup"><span data-stu-id="1ae1c-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="1ae1c-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="1ae1c-184">Impossibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="1ae1c-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="1ae1c-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="1ae1c-186">Impossibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="1ae1c-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="1ae1c-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="1ae1c-188">Shell.NameSpace("..."). Self.GetLink o Shell.NameSpace("..."). Items(). GetLink</span><span class="sxs-lookup"><span data-stu-id="1ae1c-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="1ae1c-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="1ae1c-190">Impossibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="1ae1c-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="1ae1c-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="1ae1c-192">Guscio. Shell \_ Windows o ShellWindows. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="1ae1c-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="1ae1c-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="1ae1c-194">Impossibile eseguire l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="1ae1c-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="1ae1c-195">Elemento OBJECT HTML</span><span class="sxs-lookup"><span data-stu-id="1ae1c-195">HTML OBJECT Element</span></span>

<span data-ttu-id="1ae1c-196">È anche possibile usare [**l'elemento OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) per creare un'istanza degli oggetti shell in una pagina HTML.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="1ae1c-197">A tale scopo, impostare l'attributo **ID** dell'elemento **OBJECT** sul nome della variabile che verrà utilizzata negli script e identificare l'oggetto usando il relativo numero registrato (CLASSID).</span><span class="sxs-lookup"><span data-stu-id="1ae1c-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="1ae1c-198">Il codice HTML seguente crea un'istanza [**dell'oggetto ShellFolderItem**](shellfolderitem-object.md) usando l'elemento **OBJECT.**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="1ae1c-199">La tabella seguente elenca ogni oggetto Shell e il rispettivo CLASSID.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-199">The following table lists each Shell object and its respective CLASSID.</span></span>



| <span data-ttu-id="1ae1c-200">Oggetto shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-200">Shell object</span></span>                                           | <span data-ttu-id="1ae1c-201">Classid</span><span class="sxs-lookup"><span data-stu-id="1ae1c-201">CLASSID</span></span>                              |
|--------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="1ae1c-202">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-202">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="1ae1c-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="1ae1c-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="1ae1c-204">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-204">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="1ae1c-205">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="1ae1c-205">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="1ae1c-206">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-206">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="1ae1c-207">TBBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="1ae1c-207">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="1ae1c-208">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-208">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="1ae1c-209">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="1ae1c-209">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="1ae1c-210">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-210">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="1ae1c-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="1ae1c-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="1ae1c-212">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-212">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="1ae1c-213">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="1ae1c-213">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="1ae1c-214">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-214">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="1ae1c-215">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="1ae1c-215">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="1ae1c-216">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-216">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="1ae1c-217">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="1ae1c-217">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="1ae1c-218">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-218">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="1ae1c-219">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="1ae1c-219">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="1ae1c-220">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-220">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="1ae1c-221">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="1ae1c-221">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="1ae1c-222">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-222">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="1ae1c-223">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="1ae1c-223">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="1ae1c-224">**Shell**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-224">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="1ae1c-225">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="1ae1c-225">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="1ae1c-226">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-226">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="1ae1c-227">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="1ae1c-227">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="1ae1c-228">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-228">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="1ae1c-229">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="1ae1c-229">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="1ae1c-230">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-230">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="1ae1c-231">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="1ae1c-231">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="1ae1c-232">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-232">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="1ae1c-233">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="1ae1c-233">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="1ae1c-234">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-234">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="1ae1c-235">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="1ae1c-235">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="1ae1c-236">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-236">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="1ae1c-237">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="1ae1c-237">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="1ae1c-238">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="1ae1c-238">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="1ae1c-239">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="1ae1c-239">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="1ae1c-240">Oggetto shell</span><span class="sxs-lookup"><span data-stu-id="1ae1c-240">Shell Object</span></span>

<span data-ttu-id="1ae1c-241">[**L'oggetto Shell**](shell.md) rappresenta gli oggetti nella shell.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-241">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="1ae1c-242">È possibile usare i metodi esposti dall'oggetto Shell per:</span><span class="sxs-lookup"><span data-stu-id="1ae1c-242">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="1ae1c-243">Aprire, esplorare e cercare le cartelle.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-243">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="1ae1c-244">Ridurre a icona, ripristinare, sovrapporre o affiancare le finestre aperte.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-244">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="1ae1c-245">Avviare Pannello di controllo applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-245">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="1ae1c-246">Visualizzare le finestre di dialogo di sistema.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-246">Display system dialog boxes.</span></span>

<span data-ttu-id="1ae1c-247">Gli utenti hanno probabilmente maggiore familiarità con i comandi a cui accedono dal menu **Start** e dal menu di scelta rapida della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-247">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="1ae1c-248">Il menu di scelta rapida della barra delle applicazioni viene visualizzato quando gli utenti fa clic con il pulsante destro del mouse sulla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-248">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="1ae1c-249">L'applicazione HTML (HTA) seguente genera una pagina iniziale con pulsanti che implementano molti [**dei**](shell.md) metodi dell'oggetto Shell.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-249">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="1ae1c-250">Alcuni di questi metodi implementano funzionalità nel menu **Start** e nel menu di scelta rapida della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-250">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


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



### <a name="security"></a><span data-ttu-id="1ae1c-251">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="1ae1c-251">Security</span></span>

<span data-ttu-id="1ae1c-252">Come applicazione, un'istanza HTA viene eseguita con un modello di sicurezza diverso rispetto a una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-252">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="1ae1c-253">**Per interagire con** una pagina Web che implementa la funzionalità degli oggetti shell, gli utenti devono abilitare l'opzione Inizializza e script per i controlli ActiveX non contrassegnati come sicuri per l'area di sicurezza in cui visualizzano la pagina.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-253">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="1ae1c-254">Oggetti cartella</span><span class="sxs-lookup"><span data-stu-id="1ae1c-254">Folder Objects</span></span>

<span data-ttu-id="1ae1c-255">[**L'oggetto Folder**](folder.md) rappresenta una cartella shell.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-255">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="1ae1c-256">È possibile usare i metodi esposti dall'oggetto Folder per:</span><span class="sxs-lookup"><span data-stu-id="1ae1c-256">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="1ae1c-257">Ottenere informazioni su una cartella.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-257">Get information about a folder.</span></span>
-   <span data-ttu-id="1ae1c-258">Creare sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-258">Create subfolders.</span></span>
-   <span data-ttu-id="1ae1c-259">Copiare e spostare gli oggetti file nella cartella .</span><span class="sxs-lookup"><span data-stu-id="1ae1c-259">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="1ae1c-260">[**L'oggetto FolderItem**](folderitem.md) rappresenta un elemento in una cartella shell.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-260">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="1ae1c-261">Le relative proprietà consentono di recuperare informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-261">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="1ae1c-262">È possibile usare i metodi esposti da questo oggetto per eseguire i verbi di un elemento o per recuperare informazioni sull'oggetto [**FolderItemVerbs di un**](folderitemverbs.md) elemento.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-262">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="1ae1c-263">[**L'oggetto FolderItems**](folderitems.md) rappresenta una raccolta di elementi in una cartella shell.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-263">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="1ae1c-264">I relativi metodi e proprietà consentono di recuperare informazioni sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-264">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="1ae1c-265">Nell'Visual Basic seguente viene illustrata la relazione tra diversi oggetti cartella e il modo in cui possono essere usati insieme.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-265">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="1ae1c-266">Quando l'utente fa clic sul pulsante di comando **denominato cmdGetPath**, il programma visualizza una finestra di dialogo che consente all'utente di selezionare una cartella da Computer locale , **dove** ssfDRIVES è il valore di enumerazione [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) per **Computer locale**.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-266">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="1ae1c-267">Quando l'utente sceglie una cartella, il percorso della cartella viene visualizzato nella casella di testo denominata **txtPath**.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-267">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


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



<span data-ttu-id="1ae1c-268">In VBScript questa funzione è leggermente diversa perché i valori di enumerazione [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) non sono disponibili nello script.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-268">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="1ae1c-269">Nell'esempio seguente viene illustrato l'equivalente VBScript dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="1ae1c-269">The following example shows the VBScript equivalent of the previous example.</span></span>


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



<span data-ttu-id="1ae1c-270">Nell'esempio JScript seguente, che è una traduzione diretta dell'esempio di VBScript precedente, si noti come le parentesi vuote '()' vengono usate per richiamare i metodi [**Items**](folder-items.md) [**e Item.**](folderitems-item.md)</span><span class="sxs-lookup"><span data-stu-id="1ae1c-270">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


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



 

 
