---
description: Carica i risultati dell'analisi salvata in IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'Metodo IInkAnalyzer:: LoadResults (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485076"
---
# <a name="iinkanalyzerloadresults-method"></a><span data-ttu-id="bf2bd-103">Metodo IInkAnalyzer:: LoadResults</span><span class="sxs-lookup"><span data-stu-id="bf2bd-103">IInkAnalyzer::LoadResults method</span></span>

<span data-ttu-id="bf2bd-104">Carica i risultati dell'analisi salvata in [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="bf2bd-104">Loads saved analysis results into the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf2bd-105">Syntax</span></span>


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="bf2bd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf2bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2bd-107">*ulDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf2bd-107">*ulDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2bd-108">Numero di byte in *pbSerializedResults*.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-108">The number of bytes in *pbSerializedResults*.</span></span>

</dd> <dt>

<span data-ttu-id="bf2bd-109">*pbSerializedResults* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf2bd-109">*pbSerializedResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2bd-110">Risultati dell'analisi serializzata.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-110">The serialized analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="bf2bd-111">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf2bd-111">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2bd-112">Numero degli identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-112">The number of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="bf2bd-113">*plOriginalStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf2bd-113">*plOriginalStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2bd-114">Matrice di identificatori di tratto originali.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-114">The array of original stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="bf2bd-115">*plNewStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf2bd-115">*plNewStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2bd-116">Matrice di nuovi identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-116">The array of new stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="bf2bd-117">*pfSuccessful* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bf2bd-117">*pfSuccessful* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2bd-118">**Variante \_ TRUE** se il caricamento è stato eseguito correttamente. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-118">**VARIANT\_TRUE** if loading was successful; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2bd-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf2bd-119">Return value</span></span>

<span data-ttu-id="bf2bd-120">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bf2bd-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf2bd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf2bd-121">Remarks</span></span>

<span data-ttu-id="bf2bd-122">Quando [**IInkAnalyzer**](iinkanalyzer.md) aggiunge un [**IContextNode**](icontextnode.md) dai risultati salvati, assegna un nuovo identificatore univoco globale (Guid) a **IContextNode** (vedere [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md) e [proprietà del nodo di contesto](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="bf2bd-122">When the [**IInkAnalyzer**](iinkanalyzer.md) adds a [**IContextNode**](icontextnode.md) from the saved results, it assigns a new globally unique identifier (GUID) to the **IContextNode** (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) and [Context Node Properties](context-node-properties.md)).</span></span>

<span data-ttu-id="bf2bd-123">Questo metodo aggiunge i risultati dell'analisi salvata all'albero [**IContextNode**](icontextnode.md) esistente.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-123">This method adds the saved analysis results to the existing [**IContextNode**](icontextnode.md) tree.</span></span> <span data-ttu-id="bf2bd-124">Per assicurarsi che i risultati combinati siano ordinati correttamente, aggiungere l'area contenente i nodi di contesto caricati all'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) e analizzare nuovamente l'input penna.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-124">To ensure that the combined results are ordered correctly, add the area containing the loaded context nodes to the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) and reanalyze the ink.</span></span>

<span data-ttu-id="bf2bd-125">I metodi del metodo [**IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md), [**IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)e [**IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) non salvano i dati del pacchetto insieme ai risultati dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-125">The [**IInkAnalyzer::SaveResults Method**](iinkanalyzer-saveresults.md), [**IInkAnalyzer::SaveResultsForNodes Method**](iinkanalyzer-saveresultsfornodes.md), and [**IInkAnalyzer::SaveResultsForStrokes Method**](iinkanalyzer-saveresultsforstrokes.md) methods do not save the packet data along with the analysis results.</span></span>

<span data-ttu-id="bf2bd-126">Ogni identificatore in *plOriginalStrokeIds* è l'identificatore del tratto per il tratto nei risultati dell'analisi salvata.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-126">Each identifier in *plOriginalStrokeIds* is the stroke identifier for the stroke in the saved analysis results.</span></span> <span data-ttu-id="bf2bd-127">Ogni identificatore in *plNewStrokeIds* è il nuovo identificatore con cui sostituire l'identificatore originale nei risultati dell'analisi caricata.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-127">Each identifier in *plNewStrokeIds* is the new identifier with which to replace the original identifier in the loaded analysis results.</span></span>

<span data-ttu-id="bf2bd-128">Se un hint di analisi salvato è in conflitto con un hint di analisi esistente, [**IInkAnalyzer**](iinkanalyzer.md) non carica l'hint salvato ma carica il resto dei risultati salvati.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-128">If a saved analysis hint conflicts with an existing analysis hint, the [**IInkAnalyzer**](iinkanalyzer.md) does not load the saved hint but does load the rest of the saved results.</span></span> <span data-ttu-id="bf2bd-129">Tuttavia, se **IInkAnalyzer** carica i risultati per un tratto che si trova all'interno dell'area di un hint di analisi salvato che non viene caricato dal **IInkAnalyzer** , **IInkAnalyzer** aggiunge il rettangolo di delimitazione del tratto all'area dirty dell'oggetto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="bf2bd-129">However, if the **IInkAnalyzer** loads results for a stroke that is within the area of a saved analysis hint that the **IInkAnalyzer** does not load, the **IInkAnalyzer** adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="bf2bd-130">Se, inoltre, **IInkAnalyzer** carica i risultati di un tratto che si trova all'interno di un'area dell'hint di analisi esistente, **IInkAnalyzer** aggiunge anche il rettangolo delimitatore del tratto all'area dirty dell'oggetto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="bf2bd-130">Also, if the **IInkAnalyzer** loads results for a stroke that is within an existing analysis hint's area, the **IInkAnalyzer** also adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="bf2bd-131">Per ulteriori informazioni sugli hint di analisi, vedere [proprietà hint di analisi](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bf2bd-131">For more information about analysis hints, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="bf2bd-132">Questo metodo può generare gli eventi [**\_ IAnalysisProxyEvents:: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)e [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) durante il caricamento dei risultati salvati.</span><span class="sxs-lookup"><span data-stu-id="bf2bd-132">This method may raise the [**\_IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), and [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) events as it loads the saved results.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2bd-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf2bd-133">Requirements</span></span>



| <span data-ttu-id="bf2bd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2bd-134">Requirement</span></span> | <span data-ttu-id="bf2bd-135">Valore</span><span class="sxs-lookup"><span data-stu-id="bf2bd-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2bd-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf2bd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2bd-137">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bf2bd-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bf2bd-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf2bd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2bd-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bf2bd-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bf2bd-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf2bd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf2bd-141"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bf2bd-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bf2bd-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bf2bd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf2bd-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf2bd-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bf2bd-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf2bd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2bd-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="bf2bd-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="bf2bd-146">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="bf2bd-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="bf2bd-147">**Metodo IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="bf2bd-147">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="bf2bd-148">**Metodo IInkAnalyzer:: SetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="bf2bd-148">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="bf2bd-149">**Metodo IInkAnalyzer:: SaveResults**</span><span class="sxs-lookup"><span data-stu-id="bf2bd-149">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="bf2bd-150">**Metodo IInkAnalyzer:: SaveResultsForNodes**</span><span class="sxs-lookup"><span data-stu-id="bf2bd-150">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="bf2bd-151">**Metodo IInkAnalyzer:: SaveResultsForStrokes**</span><span class="sxs-lookup"><span data-stu-id="bf2bd-151">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="bf2bd-152">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="bf2bd-152">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




