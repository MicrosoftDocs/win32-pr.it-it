---
description: Si verifica prima che IInkAnalyzer elimini un oggetto IContextLink tra due oggetti IContextNode.
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: "Evento _IAnalysisProxyEvents:: l'ContextNodeLinkDeleting (IACom. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc4ba9586fc4c520b9ee44b039bd56f8ef2ade3c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234551"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a><span data-ttu-id="404ef-103">\_Evento IAnalysisProxyEvents:: l'ContextNodeLinkDeleting</span><span class="sxs-lookup"><span data-stu-id="404ef-103">\_IAnalysisProxyEvents::ContextNodeLinkDeleting event</span></span>

<span data-ttu-id="404ef-104">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un oggetto [**IContextLink**](icontextlink.md) tra due oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="404ef-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="404ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="404ef-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="404ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="404ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="404ef-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="404ef-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="404ef-108">[**IInkAnalyzer**](iinkanalyzer.md) che elimina il collegamento.</span><span class="sxs-lookup"><span data-stu-id="404ef-108">The [**IInkAnalyzer**](iinkanalyzer.md) deleting the link.</span></span>

</dd> <dt>

<span data-ttu-id="404ef-109">*pContextLinkToBeDeleted* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="404ef-109">*pContextLinkToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="404ef-110">Oggetto [**IContextLink**](icontextlink.md) da eliminare.</span><span class="sxs-lookup"><span data-stu-id="404ef-110">The [**IContextLink**](icontextlink.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="404ef-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="404ef-111">Return value</span></span>

<span data-ttu-id="404ef-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="404ef-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="404ef-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="404ef-113">Remarks</span></span>

<span data-ttu-id="404ef-114">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="404ef-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="404ef-115">Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo **IInkAnalyzer** che rimuove un [**IContextLink**](icontextlink.md) da un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="404ef-115">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that removes an [**IContextLink**](icontextlink.md) from an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="404ef-116">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="404ef-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="404ef-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="404ef-117">Requirements</span></span>



| <span data-ttu-id="404ef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="404ef-118">Requirement</span></span> | <span data-ttu-id="404ef-119">Valore</span><span class="sxs-lookup"><span data-stu-id="404ef-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="404ef-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="404ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="404ef-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="404ef-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="404ef-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="404ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="404ef-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="404ef-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="404ef-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="404ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="404ef-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="404ef-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="404ef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="404ef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="404ef-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="404ef-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="404ef-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="404ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="404ef-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="404ef-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="404ef-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="404ef-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="404ef-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="404ef-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="404ef-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="404ef-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="404ef-133">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="404ef-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="404ef-134">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="404ef-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="404ef-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="404ef-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




