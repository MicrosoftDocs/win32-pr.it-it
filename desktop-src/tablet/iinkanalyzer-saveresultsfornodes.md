---
description: Salva i risultati dell'analisi per una raccolta di nodi di contesto specifica associata a un IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'Metodo IInkAnalyzer:: SaveResultsForNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129443"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a><span data-ttu-id="27d48-103">Metodo IInkAnalyzer:: SaveResultsForNodes</span><span class="sxs-lookup"><span data-stu-id="27d48-103">IInkAnalyzer::SaveResultsForNodes method</span></span>

<span data-ttu-id="27d48-104">Salva i risultati dell'analisi per una raccolta di nodi di contesto specifica associata a un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="27d48-104">Saves analysis results for a specific context node collection associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="27d48-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27d48-105">Syntax</span></span>


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="27d48-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27d48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27d48-107">*pContextNodes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27d48-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d48-108">Raccolta [**IContextNode**](icontextnode.md) per cui salvare i risultati dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="27d48-108">The [**IContextNode**](icontextnode.md) collection for which to save analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="27d48-109">*pulSerializedDataSize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="27d48-109">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="27d48-110">Numero di byte in *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="27d48-110">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="27d48-111">*ppbSerializedData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27d48-111">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27d48-112">Puntatore ai dati di analisi serializzati.</span><span class="sxs-lookup"><span data-stu-id="27d48-112">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27d48-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27d48-113">Return value</span></span>

<span data-ttu-id="27d48-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="27d48-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="27d48-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="27d48-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="27d48-116">Per evitare una perdita di memoria, chiamare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) su \* *ppbSerializedData* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="27d48-116">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="27d48-117">Questo metodo consente di salvare i risultati di analisi correnti per gli oggetti [**IContextNode**](icontextnode.md) in *pContextNodes* e tutti i relativi nodi di contesto predecessore e discendente.</span><span class="sxs-lookup"><span data-stu-id="27d48-117">This method saves the current analysis results for the [**IContextNode**](icontextnode.md) objects in *pContextNodes* and all of their ancestor and descendant context nodes.</span></span> <span data-ttu-id="27d48-118">Questo metodo non salva i dati del tratto.</span><span class="sxs-lookup"><span data-stu-id="27d48-118">This method does not save any stroke data.</span></span> <span data-ttu-id="27d48-119">È responsabilità dell'applicazione sincronizzare i risultati dell'analisi e i dati di Stroke corrispondenti, se il problema è permanente.</span><span class="sxs-lookup"><span data-stu-id="27d48-119">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="27d48-120">Se l'oggetto [**IContextNode**](icontextnode.md) da salvare è solo parzialmente popolato, questo metodo restituisce un codice di errore (vedere [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="27d48-120">If the [**IContextNode**](icontextnode.md) object to be saved is only partially populated, this method returns an error code (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="27d48-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27d48-121">Requirements</span></span>



| <span data-ttu-id="27d48-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d48-122">Requirement</span></span> | <span data-ttu-id="27d48-123">Valore</span><span class="sxs-lookup"><span data-stu-id="27d48-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d48-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27d48-124">Minimum supported client</span></span><br/> | <span data-ttu-id="27d48-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="27d48-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="27d48-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27d48-126">Minimum supported server</span></span><br/> | <span data-ttu-id="27d48-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="27d48-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="27d48-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27d48-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="27d48-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="27d48-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="27d48-130">DLL</span><span class="sxs-lookup"><span data-stu-id="27d48-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27d48-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27d48-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="27d48-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27d48-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d48-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="27d48-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="27d48-134">**Metodo IInkAnalyzer:: LoadResults**</span><span class="sxs-lookup"><span data-stu-id="27d48-134">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="27d48-135">**Metodo IInkAnalyzer:: SaveResults**</span><span class="sxs-lookup"><span data-stu-id="27d48-135">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="27d48-136">**Metodo IInkAnalyzer:: SaveResultsForStrokes**</span><span class="sxs-lookup"><span data-stu-id="27d48-136">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="27d48-137">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="27d48-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="27d48-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="27d48-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

