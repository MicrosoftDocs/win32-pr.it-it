---
description: Restituisce gli identificatori di qualsiasi nodo di contesto pertinente associato a questo avviso.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'Metodo IAnalysisWarning:: GetNodeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526539"
---
# <a name="ianalysiswarninggetnodeids-method"></a><span data-ttu-id="fe60c-103">Metodo IAnalysisWarning:: GetNodeIds</span><span class="sxs-lookup"><span data-stu-id="fe60c-103">IAnalysisWarning::GetNodeIds method</span></span>

<span data-ttu-id="fe60c-104">Restituisce gli identificatori di qualsiasi nodo di contesto pertinente associato a questo avviso.</span><span class="sxs-lookup"><span data-stu-id="fe60c-104">Returns the identifiers of any relevant context nodes that are associated with this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe60c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe60c-105">Syntax</span></span>


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a><span data-ttu-id="fe60c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe60c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe60c-107">*pulCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fe60c-107">*pulCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe60c-108">Il numero di identificatori univoci globali (GUID) in *ppNodeIds*.</span><span class="sxs-lookup"><span data-stu-id="fe60c-108">The number of globally unique identifiers (GUIDs) in *ppNodeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="fe60c-109">*ppNodeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe60c-109">*ppNodeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe60c-110">Puntatore a una matrice di GUID che identifica i nodi di contesto associati a questo avviso di analisi oppure **null** se all'avviso non è associato alcun nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="fe60c-110">A pointer to an array of GUIDs that identifies the context nodes that are associated with this analysis warning, or **NULL** if no context nodes are associated with the warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe60c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe60c-111">Return value</span></span>

<span data-ttu-id="fe60c-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fe60c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe60c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe60c-113">Remarks</span></span>

<span data-ttu-id="fe60c-114">Se *ppNodeIds* viene passato come **null**, il metodo **GetNodeIds** restituisce **S \_ OK** e viene restituito il numero di rettangoli in *pulCount*.</span><span class="sxs-lookup"><span data-stu-id="fe60c-114">If *ppNodeIds* is passed as **NULL**, the **GetNodeIds** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="fe60c-115">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppNodeIds* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="fe60c-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppNodeIds* when you no longer need the information.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fe60c-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="fe60c-116">Examples</span></span>

<span data-ttu-id="fe60c-117">Nell'esempio seguente viene illustrato come ottenere gli oggetti [**IContextNode**](icontextnode.md) presenti in [**IAnalysisWarning**](ianalysiswarning.md), `warning` e come ottenere solo il numero di oggetti **IContextNode**</span><span class="sxs-lookup"><span data-stu-id="fe60c-117">The following example shows how to get the [**IContextNode**](icontextnode.md) objects that are in the [**IAnalysisWarning**](ianalysiswarning.md), `warning`, and how to get only the number of **IContextNode** objects</span></span>


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="fe60c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe60c-118">Requirements</span></span>



| <span data-ttu-id="fe60c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe60c-119">Requirement</span></span> | <span data-ttu-id="fe60c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fe60c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe60c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe60c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fe60c-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fe60c-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fe60c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe60c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fe60c-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fe60c-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fe60c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe60c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe60c-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fe60c-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fe60c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fe60c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe60c-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe60c-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fe60c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe60c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe60c-130">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="fe60c-130">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="fe60c-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="fe60c-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fe60c-132">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="fe60c-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="fe60c-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="fe60c-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

