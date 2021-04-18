---
description: Si verifica prima che i IInkAnalyzer riconciliano i risultati dell'analisi in modo che un'applicazione possa sincronizzare i dati con IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: 'Evento _IAnalysisProxyEvents:: InkAnalyzerStateChanging (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320903"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a><span data-ttu-id="e688e-103">\_Evento IAnalysisProxyEvents:: InkAnalyzerStateChanging</span><span class="sxs-lookup"><span data-stu-id="e688e-103">\_IAnalysisProxyEvents::InkAnalyzerStateChanging event</span></span>

<span data-ttu-id="e688e-104">Si verifica prima che i [**IInkAnalyzer**](iinkanalyzer.md) riconciliano i risultati dell'analisi in modo che un'applicazione possa sincronizzare i dati con **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="e688e-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e688e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e688e-105">Syntax</span></span>


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a><span data-ttu-id="e688e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e688e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e688e-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e688e-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e688e-108">[**IInkAnalyzer**](iinkanalyzer.md) che sta per risolvere i risultati dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="e688e-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is about to reconcile its analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e688e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e688e-109">Return value</span></span>

<span data-ttu-id="e688e-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e688e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e688e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e688e-111">Remarks</span></span>

<span data-ttu-id="e688e-112">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e688e-112">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="e688e-113">Quando **IInkAnalyzer** genera questo evento, l'applicazione deve popolare i sottonodi del nodo radice dell'analizzatore di input penna (vedere il metodo [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="e688e-113">When the **IInkAnalyzer** raises this event, your application should populate the subnodes of the ink analyzer's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="e688e-114">[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo che ha generato l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="e688e-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="e688e-115">Genera questo evento solo durante l'esecuzione dell'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="e688e-115">It raises this event only while performing background analysis.</span></span>

<span data-ttu-id="e688e-116">Bloccare la struttura dei dati quando [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento **\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging** .</span><span class="sxs-lookup"><span data-stu-id="e688e-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the **\_IAnalysisProxyEvents::InkAnalyzerStateChanging** event.</span></span> <span data-ttu-id="e688e-117">Le modifiche apportate alla struttura dei dati durante questa fase dell'analisi possono causare errori nell'analisi dell'input penna e nella sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e688e-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="e688e-118">Sbloccare la struttura dei dati quando **IInkAnalyzer** genera l'evento [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="e688e-118">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="e688e-119">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e688e-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e688e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e688e-120">Requirements</span></span>



| <span data-ttu-id="e688e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e688e-121">Requirement</span></span> | <span data-ttu-id="e688e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e688e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e688e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e688e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e688e-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e688e-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e688e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e688e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e688e-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e688e-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e688e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e688e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e688e-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e688e-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e688e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e688e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e688e-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e688e-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e688e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e688e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e688e-132">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="e688e-132">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="e688e-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e688e-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e688e-134">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e688e-134">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e688e-135">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="e688e-135">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="e688e-136">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="e688e-136">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="e688e-137">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="e688e-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




