---
description: Si verifica prima che IInkAnalyzer esegua l'analisi all'interno dell'area di un oggetto IContextNode parzialmente popolato.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P evento opulateContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234560"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a><span data-ttu-id="b5326-103">\_IAnalysisProxyEvents::P evento opulateContextNode</span><span class="sxs-lookup"><span data-stu-id="b5326-103">\_IAnalysisProxyEvents::PopulateContextNode event</span></span>

<span data-ttu-id="b5326-104">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) esegua l'analisi all'interno dell'area di un oggetto [**IContextNode**](icontextnode.md) parzialmente popolato.</span><span class="sxs-lookup"><span data-stu-id="b5326-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5326-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5326-105">Syntax</span></span>


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a><span data-ttu-id="b5326-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5326-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5326-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5326-108">Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che sta per eseguire l'analisi.</span><span class="sxs-lookup"><span data-stu-id="b5326-108">The [**IInkAnalyzer**](iinkanalyzer.md) object about to perform analysis.</span></span>

</dd> <dt>

<span data-ttu-id="b5326-109">*pContextNodeToPopulate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5326-109">*pContextNodeToPopulate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5326-110">Oggetto [**IContextNode**](icontextnode.md) parzialmente popolato.</span><span class="sxs-lookup"><span data-stu-id="b5326-110">The partially populated [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5326-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5326-111">Return value</span></span>

<span data-ttu-id="b5326-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b5326-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5326-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5326-113">Remarks</span></span>

<span data-ttu-id="b5326-114">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="b5326-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="b5326-115">Quando **IInkAnalyzer** genera questo evento, l'applicazione deve popolare il *pContextNodeToPopulate*.</span><span class="sxs-lookup"><span data-stu-id="b5326-115">When the **IInkAnalyzer** raises this event, your application should populate the *pContextNodeToPopulate*.</span></span> <span data-ttu-id="b5326-116">Durante la fase di analisi, **IInkAnalyzer** genera questo evento per ottenere informazioni per le aree in cui analizza l'input penna.</span><span class="sxs-lookup"><span data-stu-id="b5326-116">During the analysis phase, the **IInkAnalyzer** raises this event to get information for areas in which it is analyzing ink.</span></span>

<span data-ttu-id="b5326-117">Se il documento contiene collegamenti per *pContextNodeToPopulate*, l'applicazione deve creare e aggiungere questi collegamenti.</span><span class="sxs-lookup"><span data-stu-id="b5326-117">If the document contains links for the *pContextNodeToPopulate*, your application should create and add these links.</span></span> <span data-ttu-id="b5326-118">Questo processo richiede che i nodi di origine e di destinazione, inclusi i relativi predecessori, siano popolati completamente prima che il gestore eventi per questo evento venga chiuso (vedere [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="b5326-118">This process requires that both the source and destination nodes, including their ancestors, are fully populated before the event handler for this event exits (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span>

<span data-ttu-id="b5326-119">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b5326-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="b5326-120">Durante l'analisi in background, [**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo che ha generato l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="b5326-120">During background analysis, the [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5326-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5326-121">Requirements</span></span>



| <span data-ttu-id="b5326-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5326-122">Requirement</span></span> | <span data-ttu-id="b5326-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b5326-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5326-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5326-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b5326-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b5326-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5326-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5326-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b5326-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b5326-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b5326-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5326-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5326-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b5326-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b5326-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b5326-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5326-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5326-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b5326-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5326-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5326-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="b5326-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="b5326-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b5326-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b5326-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b5326-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b5326-136">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="b5326-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b5326-137">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="b5326-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b5326-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b5326-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




