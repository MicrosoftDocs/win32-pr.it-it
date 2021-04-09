---
description: Recupera tutti gli oggetti IContextNode del tipo specificato.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'Metodo IInkAnalyzer:: FindNodesOfType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879334"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a><span data-ttu-id="006d3-103">Metodo IInkAnalyzer:: FindNodesOfType</span><span class="sxs-lookup"><span data-stu-id="006d3-103">IInkAnalyzer::FindNodesOfType method</span></span>

<span data-ttu-id="006d3-104">Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="006d3-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="006d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="006d3-105">Syntax</span></span>


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="006d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="006d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="006d3-107">*pNodeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="006d3-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="006d3-108">**GUID** che specifica il tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="006d3-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="006d3-109">*ppContextNodesFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="006d3-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="006d3-110">Puntatore a [**IContextNodes**](icontextnodes.md) contenente tutti i nodi di tipo *pNodeType*.</span><span class="sxs-lookup"><span data-stu-id="006d3-110">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes of type *pNodeType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="006d3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="006d3-111">Return value</span></span>

<span data-ttu-id="006d3-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="006d3-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="006d3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="006d3-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="006d3-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="006d3-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="006d3-115">La proprietà *pNodeType* deve contenere un GUID dalle costanti dei [tipi di nodo di contesto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="006d3-115">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="006d3-116">Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene alcun [**IContextNode**](icontextnode.md), viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.</span><span class="sxs-lookup"><span data-stu-id="006d3-116">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="006d3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="006d3-117">Requirements</span></span>



| <span data-ttu-id="006d3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="006d3-118">Requirement</span></span> | <span data-ttu-id="006d3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="006d3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="006d3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="006d3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="006d3-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="006d3-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="006d3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="006d3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="006d3-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="006d3-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="006d3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="006d3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="006d3-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="006d3-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="006d3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="006d3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="006d3-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="006d3-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="006d3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="006d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006d3-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="006d3-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="006d3-130">**Metodo IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="006d3-130">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="006d3-131">**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="006d3-131">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="006d3-132">**Metodo IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="006d3-132">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="006d3-133">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="006d3-133">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="006d3-134">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="006d3-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="006d3-135">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="006d3-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="006d3-136">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="006d3-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="006d3-137">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="006d3-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="006d3-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="006d3-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

