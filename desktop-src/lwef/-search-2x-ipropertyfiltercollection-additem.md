---
title: Proprietà AddItem IPropertyFilterCollection (WdsSharedIDL. h)
description: Aggiunge un nuovo filtro alla raccolta.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- Funzionalità di ambiente Windows legacy della proprietà AddItem
- Caratteristiche dell'ambiente Windows legacy della proprietà AddItem, interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, proprietà AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048220"
---
# <a name="ipropertyfiltercollectionadditem-property"></a><span data-ttu-id="3ac5d-106">Proprietà IPropertyFilterCollection:: AddItem</span><span class="sxs-lookup"><span data-stu-id="3ac5d-106">IPropertyFilterCollection::AddItem property</span></span>

> [!NOTE]
> <span data-ttu-id="3ac5d-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3ac5d-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="3ac5d-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac5d-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="3ac5d-109">Aggiunge un nuovo filtro alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="3ac5d-109">Adds a new filter to the collection.</span></span>

<span data-ttu-id="3ac5d-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3ac5d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac5d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ac5d-111">Syntax</span></span>


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="3ac5d-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3ac5d-112">Property value</span></span>

<span data-ttu-id="3ac5d-113">Restituisce un puntatore all'indirizzo del nuovo filtro.</span><span class="sxs-lookup"><span data-stu-id="3ac5d-113">returns a pointer to the address for the new filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac5d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ac5d-114">Requirements</span></span>



| <span data-ttu-id="3ac5d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac5d-115">Requirement</span></span> | <span data-ttu-id="3ac5d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3ac5d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac5d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ac5d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac5d-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ac5d-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3ac5d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ac5d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac5d-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="3ac5d-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3ac5d-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3ac5d-121">Redistributable</span></span><br/>          | <span data-ttu-id="3ac5d-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="3ac5d-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="3ac5d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ac5d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ac5d-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac5d-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





