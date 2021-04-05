---
description: Recupera tutti gli oggetti IContextNode che corrispondono ai criteri specificati e sono discendenti dell'oggetto IContextNode specificato.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751826"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a><span data-ttu-id="55a78-103">Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree</span><span class="sxs-lookup"><span data-stu-id="55a78-103">IInkAnalyzer::FindNodesWithCallBackInSubTree method</span></span>

<span data-ttu-id="55a78-104">Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) che corrispondono ai criteri specificati e sono discendenti dell'oggetto **IContextNode** specificato.</span><span class="sxs-lookup"><span data-stu-id="55a78-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria and are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a78-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55a78-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="55a78-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55a78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a78-107">*pCriteria* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55a78-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a78-108">Oggetto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) utilizzato per valutare se un oggetto [**IContextNode**](icontextnode.md) soddisfa o meno i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="55a78-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="55a78-109">*pContextNodeToSearchFrom* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55a78-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a78-110">Oggetto [**IContextNode**](icontextnode.md) di cui vengono cercati i discendenti.</span><span class="sxs-lookup"><span data-stu-id="55a78-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="55a78-111">*ppContextNodesFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="55a78-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55a78-112">Puntatore a [**IContextNodes**](icontextnodes.md) contenente tutti i nodi che soddisfano i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="55a78-112">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a78-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55a78-113">Return value</span></span>

<span data-ttu-id="55a78-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="55a78-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55a78-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="55a78-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="55a78-116">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55a78-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="55a78-117">Se il [**IInkAnalyzer**](iinkanalyzer.md) non contiene il nodo *pContextNodeToSearchFrom* , questo metodo restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="55a78-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="55a78-118">Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene alcun [**IContextNode**](icontextnode.md), viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.</span><span class="sxs-lookup"><span data-stu-id="55a78-118">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a78-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55a78-119">Requirements</span></span>



| <span data-ttu-id="55a78-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="55a78-120">Requirement</span></span> | <span data-ttu-id="55a78-121">Valore</span><span class="sxs-lookup"><span data-stu-id="55a78-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a78-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55a78-122">Minimum supported client</span></span><br/> | <span data-ttu-id="55a78-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="55a78-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55a78-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55a78-124">Minimum supported server</span></span><br/> | <span data-ttu-id="55a78-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="55a78-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="55a78-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55a78-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="55a78-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="55a78-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="55a78-128">DLL</span><span class="sxs-lookup"><span data-stu-id="55a78-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a78-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a78-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="55a78-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55a78-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a78-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="55a78-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="55a78-132">**Metodo IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="55a78-132">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="55a78-133">**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="55a78-133">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="55a78-134">**Metodo IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="55a78-134">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="55a78-135">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="55a78-135">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="55a78-136">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="55a78-136">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="55a78-137">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="55a78-137">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="55a78-138">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="55a78-138">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="55a78-139">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="55a78-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="55a78-140">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="55a78-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

