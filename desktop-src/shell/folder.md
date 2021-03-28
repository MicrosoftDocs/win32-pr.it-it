---
description: Rappresenta una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Oggetto Folder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524490"
---
# <a name="folder-object"></a><span data-ttu-id="04538-104">Oggetto Folder</span><span class="sxs-lookup"><span data-stu-id="04538-104">Folder object</span></span>

<span data-ttu-id="04538-105">Rappresenta una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="04538-105">Represents a Shell folder.</span></span> <span data-ttu-id="04538-106">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.</span><span class="sxs-lookup"><span data-stu-id="04538-106">This object contains properties and methods that allow you to retrieve information about the folder.</span></span>

## <a name="members"></a><span data-ttu-id="04538-107">Membri</span><span class="sxs-lookup"><span data-stu-id="04538-107">Members</span></span>

<span data-ttu-id="04538-108">L'oggetto **cartella** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="04538-108">The **Folder** object has these types of members:</span></span>

-   [<span data-ttu-id="04538-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="04538-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="04538-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04538-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04538-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="04538-111">Methods</span></span>

<span data-ttu-id="04538-112">L'oggetto **Folder** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="04538-112">The **Folder** object has these methods.</span></span>



| <span data-ttu-id="04538-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="04538-113">Method</span></span>                                      | <span data-ttu-id="04538-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04538-114">Description</span></span>                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04538-115">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="04538-115">**CopyHere**</span></span>](folder-copyhere.md)         | <span data-ttu-id="04538-116">Copia un elemento o elementi in una cartella.</span><span class="sxs-lookup"><span data-stu-id="04538-116">Copies an item or items to a folder.</span></span><br/>                                                                            |
| [<span data-ttu-id="04538-117">**GetDetailsOf**</span><span class="sxs-lookup"><span data-stu-id="04538-117">**GetDetailsOf**</span></span>](folder-getdetailsof.md) | <span data-ttu-id="04538-118">Recupera i dettagli relativi a un elemento in una cartella.</span><span class="sxs-lookup"><span data-stu-id="04538-118">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="04538-119">Ad esempio, le dimensioni, il tipo o l'ora dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="04538-119">For example, its size, type, or the time of its last modification.</span></span><br/> |
| [<span data-ttu-id="04538-120">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="04538-120">**Items**</span></span>](folder-items.md)               | <span data-ttu-id="04538-121">Recupera un oggetto [**FolderItems**](folderitems.md) che rappresenta la raccolta di elementi nella cartella.</span><span class="sxs-lookup"><span data-stu-id="04538-121">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span><br/>    |
| [<span data-ttu-id="04538-122">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="04538-122">**MoveHere**</span></span>](folder-movehere.md)         | <span data-ttu-id="04538-123">Sposta un elemento o elementi in questa cartella.</span><span class="sxs-lookup"><span data-stu-id="04538-123">Moves an item or items to this folder.</span></span><br/>                                                                          |
| [<span data-ttu-id="04538-124">**NewFolder**</span><span class="sxs-lookup"><span data-stu-id="04538-124">**NewFolder**</span></span>](folder-newfolder.md)       | <span data-ttu-id="04538-125">Crea una nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="04538-125">Creates a new folder.</span></span><br/>                                                                                           |
| [<span data-ttu-id="04538-126">**ParseName**</span><span class="sxs-lookup"><span data-stu-id="04538-126">**ParseName**</span></span>](folder-parsename.md)       | <span data-ttu-id="04538-127">Crea e restituisce un oggetto [**FolderItem**](folderitem.md) che rappresenta un elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="04538-127">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="04538-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04538-128">Properties</span></span>

<span data-ttu-id="04538-129">L'oggetto **Folder** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="04538-129">The **Folder** object has these properties.</span></span>



| <span data-ttu-id="04538-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04538-130">Property</span></span>                                               | <span data-ttu-id="04538-131">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="04538-131">Access type</span></span>          | <span data-ttu-id="04538-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04538-132">Description</span></span>                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [<span data-ttu-id="04538-133">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="04538-133">**Application**</span></span>](folder-application.md)<br/>   | <span data-ttu-id="04538-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="04538-134">Read-only</span></span><br/> | <span data-ttu-id="04538-135">Contiene l'oggetto applicazione della cartella.</span><span class="sxs-lookup"><span data-stu-id="04538-135">Contains the folder's Application object.</span></span><br/> |
| [<span data-ttu-id="04538-136">**Padre**</span><span class="sxs-lookup"><span data-stu-id="04538-136">**Parent**</span></span>](folder-parent.md)<br/>             | <span data-ttu-id="04538-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="04538-137">Read-only</span></span><br/> | <span data-ttu-id="04538-138">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="04538-138">Not implemented.</span></span><br/>                          |
| [<span data-ttu-id="04538-139">**ParentFolder**</span><span class="sxs-lookup"><span data-stu-id="04538-139">**ParentFolder**</span></span>](folder-parentfolder.md)<br/> | <span data-ttu-id="04538-140">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="04538-140">Read-only</span></span><br/> | <span data-ttu-id="04538-141">Contiene l'oggetto **cartella** padre.</span><span class="sxs-lookup"><span data-stu-id="04538-141">Contains the parent **Folder** object.</span></span><br/>    |
| [<span data-ttu-id="04538-142">**Titolo**</span><span class="sxs-lookup"><span data-stu-id="04538-142">**Title**</span></span>](folder-title.md)<br/>               | <span data-ttu-id="04538-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="04538-143">Read-only</span></span><br/> | <span data-ttu-id="04538-144">Contiene il titolo della cartella.</span><span class="sxs-lookup"><span data-stu-id="04538-144">Contains the title of the folder.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="04538-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="04538-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="04538-146">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="04538-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="04538-147">Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="04538-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="04538-148">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="04538-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04538-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04538-149">Requirements</span></span>



| <span data-ttu-id="04538-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="04538-150">Requirement</span></span> | <span data-ttu-id="04538-151">Valore</span><span class="sxs-lookup"><span data-stu-id="04538-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04538-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04538-152">Minimum supported client</span></span><br/> | <span data-ttu-id="04538-153">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="04538-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="04538-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04538-154">Minimum supported server</span></span><br/> | <span data-ttu-id="04538-155">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04538-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04538-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04538-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="04538-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04538-157"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="04538-158">IDL</span><span class="sxs-lookup"><span data-stu-id="04538-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04538-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04538-159"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




