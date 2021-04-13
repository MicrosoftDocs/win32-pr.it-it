---
description: Si verifica quando IInkAnalyzer è pronto per risolvere i risultati dell'analisi in background con lo stato corrente.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: 'Evento _IAnalysisEvents:: ReadyToReconcile (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234553"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a><span data-ttu-id="8c657-103">\_Evento IAnalysisEvents:: ReadyToReconcile</span><span class="sxs-lookup"><span data-stu-id="8c657-103">\_IAnalysisEvents::ReadyToReconcile event</span></span>

<span data-ttu-id="8c657-104">Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) è pronto per risolvere i risultati dell'analisi in background con lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="8c657-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c657-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c657-105">Syntax</span></span>


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a><span data-ttu-id="8c657-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c657-106">Parameters</span></span>

<span data-ttu-id="8c657-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="8c657-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c657-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c657-108">Return value</span></span>

<span data-ttu-id="8c657-109">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8c657-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c657-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c657-110">Remarks</span></span>

<span data-ttu-id="8c657-111">[**IInkAnalyzer**](iinkanalyzer.md) esegue la riconciliazione automatica quando viene impostato il flag **AnalysisModes \_ AutomaticReconciliation** dell'analizzatore di input penna (vedere il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="8c657-111">The [**IInkAnalyzer**](iinkanalyzer.md) performs automatic reconciliation when the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag is set (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)).</span></span> <span data-ttu-id="8c657-112">Quando il flag **AnalysisModes \_ AutomaticReconciliation** non è impostato, l'applicazione deve riconciliare manualmente i risultati dell'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="8c657-112">When the **AnalysisModes\_AutomaticReconciliation** flag is not set, your application needs to reconcile background analysis results manually.</span></span>

<span data-ttu-id="8c657-113">Per eseguire la riconciliazione manuale, attenersi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="8c657-113">To perform manual reconciliation, follow these steps.</span></span>

1.  <span data-ttu-id="8c657-114">Cancellare il flag **\_ AutomaticReconciliation AnalysisModes** dell'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="8c657-114">Clear the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag.</span></span>
2.  <span data-ttu-id="8c657-115">Gestire l'evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="8c657-115">Handle the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>
3.  <span data-ttu-id="8c657-116">Per risolvere i risultati dell'analisi, chiamare il metodo [**IInkAnalyzer:: riconcilia**](iinkanalyzer-reconcile.md) dal gestore eventi per l'evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="8c657-116">To reconcile the analysis results, call the [**IInkAnalyzer::Reconcile Method**](iinkanalyzer-reconcile.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span> <span data-ttu-id="8c657-117">Per annullare l'operazione di analisi in background corrente, chiamare il metodo [**IInkAnalyzer:: Abort**](iinkanalyzer-abort.md) dal gestore eventi per l'evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="8c657-117">To cancel the current background analysis operation, call the [**IInkAnalyzer::Abort Method**](iinkanalyzer-abort.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>

<span data-ttu-id="8c657-118">Il [**IInkAnalyzer**](iinkanalyzer.md) genera questo evento prima che venga generato l'evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="8c657-118">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event before it raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span>

<span data-ttu-id="8c657-119">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8c657-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="8c657-120">[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento durante l'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="8c657-120">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during background analysis.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c657-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c657-121">Requirements</span></span>



| <span data-ttu-id="8c657-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c657-122">Requirement</span></span> | <span data-ttu-id="8c657-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8c657-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c657-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c657-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8c657-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8c657-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8c657-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c657-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8c657-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8c657-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8c657-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c657-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c657-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8c657-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8c657-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8c657-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c657-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c657-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8c657-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c657-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c657-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="8c657-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="8c657-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="8c657-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="8c657-135">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="8c657-135">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="8c657-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8c657-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8c657-137">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="8c657-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="8c657-138">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="8c657-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="8c657-139">**Metodo IInkAnalyzer:: riconcilia**</span><span class="sxs-lookup"><span data-stu-id="8c657-139">**IInkAnalyzer::Reconcile Method**</span></span>](iinkanalyzer-reconcile.md)
</dt> <dt>

[<span data-ttu-id="8c657-140">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="8c657-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




