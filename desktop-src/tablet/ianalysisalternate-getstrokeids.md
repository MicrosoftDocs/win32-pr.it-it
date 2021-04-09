---
description: Restituisce gli identificatori di tratto associati a questo IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'Metodo IAnalysisAlternate:: GetStrokeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879374"
---
# <a name="ianalysisalternategetstrokeids-method"></a><span data-ttu-id="b84ae-103">Metodo IAnalysisAlternate:: GetStrokeIds</span><span class="sxs-lookup"><span data-stu-id="b84ae-103">IAnalysisAlternate::GetStrokeIds method</span></span>

<span data-ttu-id="b84ae-104">Restituisce gli identificatori di tratto associati a questo [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="b84ae-104">Returns the stroke identifiers that are associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b84ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b84ae-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="b84ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b84ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b84ae-107">*pulStrokeIdsCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b84ae-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b84ae-108">Puntatore a un **ULONG** impostato sul numero di identificatori di tratto associati a questo [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="b84ae-108">A pointer to a **ULONG** that is set to the number of stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> <dt>

<span data-ttu-id="b84ae-109">*pplStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b84ae-109">*pplStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b84ae-110">\[out, Size \_ is ( \* *PULSTROKEIDSCOUNT* \* sizeof (Long))\]</span><span class="sxs-lookup"><span data-stu-id="b84ae-110">\[out, size\_is(\**pulStrokeIdsCount* \* sizeof(LONG))\]</span></span>

<span data-ttu-id="b84ae-111">Matrice di **Long** di lunghezza *pulStrokeIdsCount* impostata sugli identificatori del tratto associati a questo [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="b84ae-111">An array of **LONG** of length *pulStrokeIdsCount* that is set to the stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b84ae-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b84ae-112">Return value</span></span>

<span data-ttu-id="b84ae-113">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b84ae-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b84ae-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b84ae-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b84ae-115">Per evitare una perdita di memoria, usare [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pplStrokeIds* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="b84ae-115">To avoid a memory leak, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokeIds* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b84ae-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b84ae-116">Requirements</span></span>



| <span data-ttu-id="b84ae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b84ae-117">Requirement</span></span> | <span data-ttu-id="b84ae-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b84ae-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b84ae-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b84ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b84ae-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b84ae-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b84ae-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b84ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b84ae-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b84ae-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b84ae-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b84ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b84ae-124"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b84ae-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b84ae-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b84ae-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b84ae-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b84ae-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b84ae-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b84ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84ae-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="b84ae-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="b84ae-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b84ae-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

