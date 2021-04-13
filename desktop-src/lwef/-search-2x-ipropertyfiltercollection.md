---
title: Interfaccia IPropertyFilterCollection (WdsSharedIDL. h)
description: Espone le proprietà della raccolta restituita in base alla query inviata.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, descritte
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340853"
---
# <a name="ipropertyfiltercollection-interface"></a><span data-ttu-id="92654-105">Interfaccia IPropertyFilterCollection</span><span class="sxs-lookup"><span data-stu-id="92654-105">IPropertyFilterCollection interface</span></span>

> [!NOTE]
> <span data-ttu-id="92654-106">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="92654-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="92654-107">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="92654-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="92654-108">Espone le proprietà della raccolta restituita in base alla query inviata.</span><span class="sxs-lookup"><span data-stu-id="92654-108">Exposes properties of the returned collection based on the query submitted.</span></span>

## <a name="members"></a><span data-ttu-id="92654-109">Membri</span><span class="sxs-lookup"><span data-stu-id="92654-109">Members</span></span>

<span data-ttu-id="92654-110">L'interfaccia **IPropertyFilterCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="92654-110">The **IPropertyFilterCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="92654-111">**IPropertyFilterCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="92654-111">**IPropertyFilterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="92654-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="92654-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92654-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="92654-113">Properties</span></span>

<span data-ttu-id="92654-114">L'interfaccia **IPropertyFilterCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="92654-114">The **IPropertyFilterCollection** interface has these properties.</span></span>



| <span data-ttu-id="92654-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="92654-115">Property</span></span>                                                                         | <span data-ttu-id="92654-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="92654-116">Access type</span></span>           | <span data-ttu-id="92654-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92654-117">Description</span></span>                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="92654-118">**AddItem**</span><span class="sxs-lookup"><span data-stu-id="92654-118">**AddItem**</span></span>](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | <span data-ttu-id="92654-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="92654-119">Read-only</span></span><br/>  | <span data-ttu-id="92654-120">Aggiunge un nuovo filtro alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="92654-120">Adds a new filter to the collection.</span></span> <br/>             |
| [<span data-ttu-id="92654-121">**deselezionare**</span><span class="sxs-lookup"><span data-stu-id="92654-121">**clear**</span></span>](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | <span data-ttu-id="92654-122">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="92654-122">Write-only</span></span><br/> | <span data-ttu-id="92654-123">Cancella la raccolta.</span><span class="sxs-lookup"><span data-stu-id="92654-123">Clears the collection.</span></span> <br/>                           |
| [<span data-ttu-id="92654-124">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="92654-124">**Count**</span></span>](-search-2x-ipropertyfiltercollection-count.md)<br/>           | <span data-ttu-id="92654-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="92654-125">Read-only</span></span><br/>  | <span data-ttu-id="92654-126">Numero di filtri nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="92654-126">Number of filters in the collection.</span></span> <br/>             |
| [<span data-ttu-id="92654-127">**GetITem**</span><span class="sxs-lookup"><span data-stu-id="92654-127">**GetITem**</span></span>](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | <span data-ttu-id="92654-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="92654-128">Read/write</span></span><br/> | <span data-ttu-id="92654-129">Restituisce un filtro specifico all'interno della raccolta.</span><span class="sxs-lookup"><span data-stu-id="92654-129">Returns a specific filter within the collection.</span></span> <br/> |
| [<span data-ttu-id="92654-130">**RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="92654-130">**RemoveItem**</span></span>](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | <span data-ttu-id="92654-131">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="92654-131">Write-only</span></span><br/> | <span data-ttu-id="92654-132">Rimuove un filtro specifico per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="92654-132">Removes a specific filter to the collection.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="92654-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="92654-133">Remarks</span></span>

<span data-ttu-id="92654-134">Queste proprietà vengono utilizzate per filtrare la raccolta restituita dalla query.</span><span class="sxs-lookup"><span data-stu-id="92654-134">These properties are used to filter collection returned by the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="92654-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92654-135">Requirements</span></span>



| <span data-ttu-id="92654-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="92654-136">Requirement</span></span> | <span data-ttu-id="92654-137">Valore</span><span class="sxs-lookup"><span data-stu-id="92654-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="92654-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92654-138">Minimum supported client</span></span><br/> | <span data-ttu-id="92654-139">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="92654-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="92654-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92654-140">Minimum supported server</span></span><br/> | <span data-ttu-id="92654-141">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="92654-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="92654-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="92654-142">Redistributable</span></span><br/>          | <span data-ttu-id="92654-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="92654-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="92654-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92654-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="92654-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="92654-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

