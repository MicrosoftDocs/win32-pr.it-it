---
description: Recupera tutti i nodi foglia dell'input penna.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'Metodo IInkAnalyzer:: FindInkLeafNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879341"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a><span data-ttu-id="98a82-103">Metodo IInkAnalyzer:: FindInkLeafNodes</span><span class="sxs-lookup"><span data-stu-id="98a82-103">IInkAnalyzer::FindInkLeafNodes method</span></span>

<span data-ttu-id="98a82-104">Recupera tutti i nodi foglia dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="98a82-104">Retrieves all of the ink leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="98a82-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98a82-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="98a82-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98a82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98a82-107">*ppContextNodesFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="98a82-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98a82-108">Puntatore alla raccolta [**IContextNodes**](icontextnodes.md) contenente tutti i nodi foglia dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="98a82-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all ink leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98a82-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98a82-109">Return value</span></span>

<span data-ttu-id="98a82-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="98a82-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="98a82-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="98a82-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="98a82-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="98a82-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="98a82-113">I nodi foglia non contengono nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="98a82-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="98a82-114">I nodi Ink contengono dati Stroke.</span><span class="sxs-lookup"><span data-stu-id="98a82-114">Ink nodes contain stroke data.</span></span> <span data-ttu-id="98a82-115">Esempi di nodi foglia input penna sono oggetti InkWord, InkDrawing e InkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="98a82-115">Examples of ink leaf nodes are InkWord, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="98a82-116">Per altre informazioni, vedere [tipi di nodo di contesto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="98a82-116">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98a82-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98a82-117">Requirements</span></span>



| <span data-ttu-id="98a82-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="98a82-118">Requirement</span></span> | <span data-ttu-id="98a82-119">Valore</span><span class="sxs-lookup"><span data-stu-id="98a82-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98a82-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98a82-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98a82-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="98a82-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="98a82-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98a82-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98a82-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="98a82-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="98a82-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98a82-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="98a82-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="98a82-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="98a82-126">DLL</span><span class="sxs-lookup"><span data-stu-id="98a82-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98a82-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98a82-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="98a82-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98a82-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a82-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="98a82-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="98a82-130">**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="98a82-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="98a82-131">**Metodo IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="98a82-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="98a82-132">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="98a82-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="98a82-133">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="98a82-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="98a82-134">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="98a82-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="98a82-135">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="98a82-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="98a82-136">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="98a82-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="98a82-137">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="98a82-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="98a82-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="98a82-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

