---
title: Proprietà GetItem di IPropertyFilterCollection (WdsSharedIDL. h)
description: Restituisce un filtro specifico all'interno della raccolta.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Proprietà GetItem funzionalità dell'ambiente Windows legacy
- Proprietà GetItem funzionalità dell'ambiente Windows legacy, interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, proprietà GetItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964069"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a><span data-ttu-id="9c7ec-106">Proprietà IPropertyFilterCollection:: GetItem</span><span class="sxs-lookup"><span data-stu-id="9c7ec-106">IPropertyFilterCollection::GetITem property</span></span>

> [!NOTE]
> <span data-ttu-id="9c7ec-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9c7ec-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="9c7ec-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9c7ec-109">Restituisce un filtro specifico all'interno della raccolta.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-109">Returns a specific filter within the collection.</span></span>

<span data-ttu-id="9c7ec-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c7ec-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c7ec-111">Syntax</span></span>


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="9c7ec-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9c7ec-112">Property value</span></span>

<span data-ttu-id="9c7ec-113">Imposta l'indirizzo del filtro.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-113">Sets the address of the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c7ec-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c7ec-114">Requirements</span></span>



| <span data-ttu-id="9c7ec-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c7ec-115">Requirement</span></span> | <span data-ttu-id="9c7ec-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9c7ec-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7ec-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c7ec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c7ec-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c7ec-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9c7ec-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c7ec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c7ec-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="9c7ec-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9c7ec-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9c7ec-121">Redistributable</span></span><br/>          | <span data-ttu-id="9c7ec-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="9c7ec-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9c7ec-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c7ec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c7ec-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c7ec-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





