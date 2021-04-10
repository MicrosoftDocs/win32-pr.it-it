---
description: Salva i risultati dell'analisi per i tratti specificati associati a un IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'Metodo IInkAnalyzer:: SaveResultsForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343676"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a><span data-ttu-id="5cea4-103">Metodo IInkAnalyzer:: SaveResultsForStrokes</span><span class="sxs-lookup"><span data-stu-id="5cea4-103">IInkAnalyzer::SaveResultsForStrokes method</span></span>

<span data-ttu-id="5cea4-104">Salva i risultati dell'analisi per i tratti specificati associati a un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="5cea4-104">Saves analysis results for the specified strokes associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5cea4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cea4-105">Syntax</span></span>


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="5cea4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cea4-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cea4-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cea4-108">Il numero di identificatori di tratto in **plStrokeIds**.</span><span class="sxs-lookup"><span data-stu-id="5cea4-108">The number of stroke identifiers in **plStrokeIds**.</span></span>

</dd> <dt>

<span data-ttu-id="5cea4-109">*plStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cea4-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cea4-110">Matrice di identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="5cea4-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="5cea4-111">*pulSerializedDataSize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5cea4-111">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cea4-112">Numero di byte in *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="5cea4-112">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="5cea4-113">*ppbSerializedData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5cea4-113">*ppbSerializedData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5cea4-114">Puntatore ai dati di analisi serializzati.</span><span class="sxs-lookup"><span data-stu-id="5cea4-114">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cea4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cea4-115">Return value</span></span>

<span data-ttu-id="5cea4-116">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5cea4-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cea4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cea4-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="5cea4-118">Per evitare una perdita di memoria, chiamare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) su \* *ppbSerializedData* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="5cea4-118">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="5cea4-119">Questo metodo consente di salvare i risultati di analisi correnti per i tratti specificati.</span><span class="sxs-lookup"><span data-stu-id="5cea4-119">This method saves the current analysis results for the specified strokes.</span></span> <span data-ttu-id="5cea4-120">Questo metodo salva gli oggetti foglia input penna [**IContextNode**](icontextnode.md) contenenti i tratti e tutti i predecessori dei nodi di contesto.</span><span class="sxs-lookup"><span data-stu-id="5cea4-120">This method saves the ink leaf [**IContextNode**](icontextnode.md) objects containing the strokes and all of the ancestors of those context nodes.</span></span> <span data-ttu-id="5cea4-121">Questo metodo non salva alcun nodo dati Stroke o hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="5cea4-121">This method does not save any stroke data or analysis hint nodes.</span></span> <span data-ttu-id="5cea4-122">È responsabilità dell'applicazione sincronizzare i risultati dell'analisi e i dati di Stroke corrispondenti, se il problema è permanente.</span><span class="sxs-lookup"><span data-stu-id="5cea4-122">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="5cea4-123">Questo metodo restituisce un codice di errore quando un oggetto [**IContextNode**](icontextnode.md) da salvare è parzialmente popolato (vedere [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="5cea4-123">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cea4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cea4-124">Requirements</span></span>



| <span data-ttu-id="5cea4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cea4-125">Requirement</span></span> | <span data-ttu-id="5cea4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5cea4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cea4-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cea4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5cea4-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5cea4-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5cea4-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cea4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5cea4-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5cea4-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5cea4-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cea4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cea4-132"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5cea4-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5cea4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5cea4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cea4-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cea4-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5cea4-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cea4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cea4-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5cea4-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5cea4-137">**Metodo IInkAnalyzer:: LoadResults**</span><span class="sxs-lookup"><span data-stu-id="5cea4-137">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="5cea4-138">**Metodo IInkAnalyzer:: SaveResults**</span><span class="sxs-lookup"><span data-stu-id="5cea4-138">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="5cea4-139">**Metodo IInkAnalyzer:: SaveResultsForNodes**</span><span class="sxs-lookup"><span data-stu-id="5cea4-139">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="5cea4-140">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="5cea4-140">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5cea4-141">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="5cea4-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

