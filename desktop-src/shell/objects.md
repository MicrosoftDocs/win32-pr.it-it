---
description: In questa sezione vengono descritti gli oggetti di Windows implementati dalla Shell.
title: Oggetti Shell per gli script e Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529424"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a><span data-ttu-id="f39f8-103">Oggetti Shell per gli script e Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f39f8-103">Shell Objects for Scripting and Microsoft Visual Basic</span></span>

<span data-ttu-id="f39f8-104">In questa sezione vengono descritti gli oggetti di Windows implementati dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-104">This section describes the Windows objects implemented by the Shell.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f39f8-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f39f8-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f39f8-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="f39f8-106">Topic</span></span></th>
<th><span data-ttu-id="f39f8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f39f8-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f39f8-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-109">Consente a un client di gestire le impostazioni di quota disco globale del volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="f39f8-109">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="f39f8-110">Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> per gli script e le applicazioni basate su Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f39f8-110">This object makes the essential functionality of the <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> interface available to scripting and Microsoft Visual Basic-based applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-112">Consente a un amministratore di gestire le proprietà della quota disco di un volume.</span><span class="sxs-lookup"><span data-stu-id="f39f8-112">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="f39f8-113">Il file system NTFS consente a un amministratore di gestire l'utilizzo del disco in un volume condiviso allocando a ogni utente una quantità di spazio su disco specificata o un <em>limite di quota</em>.</span><span class="sxs-lookup"><span data-stu-id="f39f8-113">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or <em>quota limit</em>, to each user.</span></span> <span data-ttu-id="f39f8-114">È possibile utilizzare questo oggetto per impostare il limite di quota predefinito che verrà assegnato automaticamente a tutti i nuovi utenti.</span><span class="sxs-lookup"><span data-stu-id="f39f8-114">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-116">Riceve gli eventi di registrazione della finestra <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>ishellwindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-116">Receives <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> window registration events.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-117"><a href="folder.md"><strong>Cartella</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-117"><a href="folder.md"><strong>Folder</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-118">Rappresenta una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-118">Represents a Shell folder.</span></span> <span data-ttu-id="f39f8-119">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.</span><span class="sxs-lookup"><span data-stu-id="f39f8-119">This object contains properties and methods that allow you to retrieve information about the folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-120"><a href="folder2-object.md"><strong>Cartella2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-121">Estende l'oggetto <a href="folder.md"><strong>Folder</strong></a> per supportare le cartelle offline.</span><span class="sxs-lookup"><span data-stu-id="f39f8-121">Extends the <a href="folder.md"><strong>Folder</strong></a> object to support offline folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-123">Rappresenta un elemento in una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-123">Represents an item in a Shell folder.</span></span> <span data-ttu-id="f39f8-124">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="f39f8-124">This object contains properties and methods that allow you to retrieve information about the item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-126">Rappresenta la raccolta di elementi in una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-126">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="f39f8-127">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="f39f8-127">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-129">Estende l'oggetto <a href="folderitems.md"><strong>FolderItems</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-129">Extends the <a href="folderitems.md"><strong>FolderItems</strong></a> object.</span></span> <span data-ttu-id="f39f8-130">Supporta un metodo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="f39f8-130">It supports one additional method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-132">Estende l'oggetto <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-132">Extends the <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> object.</span></span> <span data-ttu-id="f39f8-133">Questo oggetto supporta un metodo e una proprietà aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f39f8-133">This object supports an additional method and property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-135">Rappresenta un singolo verbo disponibile per un elemento.</span><span class="sxs-lookup"><span data-stu-id="f39f8-135">Represents a single verb available to an item.</span></span> <span data-ttu-id="f39f8-136">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sul verbo.</span><span class="sxs-lookup"><span data-stu-id="f39f8-136">This object contains properties and methods that allow you to retrieve information about the verb.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-138">Rappresenta la raccolta di verbi per un elemento in una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-138">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="f39f8-139">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="f39f8-139">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-141">Rappresenta un oggetto nella shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-141">Represents an object in the Shell.</span></span> <span data-ttu-id="f39f8-142">Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-142">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="f39f8-143">Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-143">There are also methods to obtain other Shell-related objects.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f39f8-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-146">Estende l'oggetto <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> con un'ampia gamma di nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f39f8-146">Extends the <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> object with a variety of new functionality.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f39f8-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-149">Estende l'oggetto <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-149">Extends the <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> object.</span></span> <span data-ttu-id="f39f8-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supporta un nuovo metodo, oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch2</strong>.</span><span class="sxs-lookup"><span data-stu-id="f39f8-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supports one new method in addition to the properties and methods supported by <strong>IShellDispatch2</strong>.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f39f8-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-153">Estende l'oggetto <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-153">Extends the <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> object.</span></span> <span data-ttu-id="f39f8-154">Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supporta quattro metodi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f39f8-154">In addition to the properties and methods supported by <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supports four additional methods.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f39f8-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-157">Estende l'oggetto <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-157">Extends the <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> object.</span></span> <span data-ttu-id="f39f8-158">Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> aggiunge un metodo che visualizza le finestre aperte in uno stack 3D.</span><span class="sxs-lookup"><span data-stu-id="f39f8-158">In addition to the properties and methods supported by <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adds a method that displays open windows in a 3D stack.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f39f8-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-161">Estende l'oggetto <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-161">Extends the <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> object.</span></span> <span data-ttu-id="f39f8-162">Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> aggiunge un metodo che Visualizza il riquadro di ricerca delle app.</span><span class="sxs-lookup"><span data-stu-id="f39f8-162">In addition to the properties and methods supported by <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adds a method that displays the Apps Search pane.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f39f8-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-165">Estende l'oggetto <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> e supporta una proprietà aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="f39f8-165">Extends the <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> object and supports one additional property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-167">Estende l'oggetto <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> abilitando le pagine lato server ospitate in una procedura guidata per verificare che l'utente sia stato autenticato tramite un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f39f8-167">Extends the <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-168"><a href="shell.md"><strong>Shell</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-168"><a href="shell.md"><strong>Shell</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-169">Rappresenta gli oggetti nella shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-169">Represents the objects in the Shell.</span></span> <span data-ttu-id="f39f8-170">Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-170">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="f39f8-171">Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-171">There are also methods to obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-173">Estende l'oggetto <a href="folderitem.md"><strong>FolderItem</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f39f8-173">Extends the <a href="folderitem.md"><strong>FolderItem</strong></a> object.</span></span> <span data-ttu-id="f39f8-174">Oltre alle proprietà e ai metodi supportati da <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> dispone di due metodi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f39f8-174">In addition to the properties and methods supported by <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> has two additional methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-176">Rappresenta gli oggetti in una visualizzazione e fornisce le proprietà e i metodi utilizzati per ottenere informazioni sul contenuto della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f39f8-176">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-178">Invia gli eventi generati da un oggetto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> specificato ai gestori eventi <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="f39f8-178">Forwards the events fired by a specified <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> object to corresponding <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> event handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-180">Gestisce i collegamenti della shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-180">Manages Shell links.</span></span> <span data-ttu-id="f39f8-181">Questo oggetto rende la maggior parte delle funzionalità dell'interfaccia <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> disponibili per le applicazioni di scripting.</span><span class="sxs-lookup"><span data-stu-id="f39f8-181">This object makes much of the functionality of the <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> interface available to scripting applications.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-183">Implementato dalla Shell per aiutare gli script e Visual Basic sviluppatori a usare alcune delle funzionalità disponibili nella shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-183">Implemented by the Shell to help script and Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="f39f8-184">L'oggetto <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> non dispone di proprietà o eventi.</span><span class="sxs-lookup"><span data-stu-id="f39f8-184">The <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> object does not have any properties or events.</span></span> <span data-ttu-id="f39f8-185">Sono disponibili metodi per aggiungere elementi alla Shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-185">Methods are provided to add items to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f39f8-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-187">Rappresenta una raccolta di finestre aperte che appartengono alla Shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-187">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="f39f8-188">I metodi associati a questi oggetti possono controllare ed eseguire comandi all'interno della shell e ottenere altri oggetti correlati alla Shell.</span><span class="sxs-lookup"><span data-stu-id="f39f8-188">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f39f8-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="f39f8-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="f39f8-190">Espone metodi che consentono le pagine HTML ospitate in un'estensione della procedura guidata per comunicare con la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="f39f8-190">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




