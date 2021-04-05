---
title: Proprietà IPropertyFilterCollection RemoveItem (WdsSharedIDL. h)
description: Rimuove un filtro specifico per la raccolta.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà RemoveItem
- Proprietà RemoveItem caratteristiche dell'ambiente Windows legacy, interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, proprietà RemoveItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742327"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a><span data-ttu-id="9d19f-106">Proprietà IPropertyFilterCollection:: RemoveItem</span><span class="sxs-lookup"><span data-stu-id="9d19f-106">IPropertyFilterCollection::RemoveItem property</span></span>

> [!NOTE]
> <span data-ttu-id="9d19f-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9d19f-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9d19f-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="9d19f-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9d19f-109">Rimuove un filtro specifico per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="9d19f-109">Removes a specific filter to the collection.</span></span>

<span data-ttu-id="9d19f-110">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="9d19f-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d19f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d19f-111">Syntax</span></span>


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a><span data-ttu-id="9d19f-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9d19f-112">Property value</span></span>

<span data-ttu-id="9d19f-113">Accetta un puntatore all'indice per il filtro da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9d19f-113">Accepts a pointer to the index for the filter to be removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d19f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d19f-114">Requirements</span></span>



| <span data-ttu-id="9d19f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d19f-115">Requirement</span></span> | <span data-ttu-id="9d19f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9d19f-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d19f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d19f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d19f-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d19f-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9d19f-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d19f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d19f-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="9d19f-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9d19f-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9d19f-121">Redistributable</span></span><br/>          | <span data-ttu-id="9d19f-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="9d19f-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9d19f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d19f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d19f-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d19f-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





