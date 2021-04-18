---
description: Si verifica quando IInkAnalyzer sposta un tratto da un oggetto IContextNode a un altro.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: 'Evento _IAnalysisProxyEvents:: StrokeReparented (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320902"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a><span data-ttu-id="edd13-103">\_Evento IAnalysisProxyEvents:: StrokeReparented</span><span class="sxs-lookup"><span data-stu-id="edd13-103">\_IAnalysisProxyEvents::StrokeReparented event</span></span>

<span data-ttu-id="edd13-104">Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) sposta un tratto da un oggetto [**IContextNode**](icontextnode.md) a un altro.</span><span class="sxs-lookup"><span data-stu-id="edd13-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd13-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edd13-105">Syntax</span></span>


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="edd13-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="edd13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd13-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edd13-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd13-108">Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che sposta il tratto.</span><span class="sxs-lookup"><span data-stu-id="edd13-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="edd13-109">*lStrokeIdToMove* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edd13-109">*lStrokeIdToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd13-110">Identificatore del tratto da spostare.</span><span class="sxs-lookup"><span data-stu-id="edd13-110">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="edd13-111">*pSourceContextNode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edd13-111">*pSourceContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd13-112">Oggetto [**IContextNode**](icontextnode.md) da cui viene spostato il tratto.</span><span class="sxs-lookup"><span data-stu-id="edd13-112">The [**IContextNode**](icontextnode.md) object from which the stroke is moved.</span></span>

</dd> <dt>

<span data-ttu-id="edd13-113">*pDestinationContextNode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edd13-113">*pDestinationContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd13-114">Oggetto [**IContextNode**](icontextnode.md) in cui viene spostato il tratto.</span><span class="sxs-lookup"><span data-stu-id="edd13-114">The [**IContextNode**](icontextnode.md) object to which the stroke is moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd13-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edd13-115">Return value</span></span>

<span data-ttu-id="edd13-116">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="edd13-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="edd13-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="edd13-117">Remarks</span></span>

<span data-ttu-id="edd13-118">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="edd13-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="edd13-119">Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo **IInkAnalyzer** che sposta i dati del tratto da un [**IContextNode**](icontextnode.md) a un altro.</span><span class="sxs-lookup"><span data-stu-id="edd13-119">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that moves stroke data from one [**IContextNode**](icontextnode.md) to another.</span></span>

<span data-ttu-id="edd13-120">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="edd13-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edd13-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edd13-121">Requirements</span></span>



| <span data-ttu-id="edd13-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="edd13-122">Requirement</span></span> | <span data-ttu-id="edd13-123">Valore</span><span class="sxs-lookup"><span data-stu-id="edd13-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd13-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edd13-124">Minimum supported client</span></span><br/> | <span data-ttu-id="edd13-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="edd13-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="edd13-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edd13-126">Minimum supported server</span></span><br/> | <span data-ttu-id="edd13-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="edd13-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="edd13-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edd13-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="edd13-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="edd13-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="edd13-130">DLL</span><span class="sxs-lookup"><span data-stu-id="edd13-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edd13-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd13-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="edd13-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edd13-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd13-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="edd13-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="edd13-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="edd13-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="edd13-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="edd13-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="edd13-136">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="edd13-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="edd13-137">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="edd13-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="edd13-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="edd13-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




