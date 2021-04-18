---
description: Quando sottoposto a override in una classe derivata, valuta se un oggetto IContextNode specificato soddisfa i criteri.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'Metodo IMatchesCriteriaCallBack:: EvaluateContextNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306752"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a><span data-ttu-id="b2e95-103">Metodo IMatchesCriteriaCallBack:: EvaluateContextNode</span><span class="sxs-lookup"><span data-stu-id="b2e95-103">IMatchesCriteriaCallBack::EvaluateContextNode method</span></span>

<span data-ttu-id="b2e95-104">Quando sottoposto a override in una classe derivata, valuta se un oggetto [**IContextNode**](icontextnode.md) specificato soddisfa i criteri.</span><span class="sxs-lookup"><span data-stu-id="b2e95-104">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e95-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2e95-105">Syntax</span></span>


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a><span data-ttu-id="b2e95-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2e95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e95-107">*pContextNodeToEvaluate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2e95-107">*pContextNodeToEvaluate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e95-108">Oggetto [**IContextNode**](icontextnode.md) da valutare.</span><span class="sxs-lookup"><span data-stu-id="b2e95-108">The [**IContextNode**](icontextnode.md) object to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="b2e95-109">*pbResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2e95-109">*pbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e95-110">**Variante \_ TRUE** se *pContextNodeToEvaluate* corrisponde ai criteri; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="b2e95-110">**VARIANT\_TRUE** if *pContextNodeToEvaluate* matches the criteria; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e95-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2e95-111">Return value</span></span>

<span data-ttu-id="b2e95-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b2e95-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e95-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2e95-113">Remarks</span></span>

<span data-ttu-id="b2e95-114">Per usare il metodo [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), creare una classe che implementi [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span><span class="sxs-lookup"><span data-stu-id="b2e95-114">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span></span> <span data-ttu-id="b2e95-115">Implementare **IMatchesCriteriaCallBack:: EvaluateContextNode** per restituire la **variante \_ true** se l'oggetto [**IContextNode**](icontextnode.md) corrisponde ai criteri e **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b2e95-115">Implement **IMatchesCriteriaCallBack::EvaluateContextNode** to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="b2e95-116">Per alcuni criteri, potrebbe essere necessario fornire un mezzo per inizializzare o gestire lo stato dell'oggetto **IMatchesCriteriaCallBack** .</span><span class="sxs-lookup"><span data-stu-id="b2e95-116">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e95-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2e95-117">Requirements</span></span>



| <span data-ttu-id="b2e95-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e95-118">Requirement</span></span> | <span data-ttu-id="b2e95-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b2e95-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e95-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2e95-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e95-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b2e95-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b2e95-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2e95-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e95-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b2e95-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b2e95-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2e95-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2e95-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b2e95-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b2e95-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b2e95-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2e95-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2e95-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b2e95-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2e95-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e95-129">**IMatchesCriteriaCallBack**</span><span class="sxs-lookup"><span data-stu-id="b2e95-129">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md)
</dt> <dt>

[<span data-ttu-id="b2e95-130">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="b2e95-130">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="b2e95-131">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="b2e95-131">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="b2e95-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b2e95-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




