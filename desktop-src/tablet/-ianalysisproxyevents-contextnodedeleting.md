---
description: Si verifica prima che IInkAnalyzer elimini un oggetto IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: "Evento _IAnalysisProxyEvents:: l'ContextNodeDeleting (IACom. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320913"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a><span data-ttu-id="be150-103">\_Evento IAnalysisProxyEvents:: l'ContextNodeDeleting</span><span class="sxs-lookup"><span data-stu-id="be150-103">\_IAnalysisProxyEvents::ContextNodeDeleting event</span></span>

<span data-ttu-id="be150-104">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="be150-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="be150-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be150-105">Syntax</span></span>


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="be150-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be150-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be150-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be150-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be150-108">Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che elimina l'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="be150-108">The [**IInkAnalyzer**](iinkanalyzer.md) object deleting the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="be150-109">*pContextNodeToBeDeleted* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be150-109">*pContextNodeToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be150-110">Oggetto [**IContextNode**](icontextnode.md) da eliminare.</span><span class="sxs-lookup"><span data-stu-id="be150-110">The [**IContextNode**](icontextnode.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be150-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be150-111">Return value</span></span>

<span data-ttu-id="be150-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="be150-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be150-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="be150-113">Remarks</span></span>

<span data-ttu-id="be150-114">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="be150-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="be150-115">Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che elimina un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="be150-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that deletes an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="be150-116">Prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un [**IContextNode**](icontextnode.md), **IInkAnalyzer** rimuove tutti i tratti dal nodo di contesto e rimuove tutti i collegamenti ad altri nodi di contesto.</span><span class="sxs-lookup"><span data-stu-id="be150-116">Before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md), the **IInkAnalyzer** removes all of the strokes from the context node and removes all of the links to other context nodes.</span></span> <span data-ttu-id="be150-117">Prima di rimuovere il nodo di contesto, **IInkAnalyzer** può generare gli eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="be150-117">Before the context node is removed, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="be150-118">Evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando sposta un tratto da [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="be150-118">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="be150-119">Evento [**\_ IAnalysisProxyEvents:: l'ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) prima di rimuovere un [**IContextLink**](icontextlink.md) da [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="be150-119">The [**\_IAnalysisProxyEvents::ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) event before it removes a [**IContextLink**](icontextlink.md) from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="be150-120">Evento **\_ IAnalysisProxyEvents:: l'ContextNodeDeleting** prima di rimuovere un nodo di contesto padre che non contiene più nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="be150-120">The **\_IAnalysisProxyEvents::ContextNodeDeleting** event before it removes a parent context node that no longer has child nodes.</span></span>

<span data-ttu-id="be150-121">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="be150-121">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be150-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be150-122">Requirements</span></span>



| <span data-ttu-id="be150-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="be150-123">Requirement</span></span> | <span data-ttu-id="be150-124">Valore</span><span class="sxs-lookup"><span data-stu-id="be150-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be150-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be150-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be150-126">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="be150-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be150-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be150-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be150-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="be150-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be150-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be150-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be150-130"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be150-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="be150-131">DLL</span><span class="sxs-lookup"><span data-stu-id="be150-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be150-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be150-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="be150-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be150-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be150-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="be150-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="be150-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="be150-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="be150-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="be150-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="be150-137">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="be150-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="be150-138">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="be150-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="be150-139">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="be150-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




