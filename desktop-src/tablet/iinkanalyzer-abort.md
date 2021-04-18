---
description: Annulla l'operazione di analisi corrente.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'Metodo IInkAnalyzer:: Abort (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307403"
---
# <a name="iinkanalyzerabort-method"></a><span data-ttu-id="90ffe-103">Metodo IInkAnalyzer:: Abort</span><span class="sxs-lookup"><span data-stu-id="90ffe-103">IInkAnalyzer::Abort method</span></span>

<span data-ttu-id="90ffe-104">Annulla l'operazione di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="90ffe-104">Cancels the current analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ffe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90ffe-105">Syntax</span></span>


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="90ffe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="90ffe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ffe-107">*ppAbortedRegion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90ffe-107">*ppAbortedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90ffe-108">Puntatore a un [**IAnalysisRegion**](ianalysisregion.md) che rappresenta l'area dirty (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) dell'operazione di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="90ffe-108">A pointer to an [**IAnalysisRegion**](ianalysisregion.md) that represents the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) of the current analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ffe-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90ffe-109">Return value</span></span>

<span data-ttu-id="90ffe-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="90ffe-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90ffe-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="90ffe-111">Remarks</span></span>

<span data-ttu-id="90ffe-112">Chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAbortedRegion* quando non è più necessario usare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="90ffe-112">Call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAbortedRegion* when you no longer need to use the object.</span></span>

<span data-ttu-id="90ffe-113">Questo metodo annulla l'operazione di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="90ffe-113">This method cancels the current analysis operation.</span></span>

<span data-ttu-id="90ffe-114">Quando *ppAbortedRegion* è **null**, questo metodo esegue l'interruzione come normale, perché questo indica che il chiamante non ha alcun interesse nel valore restituito.</span><span class="sxs-lookup"><span data-stu-id="90ffe-114">When *ppAbortedRegion* is **NULL**, this method performs the abort as normal, because this indicates that the caller has no interest in the return value.</span></span>

<span data-ttu-id="90ffe-115">Il **Metodo IInkAnalyzer:: Abort** silenzia gli eventi [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents:: Activity**](-ianalysisevents-activity.md) per l'operazione di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="90ffe-115">**IInkAnalyzer::Abort Method** silences the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::Activity**](-ianalysisevents-activity.md) events for the current analysis operation.</span></span>

<span data-ttu-id="90ffe-116">Il **Metodo IInkAnalyzer:: Abort** viene eseguito in modo asincrono finché non viene annullata l'operazione di analisi in background corrente.</span><span class="sxs-lookup"><span data-stu-id="90ffe-116">**IInkAnalyzer::Abort Method** runs asynchronously until the current background analysis operation is canceled.</span></span> <span data-ttu-id="90ffe-117">Poiché il processo di annullamento è asincrono, l'applicazione può eseguire altre attività mentre il opertions di analisi corrente viene annullato.</span><span class="sxs-lookup"><span data-stu-id="90ffe-117">Because the cancellation process is asynchronous, the application can perform other tasks while the current analysis opertions is canceled.</span></span>

<span data-ttu-id="90ffe-118">Se non sono in corso operazioni di analisi, questo metodo restituisce un'area di analisi vuota.</span><span class="sxs-lookup"><span data-stu-id="90ffe-118">If no analysis operations are in progress, this method returns an empty analysis region.</span></span>

<span data-ttu-id="90ffe-119">Se è in corso un'operazione di analisi, questo metodo annulla l'operazione.</span><span class="sxs-lookup"><span data-stu-id="90ffe-119">If one analysis operation is in progress, this method cancels the operation.</span></span>

<span data-ttu-id="90ffe-120">Se sono in corso operazioni di analisi sincrone e asincrone, questo metodo annulla l'operazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="90ffe-120">If both synchronous and asynchronous analysis operations are in progress, this method cancels the synchronous operation.</span></span>

<span data-ttu-id="90ffe-121">Se questo metodo viene chiamato più di una volta per la stessa operazione di analisi, la prima chiamata restituisce l'area dirty per l'operazione e le chiamate successive restituiscono un'area vuota.</span><span class="sxs-lookup"><span data-stu-id="90ffe-121">If this method is called more than once for the same analysis operation, the first call returns the dirty region for the operation, and the subsequent calls return an empty region.</span></span>

<span data-ttu-id="90ffe-122">Se l'applicazione mantiene una struttura di dati personalizzata sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md), la chiamata al **Metodo IInkAnalyzer:: Abort** può lasciare il documento con risultati parziali.</span><span class="sxs-lookup"><span data-stu-id="90ffe-122">If your application maintains its own data structure that is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), calling **IInkAnalyzer::Abort Method** can leave your document with partial results.</span></span> <span data-ttu-id="90ffe-123">Per evitare questo problema, non chiamare il **Metodo IInkAnalyzer:: Abort** tra il momento in cui **IInkAnalyzer** riceve l'evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) e l'ora in cui **IInkAnalyzer** riceve l'evento [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="90ffe-123">To avoid this, do not call **IInkAnalyzer::Abort Method** between the time the **IInkAnalyzer** receives the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event and the time the **IInkAnalyzer** receives the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="90ffe-124">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con Ink Analyzer, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="90ffe-124">For more information about synchronizing your application data with the ink analyzer, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90ffe-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90ffe-125">Requirements</span></span>



| <span data-ttu-id="90ffe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ffe-126">Requirement</span></span> | <span data-ttu-id="90ffe-127">Valore</span><span class="sxs-lookup"><span data-stu-id="90ffe-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ffe-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90ffe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="90ffe-129">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="90ffe-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="90ffe-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90ffe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="90ffe-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="90ffe-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="90ffe-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90ffe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ffe-133"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="90ffe-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="90ffe-134">DLL</span><span class="sxs-lookup"><span data-stu-id="90ffe-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90ffe-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90ffe-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="90ffe-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90ffe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ffe-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="90ffe-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="90ffe-138">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="90ffe-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="90ffe-139">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="90ffe-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="90ffe-140">**Metodo IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="90ffe-140">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="90ffe-141">**Metodo IInkAnalyzer:: SetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="90ffe-141">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="90ffe-142">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="90ffe-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

