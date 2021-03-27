---
description: Rappresenta la raccolta di verbi per un elemento in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.
title: Oggetto FolderItemVerbs (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: 651f439ea34a55203da852f2907a27ba87bdd275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881586"
---
# <a name="folderitemverbs-object"></a><span data-ttu-id="bde93-104">Oggetto FolderItemVerbs</span><span class="sxs-lookup"><span data-stu-id="bde93-104">FolderItemVerbs object</span></span>

<span data-ttu-id="bde93-105">Rappresenta la raccolta di verbi per un elemento in una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="bde93-105">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="bde93-106">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bde93-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="bde93-107">Membri</span><span class="sxs-lookup"><span data-stu-id="bde93-107">Members</span></span>

<span data-ttu-id="bde93-108">L'oggetto **folderitemverbs** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bde93-108">The **FolderItemVerbs** object has these types of members:</span></span>

-   [<span data-ttu-id="bde93-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="bde93-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="bde93-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bde93-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bde93-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="bde93-111">Methods</span></span>

<span data-ttu-id="bde93-112">L'oggetto **folderitemverbs** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bde93-112">The **FolderItemVerbs** object has these methods.</span></span>



| <span data-ttu-id="bde93-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="bde93-113">Method</span></span>                                        | <span data-ttu-id="bde93-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bde93-114">Description</span></span>                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bde93-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="bde93-115">**\_NewEnum**</span></span>](folderitemverbs--newenum.md) | <span data-ttu-id="bde93-116">Crea e restituisce un nuovo oggetto **folderitemverbs** che è una copia di questo oggetto folderitemverbs.</span><span class="sxs-lookup"><span data-stu-id="bde93-116">Creates and returns a new **FolderItemVerbs** object that is a copy of this FolderItemVerbs object.</span></span><br/>   |
| [<span data-ttu-id="bde93-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bde93-117">**Item**</span></span>](folderitemverbs-item.md)          | <span data-ttu-id="bde93-118">Recupera l'oggetto [**FolderItemVerb**](folderitemverb.md) per un elemento specificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="bde93-118">Retrieves the [**FolderItemVerb**](folderitemverb.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bde93-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bde93-119">Properties</span></span>

<span data-ttu-id="bde93-120">L'oggetto **folderitemverbs** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bde93-120">The **FolderItemVerbs** object has these properties.</span></span>



| <span data-ttu-id="bde93-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bde93-121">Property</span></span>                                                      | <span data-ttu-id="bde93-122">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="bde93-122">Access type</span></span>          | <span data-ttu-id="bde93-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bde93-123">Description</span></span>                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="bde93-124">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="bde93-124">**Application**</span></span>](folderitemverbs-application.md)<br/> | <span data-ttu-id="bde93-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="bde93-125">Read-only</span></span><br/> | <span data-ttu-id="bde93-126">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="bde93-126">Not implemented.</span></span><br/>                                |
| [<span data-ttu-id="bde93-127">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="bde93-127">**Count**</span></span>](folderitemverbs-count.md)<br/>             | <span data-ttu-id="bde93-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="bde93-128">Read-only</span></span><br/> | <span data-ttu-id="bde93-129">Contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="bde93-129">Contains the number of items in the collection.</span></span><br/> |
| [<span data-ttu-id="bde93-130">**Padre**</span><span class="sxs-lookup"><span data-stu-id="bde93-130">**Parent**</span></span>](folderitemverbs-parent.md)<br/>           | <span data-ttu-id="bde93-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="bde93-131">Read-only</span></span><br/> | <span data-ttu-id="bde93-132">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="bde93-132">Not implemented.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="bde93-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bde93-133">Requirements</span></span>



| <span data-ttu-id="bde93-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bde93-134">Requirement</span></span> | <span data-ttu-id="bde93-135">Valore</span><span class="sxs-lookup"><span data-stu-id="bde93-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde93-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bde93-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bde93-137">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bde93-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bde93-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bde93-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bde93-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bde93-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bde93-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bde93-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bde93-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bde93-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bde93-142">IDL</span><span class="sxs-lookup"><span data-stu-id="bde93-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bde93-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bde93-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bde93-144">DLL</span><span class="sxs-lookup"><span data-stu-id="bde93-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bde93-145"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="bde93-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




