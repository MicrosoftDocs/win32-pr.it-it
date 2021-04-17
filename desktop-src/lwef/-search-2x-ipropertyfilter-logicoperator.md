---
title: Proprietà IPropertyFilter LogicOperator (WdsSharedIDL. h)
description: Operatore logico da utilizzare quando si applica un filtro.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà LogicOperator
- Proprietà LogicOperator caratteristiche dell'ambiente Windows legacy, interfaccia IPropertyFilter
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter, proprietà LogicOperator
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c514ae6231a9d83063b4a294680bdd3949c91102
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479174"
---
# <a name="ipropertyfilterlogicoperator-property"></a><span data-ttu-id="0e962-106">Proprietà IPropertyFilter:: LogicOperator</span><span class="sxs-lookup"><span data-stu-id="0e962-106">IPropertyFilter::LogicOperator property</span></span>

> [!NOTE]
> <span data-ttu-id="0e962-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e962-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0e962-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="0e962-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0e962-109">Operatore logico da utilizzare quando si applica un filtro.</span><span class="sxs-lookup"><span data-stu-id="0e962-109">Logic Operator to use when applying a filter.</span></span>

<span data-ttu-id="0e962-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0e962-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e962-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e962-111">Syntax</span></span>


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a><span data-ttu-id="0e962-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0e962-112">Property value</span></span>

<span data-ttu-id="0e962-113">Imposta il tipo di operatore logico.</span><span class="sxs-lookup"><span data-stu-id="0e962-113">Sets the logic operator type.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e962-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e962-114">Requirements</span></span>



| <span data-ttu-id="0e962-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e962-115">Requirement</span></span> | <span data-ttu-id="0e962-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0e962-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e962-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e962-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0e962-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e962-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0e962-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e962-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0e962-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="0e962-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0e962-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0e962-121">Redistributable</span></span><br/>          | <span data-ttu-id="0e962-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="0e962-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="0e962-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e962-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e962-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e962-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





