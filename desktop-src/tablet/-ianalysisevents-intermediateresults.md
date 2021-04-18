---
description: Si verifica al termine della fase di analisi intermedia corrente.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: 'Evento _IAnalysisEvents:: IntermediateResults () (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320905"
---
# <a name="_ianalysiseventsintermediateresults-event"></a><span data-ttu-id="9ef42-103">\_Evento IAnalysisEvents:: IntermediateResults ()</span><span class="sxs-lookup"><span data-stu-id="9ef42-103">\_IAnalysisEvents::IntermediateResults event</span></span>

<span data-ttu-id="9ef42-104">Si verifica al termine della fase di analisi intermedia corrente.</span><span class="sxs-lookup"><span data-stu-id="9ef42-104">Occurs when the current intermediate analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef42-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ef42-105">Syntax</span></span>


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="9ef42-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ef42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef42-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ef42-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ef42-108">[**IInkAnalyzer**](iinkanalyzer.md) che sta eseguendo l'analisi.</span><span class="sxs-lookup"><span data-stu-id="9ef42-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is performing the analysis.</span></span>

</dd> <dt>

<span data-ttu-id="9ef42-109">*pAnalysisStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ef42-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ef42-110">Oggetto [**IAnalysisStatus**](ianalysisstatus.md) che rappresenta lo stato dei risultati intermedi.</span><span class="sxs-lookup"><span data-stu-id="9ef42-110">The [**IAnalysisStatus**](ianalysisstatus.md) object representing the status of the intermediate results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef42-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ef42-111">Return value</span></span>

<span data-ttu-id="9ef42-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9ef42-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef42-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ef42-113">Remarks</span></span>

<span data-ttu-id="9ef42-114">[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo aver riconciliato i risultati intermedi per la fase di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="9ef42-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the intermediate results for the current analysis stage.</span></span>

<span data-ttu-id="9ef42-115">Se l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md), questo evento indica che il **IInkAnalyzer** ha completato le modifiche ai dati interni per questa fase di analisi.</span><span class="sxs-lookup"><span data-stu-id="9ef42-115">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="9ef42-116">Bloccare la struttura dei dati quando [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef42-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="9ef42-117">Le modifiche apportate alla struttura dei dati durante questa fase dell'analisi possono causare errori nell'analisi dell'input penna e nella sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="9ef42-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="9ef42-118">È possibile sbloccare la struttura dei dati quando **IInkAnalyzer** genera l'evento **\_ IAnalysisEvents:: IntermediateResults ()** o [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef42-118">You can unlock your data structure when the **IInkAnalyzer** raises the **\_IAnalysisEvents::IntermediateResults** or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="9ef42-119">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9ef42-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="9ef42-120">[**IInkAnalyzer**](iinkanalyzer.md) genera risultati intermedi solo quando le modalità di analisi hanno il flag **AnalysisModes \_ IntermediateResults ()** impostato (vedere il [**Metodo IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="9ef42-120">The [**IInkAnalyzer**](iinkanalyzer.md) generates intermediate results only when its analysis modes has the **AnalysisModes\_IntermediateResults** flag set (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef42-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ef42-121">Requirements</span></span>



| <span data-ttu-id="9ef42-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ef42-122">Requirement</span></span> | <span data-ttu-id="9ef42-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9ef42-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef42-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ef42-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef42-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9ef42-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9ef42-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ef42-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef42-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9ef42-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9ef42-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ef42-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef42-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9ef42-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9ef42-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9ef42-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ef42-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ef42-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9ef42-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ef42-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef42-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="9ef42-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="9ef42-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="9ef42-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="9ef42-135">**\_IAnalysisEvents:: results**</span><span class="sxs-lookup"><span data-stu-id="9ef42-135">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="9ef42-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="9ef42-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="9ef42-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9ef42-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9ef42-138">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="9ef42-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="9ef42-139">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="9ef42-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="9ef42-140">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="9ef42-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>
