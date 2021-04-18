---
description: Si verifica prima che l'analizzatore input penna aggiunga un oggetto IContextLink tra due oggetti IContextNode.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: 'Evento _IAnalysisProxyEvents:: ContextNodeLinkAdding (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 341c551064869532e8b51ddecdbe1d5a78878abd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320914"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a><span data-ttu-id="7b229-103">\_Evento IAnalysisProxyEvents:: ContextNodeLinkAdding</span><span class="sxs-lookup"><span data-stu-id="7b229-103">\_IAnalysisProxyEvents::ContextNodeLinkAdding event</span></span>

<span data-ttu-id="7b229-104">Si verifica prima che l'analizzatore input penna aggiunga un oggetto [**IContextLink**](icontextlink.md) tra due oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="7b229-104">Occurs before the ink analyzer adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b229-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b229-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a><span data-ttu-id="7b229-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b229-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b229-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b229-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b229-108">[**IInkAnalyzer**](iinkanalyzer.md) che aggiunge il collegamento.</span><span class="sxs-lookup"><span data-stu-id="7b229-108">The [**IInkAnalyzer**](iinkanalyzer.md) adding the link.</span></span>

</dd> <dt>

<span data-ttu-id="7b229-109">*pContextLinkToBeAdded* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b229-109">*pContextLinkToBeAdded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b229-110">Oggetto [**IContextLink**](icontextlink.md) da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7b229-110">The [**IContextLink**](icontextlink.md) object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b229-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b229-111">Return value</span></span>

<span data-ttu-id="7b229-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7b229-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b229-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b229-113">Remarks</span></span>

<span data-ttu-id="7b229-114">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7b229-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="7b229-115">Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che aggiunge un nuovo [**IContextLink**](icontextlink.md) a un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="7b229-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that adds a new [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="7b229-116">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7b229-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b229-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b229-117">Requirements</span></span>



| <span data-ttu-id="7b229-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b229-118">Requirement</span></span> | <span data-ttu-id="7b229-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7b229-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b229-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b229-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7b229-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b229-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b229-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b229-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7b229-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7b229-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7b229-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b229-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b229-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b229-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b229-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7b229-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b229-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b229-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7b229-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b229-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b229-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="7b229-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="7b229-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7b229-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7b229-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="7b229-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7b229-132">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="7b229-132">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="7b229-133">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="7b229-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="7b229-134">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="7b229-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="7b229-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="7b229-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




