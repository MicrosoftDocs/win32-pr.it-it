---
description: Recupera gli identificatori per i quali sono presenti dati della proprietà.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'Metodo IContextNode:: GetPropertyDataIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307435"
---
# <a name="icontextnodegetpropertydataids-method"></a><span data-ttu-id="c580c-103">Metodo IContextNode:: GetPropertyDataIds</span><span class="sxs-lookup"><span data-stu-id="c580c-103">IContextNode::GetPropertyDataIds method</span></span>

<span data-ttu-id="c580c-104">Recupera gli identificatori per i quali sono presenti dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c580c-104">Retrieves the identifiers for which there is property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c580c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c580c-105">Syntax</span></span>


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a><span data-ttu-id="c580c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c580c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c580c-107">*pulGuidCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c580c-107">*pulGuidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c580c-108">Numero di proprietà.</span><span class="sxs-lookup"><span data-stu-id="c580c-108">The number of properties.</span></span>

</dd> <dt>

<span data-ttu-id="c580c-109">*ppGuids* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c580c-109">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c580c-110">Identificatori per i quali sono presenti dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c580c-110">The identifiers for which there is property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c580c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c580c-111">Return value</span></span>

<span data-ttu-id="c580c-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c580c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c580c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c580c-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c580c-114">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppGuids* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="c580c-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="c580c-115">Questo metodo restituisce gli identificatori specifici dell'applicazione per i dati delle proprietà che sono stati aggiunti.</span><span class="sxs-lookup"><span data-stu-id="c580c-115">This method returns the application-specific identifiers for property data that has been added.</span></span> <span data-ttu-id="c580c-116">Restituisce inoltre gli identificatori per i dati della proprietà interna, descritti dalle costanti delle [proprietà del nodo di contesto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="c580c-116">It also returns the identifiers for the internal property data, which are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="c580c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c580c-117">Requirements</span></span>



| <span data-ttu-id="c580c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c580c-118">Requirement</span></span> | <span data-ttu-id="c580c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c580c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c580c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c580c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c580c-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c580c-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c580c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c580c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c580c-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c580c-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c580c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c580c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c580c-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c580c-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c580c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c580c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c580c-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c580c-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c580c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c580c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c580c-129">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c580c-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c580c-130">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c580c-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="c580c-131">**IContextNode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c580c-131">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="c580c-132">**IContextNode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="c580c-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="c580c-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c580c-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

