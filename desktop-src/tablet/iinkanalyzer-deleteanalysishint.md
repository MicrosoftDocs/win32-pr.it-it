---
description: Rimuove un hint di analisi da IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: Metodo IInkAnalyzer::D eleteAnalysisHint (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129467"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a><span data-ttu-id="e5db9-103">IInkAnalyzer::D Metodo eleteAnalysisHint</span><span class="sxs-lookup"><span data-stu-id="e5db9-103">IInkAnalyzer::DeleteAnalysisHint method</span></span>

<span data-ttu-id="e5db9-104">Rimuove un hint di analisi da [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e5db9-104">Removes an analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5db9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5db9-105">Syntax</span></span>


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="e5db9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5db9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5db9-107">*pHintToDelete* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5db9-107">*pHintToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5db9-108">Hint di analisi di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e5db9-108">The analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5db9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5db9-109">Return value</span></span>

<span data-ttu-id="e5db9-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e5db9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5db9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5db9-111">Remarks</span></span>

<span data-ttu-id="e5db9-112">La rimozione di un hint di analisi non contrassegna l'area dell'hint per la rianalisi.</span><span class="sxs-lookup"><span data-stu-id="e5db9-112">Removing an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="e5db9-113">Per contrassegnare l'area all'interno dell'hint per la rianalisi, utilizzare il [**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) per impostare l'area dirty sull'Unione dell'area e dell'area dirty correnti dell'hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="e5db9-113">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="e5db9-114">L'hint viene rimosso dall'analizzatore; Tuttavia, il [**IContextNode**](icontextnode.md) stesso non viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="e5db9-114">The hint is removed from the analyzer; however, the [**IContextNode**](icontextnode.md) itself is not deleted.</span></span>

<span data-ttu-id="e5db9-115">Questo metodo restituisce un codice di errore quando *pHintToDelete* è un [**IContextNode**](icontextnode.md) che non è di tipo AnalysisHint (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="e5db9-115">This method returns an error code when *pHintToDelete* is a [**IContextNode**](icontextnode.md) that is not of type AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5db9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5db9-116">Requirements</span></span>



| <span data-ttu-id="e5db9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5db9-117">Requirement</span></span> | <span data-ttu-id="e5db9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e5db9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5db9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5db9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e5db9-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e5db9-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e5db9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5db9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e5db9-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e5db9-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e5db9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5db9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5db9-124"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e5db9-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e5db9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e5db9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5db9-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5db9-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e5db9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5db9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5db9-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e5db9-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e5db9-129">**Metodo IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="e5db9-129">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="e5db9-130">**Metodo IInkAnalyzer:: GetAnalysisHints**</span><span class="sxs-lookup"><span data-stu-id="e5db9-130">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="e5db9-131">**Metodo IInkAnalyzer:: GetAnalysisHintsByName**</span><span class="sxs-lookup"><span data-stu-id="e5db9-131">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="e5db9-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="e5db9-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




