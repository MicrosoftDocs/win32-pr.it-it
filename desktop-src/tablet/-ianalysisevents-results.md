---
description: Si verifica al termine della fase di analisi finale.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: 'Evento _IAnalysisEvents:: results (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320918"
---
# <a name="_ianalysiseventsresults-event"></a><span data-ttu-id="c6e2c-103">\_Evento IAnalysisEvents:: results</span><span class="sxs-lookup"><span data-stu-id="c6e2c-103">\_IAnalysisEvents::Results event</span></span>

<span data-ttu-id="c6e2c-104">Si verifica al termine della fase di analisi finale.</span><span class="sxs-lookup"><span data-stu-id="c6e2c-104">Occurs when the final analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e2c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6e2c-105">Syntax</span></span>


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c6e2c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6e2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6e2c-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6e2c-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e2c-108">[**IInkAnalyzer**](iinkanalyzer.md) che produce i risultati dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="c6e2c-108">The [**IInkAnalyzer**](iinkanalyzer.md) that produces the analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="c6e2c-109">*pAnalysisStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6e2c-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e2c-110">Oggetto [**IAnalysisStatus**](ianalysisstatus.md) che rappresenta lo stato dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="c6e2c-110">The [**IAnalysisStatus**](ianalysisstatus.md) object that represents the status of the analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6e2c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6e2c-111">Return value</span></span>

<span data-ttu-id="c6e2c-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c6e2c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e2c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6e2c-113">Remarks</span></span>

<span data-ttu-id="c6e2c-114">[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo aver riconciliato i risultati per la fase di analisi finale.</span><span class="sxs-lookup"><span data-stu-id="c6e2c-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the results for the final analysis stage.</span></span>

<span data-ttu-id="c6e2c-115">Se l'applicazione chiama il [**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), questo evento segnala quando i risultati dell'analisi sono pronti.</span><span class="sxs-lookup"><span data-stu-id="c6e2c-115">If your application calls [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), this event signals when analysis results are ready.</span></span>

<span data-ttu-id="c6e2c-116">Se l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md), questo evento indica che il **IInkAnalyzer** ha completato le modifiche ai dati interni per questa fase di analisi.</span><span class="sxs-lookup"><span data-stu-id="c6e2c-116">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="c6e2c-117">Bloccare la struttura dei dati quando [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="c6e2c-117">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="c6e2c-118">Le modifiche apportate alla struttura dei dati durante questa fase dell'analisi possono causare errori nell'analisi dell'input penna e nella sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c6e2c-118">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="c6e2c-119">Sbloccare la struttura dei dati quando **IInkAnalyzer** genera l'evento [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) o **\_ IAnalysisEvents:: results** .</span><span class="sxs-lookup"><span data-stu-id="c6e2c-119">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or **\_IAnalysisEvents::Results** event.</span></span>

<span data-ttu-id="c6e2c-120">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c6e2c-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e2c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6e2c-121">Requirements</span></span>



| <span data-ttu-id="c6e2c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6e2c-122">Requirement</span></span> | <span data-ttu-id="c6e2c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c6e2c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e2c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6e2c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e2c-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c6e2c-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c6e2c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6e2c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e2c-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c6e2c-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c6e2c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6e2c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e2c-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c6e2c-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c6e2c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c6e2c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6e2c-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6e2c-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c6e2c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6e2c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e2c-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="c6e2c-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="c6e2c-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="c6e2c-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="c6e2c-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c6e2c-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c6e2c-136">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="c6e2c-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="c6e2c-137">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="c6e2c-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="c6e2c-138">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="c6e2c-138">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="c6e2c-139">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c6e2c-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




