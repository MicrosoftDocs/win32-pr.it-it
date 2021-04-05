---
title: Proprietà Count IPropertyFilterCollection (WdsSharedIDL. h)
description: Numero di filtri nella raccolta.
ms.assetid: 9d656f06-eb1d-4cc6-9096-252f0fc65ae2
keywords:
- Proprietà Count funzionalità dell'ambiente Windows legacy
- Proprietà Count funzionalità dell'ambiente Windows legacy, interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, proprietà Count
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.Count
- IPropertyFilterCollection.get_Count
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258a2ca8089cecb8e2e15fbe7e9e92ce1ed3468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741047"
---
# <a name="ipropertyfiltercollectioncount-property"></a><span data-ttu-id="afa12-106">Proprietà IPropertyFilterCollection:: count</span><span class="sxs-lookup"><span data-stu-id="afa12-106">IPropertyFilterCollection::Count property</span></span>

> [!NOTE]
> <span data-ttu-id="afa12-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="afa12-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="afa12-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="afa12-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="afa12-109">Numero di filtri nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="afa12-109">Number of filters in the collection.</span></span>

<span data-ttu-id="afa12-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="afa12-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa12-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afa12-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="afa12-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="afa12-112">Property value</span></span>

<span data-ttu-id="afa12-113">Restituisce un puntatore al numero di filtri nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="afa12-113">returns a pointer to the number of filters in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa12-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afa12-114">Requirements</span></span>



| <span data-ttu-id="afa12-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa12-115">Requirement</span></span> | <span data-ttu-id="afa12-116">Valore</span><span class="sxs-lookup"><span data-stu-id="afa12-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa12-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afa12-117">Minimum supported client</span></span><br/> | <span data-ttu-id="afa12-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="afa12-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="afa12-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afa12-119">Minimum supported server</span></span><br/> | <span data-ttu-id="afa12-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="afa12-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="afa12-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="afa12-121">Redistributable</span></span><br/>          | <span data-ttu-id="afa12-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="afa12-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="afa12-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afa12-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa12-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="afa12-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





