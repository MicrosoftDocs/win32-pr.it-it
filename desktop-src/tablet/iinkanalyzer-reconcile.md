---
description: "Applica i risultati di un'operazione di analisi dell'input penna in background all'albero del nodo di contesto per le parti dell'albero che non sono state modificate dall'applicazione dalla chiamata al metodo IInkAnalyzer:: BackgroundAnalyze."
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'Metodo IInkAnalyzer:: riconcilia (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307378"
---
# <a name="iinkanalyzerreconcile-method"></a><span data-ttu-id="b80b9-103">Metodo IInkAnalyzer:: riconcilia</span><span class="sxs-lookup"><span data-stu-id="b80b9-103">IInkAnalyzer::Reconcile method</span></span>

<span data-ttu-id="b80b9-104">Applica i risultati di un'operazione di analisi dell'input penna in background all'albero del nodo di contesto per le parti dell'albero che non sono state modificate dall'applicazione dalla chiamata al [**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="b80b9-104">Applies the results of a background ink analysis operation to the context node tree for the portions of the tree that have not been modified by the application since the call to [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b80b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b80b9-105">Syntax</span></span>


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a><span data-ttu-id="b80b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b80b9-106">Parameters</span></span>

<span data-ttu-id="b80b9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b80b9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b80b9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b80b9-108">Return value</span></span>

<span data-ttu-id="b80b9-109">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b80b9-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b80b9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b80b9-110">Remarks</span></span>

<span data-ttu-id="b80b9-111">Per impostazione predefinita, [**IInkAnalyzer**](iinkanalyzer.md) esegue una fase di riconciliazione automatica immediatamente prima di generare gli eventi [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) e [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="b80b9-111">By default, the [**IInkAnalyzer**](iinkanalyzer.md) performs an automatic reconciliation phase immediately before raising the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) and [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) events.</span></span>

<span data-ttu-id="b80b9-112">Per disabilitare la riconciliazione automatica, deselezionare il flag **AnalysisModes \_ AutomaticReconciliation** dalle modalità di analisi dell'analizzatore di input penna (vedere il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) e [**AnalysisModes**](analysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="b80b9-112">To disable automatic reconciliation, clear the **AnalysisModes\_AutomaticReconciliation** flag from the ink analyzer's analysis modes (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) and [**AnalysisModes**](analysismodes.md)).</span></span> <span data-ttu-id="b80b9-113">Il metodo [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) restituisce un errore quando la riconciliazione automatica è disabilitata e l'applicazione non gestisce l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="b80b9-113">The [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method returns an error when automatic reconciliation is disabled and your application does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="b80b9-114">L'applicazione deve chiamare il metodo **IInkAnalyzer:: riconcilia Method** prima che [**IInkAnalyzer**](iinkanalyzer.md) possa continuare a elaborare i risultati o continuare l'analisi per la fase di analisi corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b80b9-114">Your application must call the **IInkAnalyzer::Reconcile Method** method before the [**IInkAnalyzer**](iinkanalyzer.md) can continue to process the results or continue further analysis for the corresponding analysis stage.</span></span>

<span data-ttu-id="b80b9-115">L'applicazione può apportare modifiche, ad esempio l'aggiunta o la rimozione di tratti e la modifica dei dati del tratto, nell'albero del nodo di contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) durante l'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="b80b9-115">Your application can make changes, such as adding or removing strokes and changing stroke data, in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree during background analysis.</span></span> <span data-ttu-id="b80b9-116">Tali modifiche possono invalidare parti dei risultati dell'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="b80b9-116">Such changes can invalidate portions of the background analysis results.</span></span> <span data-ttu-id="b80b9-117">Questo metodo applica i risultati dell'analisi solo all'albero del nodo di contesto dell'analizzatore per le parti della struttura ad albero che l'applicazione non è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="b80b9-117">This method applies analysis results only to the analyzer's context node tree for the portions of the tree that your application has not changed.</span></span> <span data-ttu-id="b80b9-118">Questo metodo aggiunge anche aree contenenti risultati di analisi invalidati all'area dirty dell'oggetto **IInkAnalyzer** (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="b80b9-118">This method also adds regions containing invalidated analysis results to the **IInkAnalyzer** object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="b80b9-119">Per ulteriori informazioni sull'utilizzo di per analizzare l'input penna, vedere [Cenni preliminari sull'analisi dell'input penna](ink-analysis-overview.md). [**AnalysisModes**](analysismodes.md)</span><span class="sxs-lookup"><span data-stu-id="b80b9-119">For more information about using the to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).[**AnalysisModes**](analysismodes.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="b80b9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b80b9-120">Requirements</span></span>



| <span data-ttu-id="b80b9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b80b9-121">Requirement</span></span> | <span data-ttu-id="b80b9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b80b9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b80b9-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b80b9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b80b9-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b80b9-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b80b9-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b80b9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b80b9-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b80b9-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b80b9-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b80b9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b80b9-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b80b9-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b80b9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b80b9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b80b9-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b80b9-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b80b9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b80b9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b80b9-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b80b9-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b80b9-133">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="b80b9-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b80b9-134">**\_IAnalysisEvents:: ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="b80b9-134">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="b80b9-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b80b9-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




