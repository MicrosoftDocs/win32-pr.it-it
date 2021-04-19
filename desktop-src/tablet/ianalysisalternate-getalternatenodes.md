---
description: Ottiene gli oggetti IContextNode associati a questa alternativa.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'Metodo IAnalysisAlternate:: GetAlternateNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307478"
---
# <a name="ianalysisalternategetalternatenodes-method"></a><span data-ttu-id="ae4e7-103">Metodo IAnalysisAlternate:: GetAlternateNodes</span><span class="sxs-lookup"><span data-stu-id="ae4e7-103">IAnalysisAlternate::GetAlternateNodes method</span></span>

<span data-ttu-id="ae4e7-104">Ottiene gli oggetti [**IContextNode**](icontextnode.md) associati a questa alternativa.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-104">Gets the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae4e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae4e7-105">Syntax</span></span>


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a><span data-ttu-id="ae4e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae4e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae4e7-107">*ppAlternateNodes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae4e7-107">*ppAlternateNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae4e7-108">Puntatore alla raccolta [**IContextNodes**](icontextnodes.md) che contiene gli oggetti [**IContextNode**](icontextnode.md) associati a questa alternativa.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection that contains [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae4e7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae4e7-109">Return value</span></span>

<span data-ttu-id="ae4e7-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ae4e7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae4e7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae4e7-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ae4e7-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppAlternateNodes* quando non è più necessario usare la raccolta di nodi di contesto.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternateNodes* when you no longer need to use the context node collection.</span></span>

 

<span data-ttu-id="ae4e7-113">Questo metodo restituisce i nodi di contesto foglia associati a questa alternativa.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-113">This method returns the leaf context nodes that are associated with this alternate.</span></span> <span data-ttu-id="ae4e7-114">Esempi di nodi foglia sono i nodi di contesto InkWord, TextWord, image, InkDrawing e InkBullet.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-114">Examples of leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet context nodes.</span></span> <span data-ttu-id="ae4e7-115">Per altre informazioni, vedere [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipi di nodo di contesto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="ae4e7-115">For more information, see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="ae4e7-116">Poiché corrispondono a alternative, questi oggetti [**IContextNode**](icontextnode.md) non sono discendenti del **IContextNode** radice dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)), a meno che non siano l'alternativa superiore, ovvero il primo elemento di una raccolta [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4e7-116">Because they correspond to alternates, these [**IContextNode**](icontextnode.md) objects are not descendants of the [**IInkAnalyzer**](iinkanalyzer.md) object's root **IContextNode** (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)) unless they are the top alternate, which is the first element in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae4e7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae4e7-117">Requirements</span></span>



| <span data-ttu-id="ae4e7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae4e7-118">Requirement</span></span> | <span data-ttu-id="ae4e7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ae4e7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae4e7-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae4e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae4e7-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ae4e7-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ae4e7-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae4e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae4e7-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ae4e7-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ae4e7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae4e7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae4e7-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ae4e7-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ae4e7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ae4e7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae4e7-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae4e7-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ae4e7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae4e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae4e7-129">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="ae4e7-129">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="ae4e7-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ae4e7-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ae4e7-131">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="ae4e7-131">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="ae4e7-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ae4e7-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> <dt>

[<span data-ttu-id="ae4e7-133">System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. AlternateNodes</span><span class="sxs-lookup"><span data-stu-id="ae4e7-133">System.Windows.Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes</span></span>](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

