---
description: Recupera tutti gli oggetti IContextNode che corrispondono ai criteri specificati.
ms.assetid: c0ba46f4-a286-454a-8de2-6663fd2dfed6
title: 'Metodo IInkAnalyzer:: FindNodesWithCallBack (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b34501e33d637ca65f13e6e2e5ea0a9001b06198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751831"
---
# <a name="iinkanalyzerfindnodeswithcallback-method"></a><span data-ttu-id="dd135-103">Metodo IInkAnalyzer:: FindNodesWithCallBack</span><span class="sxs-lookup"><span data-stu-id="dd135-103">IInkAnalyzer::FindNodesWithCallBack method</span></span>

<span data-ttu-id="dd135-104">Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) che corrispondono ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="dd135-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd135-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd135-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBack(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="dd135-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd135-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd135-107">*pCriteria* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd135-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd135-108">Oggetto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) utilizzato per valutare se un oggetto [**IContextNode**](icontextnode.md) soddisfa o meno i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="dd135-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="dd135-109">*ppContextNodesFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd135-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd135-110">Puntatore alla raccolta [**IContextNodes**](icontextnodes.md) contenente tutti i nodi che soddisfano i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="dd135-110">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd135-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd135-111">Return value</span></span>

<span data-ttu-id="dd135-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dd135-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dd135-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd135-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dd135-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd135-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="dd135-115">Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene alcun [**IContextNode**](icontextnode.md), viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.</span><span class="sxs-lookup"><span data-stu-id="dd135-115">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd135-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd135-116">Requirements</span></span>



| <span data-ttu-id="dd135-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd135-117">Requirement</span></span> | <span data-ttu-id="dd135-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dd135-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd135-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd135-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dd135-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dd135-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dd135-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd135-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dd135-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dd135-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dd135-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd135-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd135-124"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dd135-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dd135-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dd135-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd135-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd135-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dd135-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd135-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd135-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="dd135-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="dd135-129">**Metodo IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="dd135-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="dd135-130">**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="dd135-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="dd135-131">**Metodo IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="dd135-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="dd135-132">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="dd135-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="dd135-133">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="dd135-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="dd135-134">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="dd135-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="dd135-135">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="dd135-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="dd135-136">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="dd135-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="dd135-137">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="dd135-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

