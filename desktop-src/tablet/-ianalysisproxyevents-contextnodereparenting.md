---
description: Si verifica prima che IInkAnalyzer sposti un oggetto IContextNode modificando il relativo nodo padre.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: "Evento _IAnalysisProxyEvents:: l'ContextNodeReparenting (IACom. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320950"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a><span data-ttu-id="b42ad-103">\_Evento IAnalysisProxyEvents:: l'ContextNodeReparenting</span><span class="sxs-lookup"><span data-stu-id="b42ad-103">\_IAnalysisProxyEvents::ContextNodeReparenting event</span></span>

<span data-ttu-id="b42ad-104">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) sposti un oggetto [**IContextNode**](icontextnode.md) modificando il relativo nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b42ad-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span>

## <a name="syntax"></a><span data-ttu-id="b42ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b42ad-105">Syntax</span></span>


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a><span data-ttu-id="b42ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b42ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b42ad-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b42ad-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b42ad-108">Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che trasferisce l'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b42ad-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b42ad-109">*pNewParentContextNode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b42ad-109">*pNewParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b42ad-110">Nuovo oggetto [**IContextNode**](icontextnode.md) padre.</span><span class="sxs-lookup"><span data-stu-id="b42ad-110">The new parent [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b42ad-111">*pContextNodeToBeReparented* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b42ad-111">*pContextNodeToBeReparented* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b42ad-112">Oggetto [**IContextNode**](icontextnode.md) da spostare.</span><span class="sxs-lookup"><span data-stu-id="b42ad-112">The [**IContextNode**](icontextnode.md) object to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b42ad-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b42ad-113">Return value</span></span>

<span data-ttu-id="b42ad-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b42ad-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b42ad-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b42ad-115">Remarks</span></span>

<span data-ttu-id="b42ad-116">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="b42ad-116">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="b42ad-117">Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo che sposta un [**IContextNode**](icontextnode.md) da una raccolta di sottonodi a un'altra (vedere [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="b42ad-117">This event occurs during the reconcile phase of ink analysis, or in response to a method that moves an [**IContextNode**](icontextnode.md) from one collection of subnodes to another (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="b42ad-118">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b42ad-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b42ad-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b42ad-119">Requirements</span></span>



| <span data-ttu-id="b42ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b42ad-120">Requirement</span></span> | <span data-ttu-id="b42ad-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b42ad-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b42ad-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b42ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b42ad-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b42ad-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b42ad-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b42ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b42ad-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b42ad-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b42ad-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b42ad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b42ad-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b42ad-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b42ad-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b42ad-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b42ad-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b42ad-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b42ad-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b42ad-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b42ad-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="b42ad-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="b42ad-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b42ad-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b42ad-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b42ad-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b42ad-134">**IContextNode:: GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="b42ad-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="b42ad-135">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="b42ad-135">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="b42ad-136">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="b42ad-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b42ad-137">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="b42ad-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b42ad-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b42ad-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




