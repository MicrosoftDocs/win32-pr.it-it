---
description: Rappresenta un elemento in una cartella shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.
title: Oggetto FolderItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a8b9309e7bd1c8cbcc05360c076db085d0f8b991
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840982"
---
# <a name="folderitem-object"></a><span data-ttu-id="3a38a-104">Oggetto FolderItem</span><span class="sxs-lookup"><span data-stu-id="3a38a-104">FolderItem object</span></span>

<span data-ttu-id="3a38a-105">Rappresenta un elemento in una cartella shell.</span><span class="sxs-lookup"><span data-stu-id="3a38a-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="3a38a-106">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="3a38a-107">Membri</span><span class="sxs-lookup"><span data-stu-id="3a38a-107">Members</span></span>

<span data-ttu-id="3a38a-108">**L'oggetto FolderItem** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3a38a-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="3a38a-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="3a38a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a38a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3a38a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a38a-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3a38a-111">Methods</span></span>

<span data-ttu-id="3a38a-112">**L'oggetto FolderItem** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3a38a-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="3a38a-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="3a38a-113">Method</span></span>                                      | <span data-ttu-id="3a38a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a38a-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a38a-115">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="3a38a-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="3a38a-116">Esegue un verbo sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="3a38a-117">**Verbi**</span><span class="sxs-lookup"><span data-stu-id="3a38a-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="3a38a-118">Recupera l'oggetto [**FolderItemVerbs**](folderitemverbs.md) dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="3a38a-119">Questo oggetto è la raccolta di verbi che possono essere eseguiti sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3a38a-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3a38a-120">Properties</span></span>

<span data-ttu-id="3a38a-121">**L'oggetto FolderItem** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a38a-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="3a38a-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3a38a-122">Property</span></span>                                                   | <span data-ttu-id="3a38a-123">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="3a38a-123">Access type</span></span>           | <span data-ttu-id="3a38a-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a38a-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a38a-125">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="3a38a-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="3a38a-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-126">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-127">Contiene [**l'oggetto Application**](folderitem-application.md) dell'elemento cartella.</span><span class="sxs-lookup"><span data-stu-id="3a38a-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="3a38a-128">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="3a38a-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="3a38a-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-129">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-130">Contiene l'oggetto [**Folder**](folder.md) dell'elemento, se l'elemento è una cartella.</span><span class="sxs-lookup"><span data-stu-id="3a38a-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="3a38a-131">**GetLink**</span><span class="sxs-lookup"><span data-stu-id="3a38a-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="3a38a-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-132">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-133">Contiene l'oggetto [**ShellLinkObject dell'elemento,**](shelllinkobject-object.md) se l'elemento è un collegamento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="3a38a-134">**IsBrowsable**</span><span class="sxs-lookup"><span data-stu-id="3a38a-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="3a38a-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-135">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-136">Indica se l'elemento può essere ospitato all'interno di un browser o Esplora risorse frame.</span><span class="sxs-lookup"><span data-stu-id="3a38a-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="3a38a-137">**IsFileSystem**</span><span class="sxs-lookup"><span data-stu-id="3a38a-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="3a38a-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-138">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-139">Indica se l'elemento fa parte del file system.</span><span class="sxs-lookup"><span data-stu-id="3a38a-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="3a38a-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="3a38a-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="3a38a-141">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-141">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-142">Indica se l'elemento è una cartella.</span><span class="sxs-lookup"><span data-stu-id="3a38a-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="3a38a-143">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="3a38a-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="3a38a-144">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-144">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-145">Indica se l'elemento è un collegamento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="3a38a-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="3a38a-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="3a38a-147">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3a38a-147">Read/write</span></span><br/> | <span data-ttu-id="3a38a-148">Imposta o ottiene la data e l'ora dell'ultima modifica di un file.</span><span class="sxs-lookup"><span data-stu-id="3a38a-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="3a38a-149">[**ModifyDate**](folderitem-modifydate.md) può essere usato per recuperare la data e l'ora dell'ultima modifica di una cartella, ma non è possibile impostarla.</span><span class="sxs-lookup"><span data-stu-id="3a38a-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="3a38a-150">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3a38a-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="3a38a-151">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3a38a-151">Read/write</span></span><br/> | <span data-ttu-id="3a38a-152">Imposta o ottiene il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="3a38a-153">**Padre**</span><span class="sxs-lookup"><span data-stu-id="3a38a-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="3a38a-154">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-154">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-155">Ottiene un oggetto che rappresenta l'elemento padre dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="3a38a-156">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="3a38a-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="3a38a-157">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-157">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-158">Contiene il percorso completo e il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="3a38a-159">**Dimensione**</span><span class="sxs-lookup"><span data-stu-id="3a38a-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="3a38a-160">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-160">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-161">Contiene le dimensioni dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="3a38a-162">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3a38a-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="3a38a-163">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a38a-163">Read-only</span></span><br/>  | <span data-ttu-id="3a38a-164">Contiene una rappresentazione di stringa del tipo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3a38a-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="3a38a-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a38a-165">Requirements</span></span>



| <span data-ttu-id="3a38a-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a38a-166">Requirement</span></span> | <span data-ttu-id="3a38a-167">Valore</span><span class="sxs-lookup"><span data-stu-id="3a38a-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a38a-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a38a-168">Minimum supported client</span></span><br/> | <span data-ttu-id="3a38a-169">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3a38a-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3a38a-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a38a-170">Minimum supported server</span></span><br/> | <span data-ttu-id="3a38a-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a38a-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3a38a-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a38a-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a38a-173"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="3a38a-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3a38a-174">Idl</span><span class="sxs-lookup"><span data-stu-id="3a38a-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a38a-175"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a38a-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3a38a-176">DLL</span><span class="sxs-lookup"><span data-stu-id="3a38a-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a38a-177"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3a38a-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




