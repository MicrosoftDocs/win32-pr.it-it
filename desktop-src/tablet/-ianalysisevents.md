---
description: Specifica gli eventi associati ai passaggi di analisi di un oggetto IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Interfaccia _IAnalysisEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314929"
---
# <a name="_ianalysisevents-interface"></a><span data-ttu-id="a1bb6-103">\_Interfaccia IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="a1bb6-103">\_IAnalysisEvents interface</span></span>

<span data-ttu-id="a1bb6-104">Specifica gli eventi associati ai passaggi di analisi di un oggetto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="a1bb6-104">Specifies events associated with the analysis steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="a1bb6-105">Eventi</span><span class="sxs-lookup"><span data-stu-id="a1bb6-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="a1bb6-106">Eventi</span><span class="sxs-lookup"><span data-stu-id="a1bb6-106">Events</span></span>

<span data-ttu-id="a1bb6-107">L'interfaccia **\_ IAnalysisEvents** presenta questi eventi.</span><span class="sxs-lookup"><span data-stu-id="a1bb6-107">The **\_IAnalysisEvents** interface has these events.</span></span>



| <span data-ttu-id="a1bb6-108">Event</span><span class="sxs-lookup"><span data-stu-id="a1bb6-108">Event</span></span>                                                               | <span data-ttu-id="a1bb6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1bb6-109">Description</span></span>                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1bb6-110">**Attività**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-110">**Activity**</span></span>](-ianalysisevents-activity.md)                       | <span data-ttu-id="a1bb6-111">Si verifica durante le chiamate al metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o al metodo [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .</span><span class="sxs-lookup"><span data-stu-id="a1bb6-111">Occurs during calls to the [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method.</span></span><br/> |
| [<span data-ttu-id="a1bb6-112">**IntermediateResults ()**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-112">**IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md) | <span data-ttu-id="a1bb6-113">Si verifica al termine della fase di analisi intermedia corrente.</span><span class="sxs-lookup"><span data-stu-id="a1bb6-113">Occurs when the current intermediate analysis stage is finished.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="a1bb6-114">**ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-114">**ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)       | <span data-ttu-id="a1bb6-115">Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) è pronto per risolvere i risultati dell'analisi in background con lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="a1bb6-115">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span><br/>                                                  |
| [<span data-ttu-id="a1bb6-116">**Risultati**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-116">**Results**</span></span>](-ianalysisevents-results.md)                         | <span data-ttu-id="a1bb6-117">Si verifica al termine della fase di analisi finale.</span><span class="sxs-lookup"><span data-stu-id="a1bb6-117">Occurs when the final analysis stage is finished.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="a1bb6-118">**UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-118">**UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)   | <span data-ttu-id="a1bb6-119">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) acceda ai dati del tratto.</span><span class="sxs-lookup"><span data-stu-id="a1bb6-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span><br/>                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="a1bb6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1bb6-120">Requirements</span></span>



| <span data-ttu-id="a1bb6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1bb6-121">Requirement</span></span> | <span data-ttu-id="a1bb6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a1bb6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a1bb6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1bb6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a1bb6-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a1bb6-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a1bb6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1bb6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a1bb6-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a1bb6-126">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="a1bb6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1bb6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1bb6-128">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-128">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="a1bb6-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a1bb6-130">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a1bb6-131">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="a1bb6-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a1bb6-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="a1bb6-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

