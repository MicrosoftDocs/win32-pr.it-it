---
description: Si verifica prima che IInkAnalyzer acceda ai dati del tratto.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: 'Evento _IAnalysisEvents:: UpdateStrokesCache (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320915"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a><span data-ttu-id="dc4c6-103">\_Evento IAnalysisEvents:: UpdateStrokesCache</span><span class="sxs-lookup"><span data-stu-id="dc4c6-103">\_IAnalysisEvents::UpdateStrokesCache event</span></span>

<span data-ttu-id="dc4c6-104">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) acceda ai dati del tratto.</span><span class="sxs-lookup"><span data-stu-id="dc4c6-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc4c6-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="dc4c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc4c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc4c6-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc4c6-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc4c6-108">Il numero di identificatori di tratto in *plStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="dc4c6-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="dc4c6-109">*plStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc4c6-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc4c6-110">Identificatori dei tratti i cui dati del pacchetto sono stati cancellati.</span><span class="sxs-lookup"><span data-stu-id="dc4c6-110">The identifiers of the strokes whose packet data has been cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc4c6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc4c6-111">Return value</span></span>

<span data-ttu-id="dc4c6-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dc4c6-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc4c6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc4c6-113">Remarks</span></span>

<span data-ttu-id="dc4c6-114">[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento durante l'analisi dell'input penna quando accede a uno o più tratti per i quali sono stati cancellati i dati del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="dc4c6-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during ink analysis when it accesses one or more strokes for which the packet data has been cleared.</span></span> <span data-ttu-id="dc4c6-115">Per aggiornare i dati del pacchetto del tratto, usare il metodo [**IInkAnalyzer:: UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) .</span><span class="sxs-lookup"><span data-stu-id="dc4c6-115">To update the stroke packet data, use the [**IInkAnalyzer::UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) method.</span></span>

<span data-ttu-id="dc4c6-116">[**IInkAnalyzer**](iinkanalyzer.md) non genera questo evento quando si accede a un nodo foglia input penna parzialmente popolato quando il percorso del nodo non è stato impostato da **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="dc4c6-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise this event when accessing a partially populated ink leaf node when the location of the node has not been set by the **IInkAnalyzer**.</span></span>

<span data-ttu-id="dc4c6-117">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dc4c6-117">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc4c6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc4c6-118">Requirements</span></span>



| <span data-ttu-id="dc4c6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc4c6-119">Requirement</span></span> | <span data-ttu-id="dc4c6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dc4c6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4c6-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc4c6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc4c6-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dc4c6-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dc4c6-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc4c6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc4c6-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dc4c6-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dc4c6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc4c6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc4c6-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dc4c6-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dc4c6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dc4c6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc4c6-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc4c6-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dc4c6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc4c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4c6-130">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="dc4c6-130">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="dc4c6-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="dc4c6-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="dc4c6-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="dc4c6-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="dc4c6-133">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="dc4c6-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="dc4c6-134">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="dc4c6-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="dc4c6-135">**Metodo IInkAnalyzer:: UpdateStrokesData**</span><span class="sxs-lookup"><span data-stu-id="dc4c6-135">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="dc4c6-136">**IContextNode:: CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="dc4c6-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="dc4c6-137">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="dc4c6-137">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="dc4c6-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="dc4c6-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




