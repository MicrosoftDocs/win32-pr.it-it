---
description: Si verifica prima che IInkAnalyzer sposti un oggetto IContextNode in una nuova posizione all'interno della relativa raccolta di nodi padre.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: 'Evento _IAnalysisProxyEvents:: ContextNodeMovingToPosition (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320904"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a><span data-ttu-id="c20c4-103">\_Evento IAnalysisProxyEvents:: ContextNodeMovingToPosition</span><span class="sxs-lookup"><span data-stu-id="c20c4-103">\_IAnalysisProxyEvents::ContextNodeMovingToPosition event</span></span>

<span data-ttu-id="c20c4-104">Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) sposti un oggetto [**IContextNode**](icontextnode.md) in una nuova posizione all'interno della relativa raccolta di nodi padre.</span><span class="sxs-lookup"><span data-stu-id="c20c4-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c20c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c20c4-105">Syntax</span></span>


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c20c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c20c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c20c4-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c20c4-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20c4-108">Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che trasferisce l'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c20c4-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c20c4-109">*pISubNodeToMove* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c20c4-109">*pISubNodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20c4-110">Oggetto [**IContextNode**](icontextnode.md) da spostare.</span><span class="sxs-lookup"><span data-stu-id="c20c4-110">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="c20c4-111">*pParentContextNode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c20c4-111">*pParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20c4-112">Oggetto [**IContextNode**](icontextnode.md) padre di *pISubNodeToMove*.</span><span class="sxs-lookup"><span data-stu-id="c20c4-112">The parent [**IContextNode**](icontextnode.md) object of *pISubNodeToMove*.</span></span>

</dd> <dt>

<span data-ttu-id="c20c4-113">*ulNewIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c20c4-113">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20c4-114">Nuova posizione di *pISubNodeToMove* nella raccolta di sottonodi del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="c20c4-114">The new location of *pISubNodeToMove* in its parent node's collection of subnodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c20c4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c20c4-115">Return value</span></span>

<span data-ttu-id="c20c4-116">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c20c4-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c20c4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c20c4-117">Remarks</span></span>

<span data-ttu-id="c20c4-118">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="c20c4-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="c20c4-119">Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che sposta un [**IContextNode**](icontextnode.md) all'interno della relativa raccolta di nodi padre (vedere [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="c20c4-119">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that moves an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="c20c4-120">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c20c4-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c20c4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c20c4-121">Requirements</span></span>



| <span data-ttu-id="c20c4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c20c4-122">Requirement</span></span> | <span data-ttu-id="c20c4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c20c4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c20c4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c20c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c20c4-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c20c4-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c20c4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c20c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c20c4-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c20c4-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c20c4-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c20c4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c20c4-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c20c4-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c20c4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c20c4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c20c4-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c20c4-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c20c4-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c20c4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c20c4-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="c20c4-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="c20c4-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c20c4-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c20c4-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c20c4-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c20c4-136">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="c20c4-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="c20c4-137">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="c20c4-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="c20c4-138">**IContextNode:: GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="c20c4-138">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="c20c4-139">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="c20c4-139">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="c20c4-140">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c20c4-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




