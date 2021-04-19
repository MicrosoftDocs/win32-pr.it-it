---
description: Esegue l'analisi dell'input sincrono.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Metodo IInkAnalyzer:: Analyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307395"
---
# <a name="iinkanalyzeranalyze-method"></a><span data-ttu-id="26748-103">Metodo IInkAnalyzer:: Analyze</span><span class="sxs-lookup"><span data-stu-id="26748-103">IInkAnalyzer::Analyze method</span></span>

<span data-ttu-id="26748-104">Esegue l'analisi dell'input sincrono.</span><span class="sxs-lookup"><span data-stu-id="26748-104">Performs synchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="26748-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26748-105">Syntax</span></span>


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a><span data-ttu-id="26748-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26748-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26748-107">*ppStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="26748-107">*ppStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26748-108">Puntatore a un [**IAnalysisStatus**](ianalysisstatus.md) che descrive lo stato dell'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="26748-108">A pointer to an [**IAnalysisStatus**](ianalysisstatus.md) that describes the status of the analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26748-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26748-109">Return value</span></span>

<span data-ttu-id="26748-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="26748-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26748-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="26748-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="26748-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppStatus* quando non è più necessario usare lo stato di analisi.</span><span class="sxs-lookup"><span data-stu-id="26748-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppStatus* when you no longer need to use the analysis status.</span></span>

 

<span data-ttu-id="26748-113">Questo metodo avvia un'operazione di analisi dell'input penna sincrona.</span><span class="sxs-lookup"><span data-stu-id="26748-113">This method starts a synchronous ink analysis operation.</span></span> <span data-ttu-id="26748-114">L'analisi dell'input penna include l'analisi del layout, la scrittura e la classificazione del disegno e il riconoscimento grafia.</span><span class="sxs-lookup"><span data-stu-id="26748-114">Ink analysis includes layout analysis, writing and drawing classification, and handwriting recognition.</span></span> <span data-ttu-id="26748-115">Questo metodo viene restituito al termine dell'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="26748-115">This method returns after the analysis operation is complete.</span></span>

<span data-ttu-id="26748-116">Questo metodo restituisce **un \_ puntatore E** se *ppStatus* è **null**.</span><span class="sxs-lookup"><span data-stu-id="26748-116">This method returns **E\_POINTER** if *ppStatus* is **NULL**.</span></span>

<span data-ttu-id="26748-117">Durante una chiamata al metodo **IInkAnalyzer:: Analyze** o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), [**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno dell'area dirty (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="26748-117">During a call to **IInkAnalyzer::Analyze Method** or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), the [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span> <span data-ttu-id="26748-118">Tuttavia, **IInkAnalyzer** può espandere l'operazione di analisi per includere le aree adiacenti.</span><span class="sxs-lookup"><span data-stu-id="26748-118">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="26748-119">Questo metodo imposta l'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) su un'area vuota.</span><span class="sxs-lookup"><span data-stu-id="26748-119">This method sets the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region to an empty region.</span></span> <span data-ttu-id="26748-120">Se un altro thread ha aggiunto dati del tratto che non sono stati analizzati, **IInkAnalyzer** aggiunge il rettangolo di delimitazione dei tratti non analizzati alla relativa area dirty durante la fase di riconciliazione dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="26748-120">If another thread has added stroke data that has not been analyzed, the **IInkAnalyzer** adds the bounding box of the unanalyzed strokes to its dirty region during the reconcile phase of the analysis.</span></span>

<span data-ttu-id="26748-121">Questo metodo restituisce un errore se l'applicazione non gestisce l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="26748-121">This method returns an error if your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

<span data-ttu-id="26748-122">[**IInkAnalyzer**](iinkanalyzer.md) non genera gli eventi [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) in risposta a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="26748-122">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) events in response to this method.</span></span>

<span data-ttu-id="26748-123">Per modificare la modalità di esecuzione dell'analisi dell'input penna, usare il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).</span><span class="sxs-lookup"><span data-stu-id="26748-123">To modify the way ink analysis is performed, use [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md).</span></span>

<span data-ttu-id="26748-124">Per altre informazioni sull'analisi dell'input penna, vedere [Cenni preliminari sull'analisi degli input penna](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="26748-124">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="26748-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="26748-125">Examples</span></span>

<span data-ttu-id="26748-126">Nell'esempio seguente viene eseguita l'analisi dell'input penna in primo piano.</span><span class="sxs-lookup"><span data-stu-id="26748-126">The following example performs foreground ink analysis.</span></span>


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="26748-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26748-127">Requirements</span></span>



| <span data-ttu-id="26748-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="26748-128">Requirement</span></span> | <span data-ttu-id="26748-129">Valore</span><span class="sxs-lookup"><span data-stu-id="26748-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26748-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26748-130">Minimum supported client</span></span><br/> | <span data-ttu-id="26748-131">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="26748-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26748-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26748-132">Minimum supported server</span></span><br/> | <span data-ttu-id="26748-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="26748-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="26748-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26748-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="26748-135"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="26748-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="26748-136">DLL</span><span class="sxs-lookup"><span data-stu-id="26748-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26748-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26748-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="26748-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26748-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26748-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="26748-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="26748-140">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="26748-140">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="26748-141">**Metodo IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="26748-141">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="26748-142">**Metodo IInkAnalyzer:: SetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="26748-142">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="26748-143">**Metodo IInkAnalyzer:: GetRootNode**</span><span class="sxs-lookup"><span data-stu-id="26748-143">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="26748-144">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="26748-144">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

