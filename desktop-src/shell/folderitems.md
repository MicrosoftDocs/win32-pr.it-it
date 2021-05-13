---
description: Rappresenta la raccolta di elementi in una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.
title: Oggetto FolderItems (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840652"
---
# <a name="folderitems-object"></a><span data-ttu-id="53167-104">Oggetto FolderItems</span><span class="sxs-lookup"><span data-stu-id="53167-104">FolderItems object</span></span>

<span data-ttu-id="53167-105">Rappresenta la raccolta di elementi in una cartella Shell.</span><span class="sxs-lookup"><span data-stu-id="53167-105">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="53167-106">Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="53167-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="53167-107">Membri</span><span class="sxs-lookup"><span data-stu-id="53167-107">Members</span></span>

<span data-ttu-id="53167-108">**L'oggetto FolderItems** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="53167-108">The **FolderItems** object has these types of members:</span></span>

-   [<span data-ttu-id="53167-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="53167-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="53167-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53167-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="53167-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="53167-111">Methods</span></span>

<span data-ttu-id="53167-112">**L'oggetto FolderItems** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="53167-112">The **FolderItems** object has these methods.</span></span>



| <span data-ttu-id="53167-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="53167-113">Method</span></span>                                    | <span data-ttu-id="53167-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53167-114">Description</span></span>                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53167-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="53167-115">**\_NewEnum**</span></span>](folderitems--newenum.md) | <span data-ttu-id="53167-116">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="53167-116">Not implemented.</span></span><br/>                                                                              |
| [<span data-ttu-id="53167-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="53167-117">**Item**</span></span>](folderitems-item.md)          | <span data-ttu-id="53167-118">Recupera [**l'oggetto FolderItem**](folderitem.md) per un elemento specificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="53167-118">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="53167-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53167-119">Properties</span></span>

<span data-ttu-id="53167-120">**L'oggetto FolderItems** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="53167-120">The **FolderItems** object has these properties.</span></span>



| <span data-ttu-id="53167-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53167-121">Property</span></span>                                                  | <span data-ttu-id="53167-122">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="53167-122">Access type</span></span>          | <span data-ttu-id="53167-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53167-123">Description</span></span>                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53167-124">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="53167-124">**Application**</span></span>](folderitems-application.md)<br/> | <span data-ttu-id="53167-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="53167-125">Read-only</span></span><br/> | <span data-ttu-id="53167-126">Contiene [**l'oggetto Application**](folderitems-application.md) della raccolta di elementi cartella.</span><span class="sxs-lookup"><span data-stu-id="53167-126">Contains the [**Application**](folderitems-application.md) object of the folder items collection.</span></span><br/> |
| [<span data-ttu-id="53167-127">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="53167-127">**Count**</span></span>](folderitems-count.md)<br/>             | <span data-ttu-id="53167-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="53167-128">Read-only</span></span><br/> | <span data-ttu-id="53167-129">Contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="53167-129">Contains the number of items in the collection.</span></span><br/>                                                    |
| [<span data-ttu-id="53167-130">**Padre**</span><span class="sxs-lookup"><span data-stu-id="53167-130">**Parent**</span></span>](folderitems-parent.md)<br/>           | <span data-ttu-id="53167-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="53167-131">Read-only</span></span><br/> | <span data-ttu-id="53167-132">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="53167-132">Not implemented.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="53167-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53167-133">Requirements</span></span>



| <span data-ttu-id="53167-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="53167-134">Requirement</span></span> | <span data-ttu-id="53167-135">Valore</span><span class="sxs-lookup"><span data-stu-id="53167-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53167-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53167-136">Minimum supported client</span></span><br/> | <span data-ttu-id="53167-137">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="53167-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53167-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53167-138">Minimum supported server</span></span><br/> | <span data-ttu-id="53167-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="53167-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53167-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53167-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="53167-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="53167-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="53167-142">Idl</span><span class="sxs-lookup"><span data-stu-id="53167-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53167-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="53167-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="53167-144">DLL</span><span class="sxs-lookup"><span data-stu-id="53167-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53167-145"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="53167-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




