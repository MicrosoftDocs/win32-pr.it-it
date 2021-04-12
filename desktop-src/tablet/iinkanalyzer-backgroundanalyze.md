---
description: Esegue l'analisi asincrona dell'input penna.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'Metodo IInkAnalyzer:: BackgroundAnalyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526503"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a><span data-ttu-id="4173a-103">Metodo IInkAnalyzer:: BackgroundAnalyze</span><span class="sxs-lookup"><span data-stu-id="4173a-103">IInkAnalyzer::BackgroundAnalyze method</span></span>

<span data-ttu-id="4173a-104">Esegue l'analisi asincrona dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="4173a-104">Performs asynchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="4173a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4173a-105">Syntax</span></span>


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a><span data-ttu-id="4173a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4173a-106">Parameters</span></span>

<span data-ttu-id="4173a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4173a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4173a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4173a-108">Return value</span></span>

<span data-ttu-id="4173a-109">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4173a-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4173a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4173a-110">Remarks</span></span>

<span data-ttu-id="4173a-111">Quando viene chiamato questo metodo, [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna su un thread in background.</span><span class="sxs-lookup"><span data-stu-id="4173a-111">When this method is called, the [**IInkAnalyzer**](iinkanalyzer.md) performs the ink analysis on a background thread.</span></span>

<span data-ttu-id="4173a-112">Questo metodo restituisce **\_ false** e non avvia una nuova operazione di analisi in background nelle circostanze seguenti.</span><span class="sxs-lookup"><span data-stu-id="4173a-112">This method returns **S\_FALSE** and does not start a new background analysis operation under the following circumstances.</span></span>

-   <span data-ttu-id="4173a-113">Il [**IInkAnalyzer**](iinkanalyzer.md) sta attualmente eseguendo l'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="4173a-113">The [**IInkAnalyzer**](iinkanalyzer.md) is currently performing background analysis.</span></span>
-   <span data-ttu-id="4173a-114">l'area dirty (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) rappresenta un'area vuota.</span><span class="sxs-lookup"><span data-stu-id="4173a-114">the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) represents an empty area.</span></span>

<span data-ttu-id="4173a-115">[**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno dell'area dirty durante una chiamata al metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o **IInkAnalyzer:: BackgroundAnalyze**.</span><span class="sxs-lookup"><span data-stu-id="4173a-115">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or **IInkAnalyzer::BackgroundAnalyze Method**.</span></span> <span data-ttu-id="4173a-116">Tuttavia, **IInkAnalyzer** può espandere l'operazione di analisi per includere le aree adiacenti.</span><span class="sxs-lookup"><span data-stu-id="4173a-116">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="4173a-117">Questo metodo imposta l'area dirty su un'area vuota.</span><span class="sxs-lookup"><span data-stu-id="4173a-117">This method sets the dirty region to an empty region.</span></span>

<span data-ttu-id="4173a-118">Se i dati del tratto sono stati aggiunti a [**IInkAnalyzer**](iinkanalyzer.md) dopo la chiamata al **Metodo IInkAnalyzer:: BackgroundAnalyze**, il **IInkAnalyzer** può aggiornare l'area dirty durante la fase di riconciliazione dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="4173a-118">If stroke data was added to the [**IInkAnalyzer**](iinkanalyzer.md) after the call to **IInkAnalyzer::BackgroundAnalyze Method**, the **IInkAnalyzer** may update the dirty region during the reconcile phase of ink analysis.</span></span>

<span data-ttu-id="4173a-119">L'impostazione modalità di analisi (vedere [**IInkAnalyzer:: GetAnalysisModes metodo**](iinkanalyzer-getanalysismodes.md)) specifica il modo in cui [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="4173a-119">The analysis modes setting (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs background analysis.</span></span> <span data-ttu-id="4173a-120">Per altre informazioni sull'analisi dell'input penna, vedere [Cenni preliminari sull'analisi degli input penna](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4173a-120">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

<span data-ttu-id="4173a-121">Questo metodo restituisce un codice di errore nelle circostanze seguenti.</span><span class="sxs-lookup"><span data-stu-id="4173a-121">This method returns an error code under the following circumstances.</span></span>

-   <span data-ttu-id="4173a-122">L'applicazione ha impostato il valore [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ IntermediateResults ()** in [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) e non gestisce l'evento [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) .</span><span class="sxs-lookup"><span data-stu-id="4173a-122">Your application has set [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_IntermediateResults** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) event.</span></span>
-   <span data-ttu-id="4173a-123">L'applicazione ha cancellato il valore [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ AutomaticReconciliation** in [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) e non gestisce l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="4173a-123">Your application has cleared [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_AutomaticReconciliation** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>
-   <span data-ttu-id="4173a-124">L'applicazione non gestisce l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="4173a-124">Your application does not handle the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>
-   <span data-ttu-id="4173a-125">L'applicazione non gestisce l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="4173a-125">Your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

## <a name="examples"></a><span data-ttu-id="4173a-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="4173a-126">Examples</span></span>

<span data-ttu-id="4173a-127">Nell'esempio seguente viene controllata l'area dirty dell'analizzatore di input penna e viene avviata l'analisi dell'input penna in background se l'area dirty non è vuota.</span><span class="sxs-lookup"><span data-stu-id="4173a-127">The following example checks the ink analyzer's dirty region, and then initiates background ink analysis if the dirty region is not empty.</span></span>


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



## <a name="requirements"></a><span data-ttu-id="4173a-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4173a-128">Requirements</span></span>



| <span data-ttu-id="4173a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4173a-129">Requirement</span></span> | <span data-ttu-id="4173a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4173a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4173a-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4173a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4173a-132">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4173a-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4173a-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4173a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4173a-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4173a-134">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4173a-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4173a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4173a-136"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4173a-136"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4173a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4173a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4173a-138"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4173a-138"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4173a-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4173a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4173a-140">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4173a-140">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4173a-141">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="4173a-141">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="4173a-142">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="4173a-142">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="4173a-143">**Metodo IInkAnalyzer:: GetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="4173a-143">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="4173a-144">**Metodo IInkAnalyzer:: SetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="4173a-144">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="4173a-145">**Metodo IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="4173a-145">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="4173a-146">**Metodo IInkAnalyzer:: SetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="4173a-146">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="4173a-147">**Metodo IInkAnalyzer:: GetRootNode**</span><span class="sxs-lookup"><span data-stu-id="4173a-147">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="4173a-148">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="4173a-148">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




