---
description: Recupera una matrice di identificatori per i tratti all'interno dell'oggetto IContextNode.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'Metodo IContextNode:: GetStrokeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129499"
---
# <a name="icontextnodegetstrokeids-method"></a><span data-ttu-id="340b1-103">Metodo IContextNode:: GetStrokeIds</span><span class="sxs-lookup"><span data-stu-id="340b1-103">IContextNode::GetStrokeIds method</span></span>

<span data-ttu-id="340b1-104">Recupera una matrice di identificatori per i tratti all'interno dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="340b1-104">Retrieves an array of identifiers for the strokes within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="340b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="340b1-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="340b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="340b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="340b1-107">*pulStrokeIdsCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="340b1-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="340b1-108">Numero di tratti.</span><span class="sxs-lookup"><span data-stu-id="340b1-108">The number of strokes.</span></span> <span data-ttu-id="340b1-109">Il valore passato non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="340b1-109">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="340b1-110">*pplStrokes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="340b1-110">*pplStrokes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="340b1-111">Puntatore alla matrice di identificatori di tratto per questo oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="340b1-111">A pointer to the array of stroke identifiers for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="340b1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="340b1-112">Return value</span></span>

<span data-ttu-id="340b1-113">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="340b1-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="340b1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="340b1-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="340b1-115">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pplStrokes* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="340b1-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokes* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="340b1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="340b1-116">Requirements</span></span>



| <span data-ttu-id="340b1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="340b1-117">Requirement</span></span> | <span data-ttu-id="340b1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="340b1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="340b1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="340b1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="340b1-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="340b1-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="340b1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="340b1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="340b1-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="340b1-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="340b1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="340b1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="340b1-124"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="340b1-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="340b1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="340b1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="340b1-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="340b1-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="340b1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="340b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="340b1-128">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="340b1-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="340b1-129">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="340b1-129">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="340b1-130">**IContextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="340b1-130">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="340b1-131">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="340b1-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

