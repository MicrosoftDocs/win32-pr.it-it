---
description: Si verifica dopo che IInkAnalyzer crea un oggetto IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: 'Evento _IAnalysisProxyEvents:: ContextNodeCreated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103968993"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a><span data-ttu-id="270a7-103">\_Evento IAnalysisProxyEvents:: ContextNodeCreated</span><span class="sxs-lookup"><span data-stu-id="270a7-103">\_IAnalysisProxyEvents::ContextNodeCreated event</span></span>

<span data-ttu-id="270a7-104">Si verifica dopo che [**IInkAnalyzer**](iinkanalyzer.md) crea un oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="270a7-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="270a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="270a7-105">Syntax</span></span>


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="270a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="270a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="270a7-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="270a7-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270a7-108">[**IInkAnalyzer**](iinkanalyzer.md) che crea l'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="270a7-108">The [**IInkAnalyzer**](iinkanalyzer.md) creating the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="270a7-109">*pContextNodeCreated* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="270a7-109">*pContextNodeCreated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270a7-110">Nuovo oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="270a7-110">The new [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="270a7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="270a7-111">Return value</span></span>

<span data-ttu-id="270a7-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="270a7-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="270a7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="270a7-113">Remarks</span></span>

<span data-ttu-id="270a7-114">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="270a7-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="270a7-115">Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che crea un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="270a7-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that creates an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="270a7-116">Quando [**IInkAnalyzer**](iinkanalyzer.md) crea un [**IContextNode**](icontextnode.md), il nuovo **IContextNode** non contiene alcun tratto, non contiene collegamenti ad altri oggetti **IContextNode** e potrebbe non avere tutte le relative proprietà impostate.</span><span class="sxs-lookup"><span data-stu-id="270a7-116">When the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md), the new **IContextNode** does not contain any strokes, does not contain links to other **IContextNode** objects, and may not have all of its properties set.</span></span> <span data-ttu-id="270a7-117">Inoltre, il nuovo **IContextNode** viene aggiunto alla fine della raccolta di nodi del nodo padre (vedere [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="270a7-117">Also, the new **IContextNode** is added to the end of its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="270a7-118">Dopo questo evento, **IInkAnalyzer** può generare gli eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="270a7-118">After this event, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="270a7-119">Evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando sposta un tratto da un nodo di contesto a un altro.</span><span class="sxs-lookup"><span data-stu-id="270a7-119">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from one context node to another.</span></span>
-   <span data-ttu-id="270a7-120">Evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) quando aggiunge un [**IContextLink**](icontextlink.md) a un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="270a7-120">The [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) event when it adds an [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="270a7-121">Evento [**\_ IAnalysisProxyEvents:: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) quando modifica l'ordine di un [**IContextNode**](icontextnode.md) all'interno della relativa raccolta di nodi padre.</span><span class="sxs-lookup"><span data-stu-id="270a7-121">The [**\_IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) event when it changes the order of an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes.</span></span>
-   <span data-ttu-id="270a7-122">[**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) dopo che risolve lo stato di [**IContextNode**](icontextnode.md) per questa fase di analisi.</span><span class="sxs-lookup"><span data-stu-id="270a7-122">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) event after it resolves the state of the [**IContextNode**](icontextnode.md) for this analysis phase.</span></span>

<span data-ttu-id="270a7-123">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="270a7-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="270a7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="270a7-124">Requirements</span></span>



| <span data-ttu-id="270a7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="270a7-125">Requirement</span></span> | <span data-ttu-id="270a7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="270a7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="270a7-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="270a7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="270a7-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="270a7-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="270a7-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="270a7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="270a7-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="270a7-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="270a7-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="270a7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="270a7-132"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="270a7-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="270a7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="270a7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="270a7-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="270a7-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="270a7-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="270a7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="270a7-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="270a7-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="270a7-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="270a7-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="270a7-138">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="270a7-138">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="270a7-139">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="270a7-139">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="270a7-140">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="270a7-140">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="270a7-141">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="270a7-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




