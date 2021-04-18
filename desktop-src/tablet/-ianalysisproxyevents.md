---
description: Specifica gli eventi associati ai passaggi del proxy di dati di un oggetto IInkAnalyzer.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: Interfaccia _IAnalysisProxyEvents (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320946"
---
# <a name="_ianalysisproxyevents-interface"></a><span data-ttu-id="ec407-103">\_Interfaccia IAnalysisProxyEvents</span><span class="sxs-lookup"><span data-stu-id="ec407-103">\_IAnalysisProxyEvents interface</span></span>

<span data-ttu-id="ec407-104">Specifica gli eventi associati ai passaggi del proxy di dati di un oggetto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="ec407-104">Specifies events associated with the data proxy steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="ec407-105">Eventi</span><span class="sxs-lookup"><span data-stu-id="ec407-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="ec407-106">Eventi</span><span class="sxs-lookup"><span data-stu-id="ec407-106">Events</span></span>

<span data-ttu-id="ec407-107">L'interfaccia **\_ IAnalysisProxyEvents** presenta questi eventi.</span><span class="sxs-lookup"><span data-stu-id="ec407-107">The **\_IAnalysisProxyEvents** interface has these events.</span></span>



| <span data-ttu-id="ec407-108">Event</span><span class="sxs-lookup"><span data-stu-id="ec407-108">Event</span></span>                                                                                      | <span data-ttu-id="ec407-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec407-109">Description</span></span>                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec407-110">**ContextNodeCreated**</span><span class="sxs-lookup"><span data-stu-id="ec407-110">**ContextNodeCreated**</span></span>](-ianalysisproxyevents-contextnodecreated.md)                     | <span data-ttu-id="ec407-111">Si verifica dopo che [**IInkAnalyzer**](iinkanalyzer.md) crea un oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ec407-111">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                  |
| [<span data-ttu-id="ec407-112">**L'ContextNodeDeleting**</span><span class="sxs-lookup"><span data-stu-id="ec407-112">**ContextNodeDeleting**</span></span>](-ianalysisproxyevents-contextnodedeleting.md)                   | <span data-ttu-id="ec407-113">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ec407-113">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                 |
| [<span data-ttu-id="ec407-114">**ContextNodeLinkAdding**</span><span class="sxs-lookup"><span data-stu-id="ec407-114">**ContextNodeLinkAdding**</span></span>](-ianalysisproxyevents-contextnodelinkadding.md)               | <span data-ttu-id="ec407-115">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) aggiunga un oggetto [**IContextLink**](icontextlink.md) tra due oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ec407-115">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>           |
| [<span data-ttu-id="ec407-116">**L'ContextNodeLinkDeleting**</span><span class="sxs-lookup"><span data-stu-id="ec407-116">**ContextNodeLinkDeleting**</span></span>](-ianalysisproxyevents-contextnodelinkdeleting.md)           | <span data-ttu-id="ec407-117">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un oggetto [**IContextLink**](icontextlink.md) tra due oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ec407-117">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>         |
| [<span data-ttu-id="ec407-118">**ContextNodeMovingToPosition**</span><span class="sxs-lookup"><span data-stu-id="ec407-118">**ContextNodeMovingToPosition**</span></span>](-ianalysisproxyevents-contextnodemovingtoposition.md)   | <span data-ttu-id="ec407-119">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) sposti un oggetto [**IContextNode**](icontextnode.md) in una nuova posizione all'interno della relativa raccolta di nodi padre.</span><span class="sxs-lookup"><span data-stu-id="ec407-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span><br/> |
| [<span data-ttu-id="ec407-120">**ContextNodePropertiesUpdated**</span><span class="sxs-lookup"><span data-stu-id="ec407-120">**ContextNodePropertiesUpdated**</span></span>](-ianalysisproxyevents-contextnodepropertiesupdated.md) | <span data-ttu-id="ec407-121">Si verifica dopo che [**IInkAnalyzer**](iinkanalyzer.md) aggiorna una o più proprietà di un oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ec407-121">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                        |
| [<span data-ttu-id="ec407-122">**L'ContextNodeReparenting**</span><span class="sxs-lookup"><span data-stu-id="ec407-122">**ContextNodeReparenting**</span></span>](-ianalysisproxyevents-contextnodereparenting.md)             | <span data-ttu-id="ec407-123">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) sposti un oggetto [**IContextNode**](icontextnode.md) modificando il relativo nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ec407-123">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span><br/>                                       |
| [<span data-ttu-id="ec407-124">**InkAnalyzerStateChanging**</span><span class="sxs-lookup"><span data-stu-id="ec407-124">**InkAnalyzerStateChanging**</span></span>](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | <span data-ttu-id="ec407-125">Si verifica prima che i [**IInkAnalyzer**](iinkanalyzer.md) riconciliano i risultati dell'analisi in modo che un'applicazione possa sincronizzare i dati con **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="ec407-125">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span><br/>                      |
| [<span data-ttu-id="ec407-126">**PopulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="ec407-126">**PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)                   | <span data-ttu-id="ec407-127">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) esegua l'analisi all'interno dell'area di un oggetto [**IContextNode**](icontextnode.md) parzialmente popolato.</span><span class="sxs-lookup"><span data-stu-id="ec407-127">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span><br/>               |
| [<span data-ttu-id="ec407-128">**StrokeReparented**</span><span class="sxs-lookup"><span data-stu-id="ec407-128">**StrokeReparented**</span></span>](-ianalysisproxyevents-strokereparented.md)                         | <span data-ttu-id="ec407-129">Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) sposta un tratto da un oggetto [**IContextNode**](icontextnode.md) a un altro.</span><span class="sxs-lookup"><span data-stu-id="ec407-129">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span><br/>                                           |



 

## <a name="remarks"></a><span data-ttu-id="ec407-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec407-130">Remarks</span></span>

<span data-ttu-id="ec407-131">Usare questi eventi quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ec407-131">Use these events when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ec407-132">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con **IInkAnalyzer**, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ec407-132">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec407-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec407-133">Requirements</span></span>



| <span data-ttu-id="ec407-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec407-134">Requirement</span></span> | <span data-ttu-id="ec407-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ec407-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec407-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec407-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ec407-137">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ec407-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec407-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec407-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ec407-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ec407-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ec407-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec407-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec407-141"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec407-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec407-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ec407-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec407-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec407-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ec407-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec407-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec407-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ec407-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ec407-146">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ec407-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ec407-147">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="ec407-147">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ec407-148">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="ec407-148">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ec407-149">\_IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="ec407-149">\_IAnalysisEvents</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="ec407-150">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ec407-150">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

