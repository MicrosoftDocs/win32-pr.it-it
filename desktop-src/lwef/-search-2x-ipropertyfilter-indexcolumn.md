---
title: Proprietà IPropertyFilter IndexColumn (WdsSharedIDL. h)
description: Nome della colonna indicizzata della proprietà in base a cui filtrare.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Funzionalità dell'ambiente Windows legacy della Proprietà IndexColumn
- Proprietà IndexColumn caratteristiche dell'ambiente Windows legacy, interfaccia IPropertyFilter
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter, Proprietà IndexColumn
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048314"
---
# <a name="ipropertyfilterindexcolumn-property"></a><span data-ttu-id="51654-106">Proprietà IPropertyFilter:: IndexColumn</span><span class="sxs-lookup"><span data-stu-id="51654-106">IPropertyFilter::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="51654-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="51654-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="51654-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="51654-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="51654-109">Nome della colonna indicizzata della proprietà in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="51654-109">Indexed column name of the property to filter by.</span></span>

<span data-ttu-id="51654-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="51654-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="51654-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51654-111">Syntax</span></span>


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="51654-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="51654-112">Property value</span></span>

<span data-ttu-id="51654-113">Imposta la proprietà della colonna.</span><span class="sxs-lookup"><span data-stu-id="51654-113">Sets the Column property.</span></span>

## <a name="requirements"></a><span data-ttu-id="51654-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51654-114">Requirements</span></span>



| <span data-ttu-id="51654-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="51654-115">Requirement</span></span> | <span data-ttu-id="51654-116">Valore</span><span class="sxs-lookup"><span data-stu-id="51654-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="51654-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51654-117">Minimum supported client</span></span><br/> | <span data-ttu-id="51654-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="51654-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="51654-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51654-119">Minimum supported server</span></span><br/> | <span data-ttu-id="51654-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="51654-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="51654-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="51654-121">Redistributable</span></span><br/>          | <span data-ttu-id="51654-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="51654-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="51654-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51654-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="51654-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="51654-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





