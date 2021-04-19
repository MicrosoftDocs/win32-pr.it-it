---
description: Recupera tutti gli oggetti IContextNode del tipo specificato che sono discendenti dell'oggetto IContextNode specificato.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 545e56d297b053b5b6f5dc61f944d6a4f6d4e03c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307389"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a><span data-ttu-id="a265c-103">Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree</span><span class="sxs-lookup"><span data-stu-id="a265c-103">IInkAnalyzer::FindNodesOfTypeInSubTree method</span></span>

<span data-ttu-id="a265c-104">Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato che sono discendenti dell'oggetto **IContextNode** specificato.</span><span class="sxs-lookup"><span data-stu-id="a265c-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a265c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a265c-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="a265c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a265c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a265c-107">*pNodeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a265c-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a265c-108">**GUID** che specifica il tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="a265c-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="a265c-109">*pContextNodeToSearchFrom* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a265c-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a265c-110">Oggetto [**IContextNode**](icontextnode.md) di cui vengono cercati i discendenti.</span><span class="sxs-lookup"><span data-stu-id="a265c-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="a265c-111">*ppContextNodesFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a265c-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a265c-112">Raccolta [**IContextNodes**](icontextnodes.md) contenente tutti i nodi di tipo *pNodeType* che sono discendenti di *pContextNodeToSearchFrom*.</span><span class="sxs-lookup"><span data-stu-id="a265c-112">The [**IContextNodes**](icontextnodes.md) collection containing all nodes of type *pNodeType* that are descendants of *pContextNodeToSearchFrom*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a265c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a265c-113">Return value</span></span>

<span data-ttu-id="a265c-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a265c-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a265c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a265c-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a265c-116">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a265c-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a265c-117">Se il [**IInkAnalyzer**](iinkanalyzer.md) non contiene il nodo *pContextNodeToSearchFrom* , questo metodo restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="a265c-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="a265c-118">La proprietà *pNodeType* deve contenere un identificatore univoco globale (Guid) dalle costanti dei [tipi di nodo di contesto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="a265c-118">The *pNodeType* property must contain a globally unique identifier (GUID) from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="a265c-119">Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene alcun [**IContextNode**](icontextnode.md), viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.</span><span class="sxs-lookup"><span data-stu-id="a265c-119">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a265c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a265c-120">Requirements</span></span>



| <span data-ttu-id="a265c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a265c-121">Requirement</span></span> | <span data-ttu-id="a265c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a265c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a265c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a265c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a265c-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a265c-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a265c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a265c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a265c-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a265c-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a265c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a265c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a265c-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a265c-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a265c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a265c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a265c-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a265c-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a265c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a265c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a265c-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a265c-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a265c-133">**Metodo IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="a265c-133">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="a265c-134">**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="a265c-134">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="a265c-135">**Metodo IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="a265c-135">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="a265c-136">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="a265c-136">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="a265c-137">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="a265c-137">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="a265c-138">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="a265c-138">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="a265c-139">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="a265c-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="a265c-140">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="a265c-140">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="a265c-141">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="a265c-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

