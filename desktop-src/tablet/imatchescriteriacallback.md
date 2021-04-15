---
description: Espone un metodo per valutare se un oggetto IContextNode soddisfa o meno un criterio specificato.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interfaccia IMatchesCriteriaCallBack (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525320"
---
# <a name="imatchescriteriacallback-interface"></a><span data-ttu-id="913ee-103">Interfaccia IMatchesCriteriaCallBack</span><span class="sxs-lookup"><span data-stu-id="913ee-103">IMatchesCriteriaCallBack interface</span></span>

<span data-ttu-id="913ee-104">Espone un metodo per valutare se un oggetto [**IContextNode**](icontextnode.md) soddisfa o meno un criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="913ee-104">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span>

## <a name="members"></a><span data-ttu-id="913ee-105">Membri</span><span class="sxs-lookup"><span data-stu-id="913ee-105">Members</span></span>

<span data-ttu-id="913ee-106">L'interfaccia **IMatchesCriteriaCallBack** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="913ee-106">The **IMatchesCriteriaCallBack** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="913ee-107">**IMatchesCriteriaCallBack** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="913ee-107">**IMatchesCriteriaCallBack** also has these types of members:</span></span>

-   [<span data-ttu-id="913ee-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="913ee-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="913ee-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="913ee-109">Methods</span></span>

<span data-ttu-id="913ee-110">L'interfaccia **IMatchesCriteriaCallBack** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="913ee-110">The **IMatchesCriteriaCallBack** interface has these methods.</span></span>



| <span data-ttu-id="913ee-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="913ee-111">Method</span></span>                                                                      | <span data-ttu-id="913ee-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="913ee-112">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="913ee-113">**EvaluateContextNode**</span><span class="sxs-lookup"><span data-stu-id="913ee-113">**EvaluateContextNode**</span></span>](imatchescriteriacallback-evaluatecontextnode.md) | <span data-ttu-id="913ee-114">Quando sottoposto a override in una classe derivata, valuta se un oggetto [**IContextNode**](icontextnode.md) specificato soddisfa i criteri.</span><span class="sxs-lookup"><span data-stu-id="913ee-114">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="913ee-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="913ee-115">Remarks</span></span>

<span data-ttu-id="913ee-116">Per usare il metodo [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), creare una classe che implementi **IMatchesCriteriaCallBack**.</span><span class="sxs-lookup"><span data-stu-id="913ee-116">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements **IMatchesCriteriaCallBack**.</span></span> <span data-ttu-id="913ee-117">Implementare [**IMatchesCriteriaCallBack:: EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) per restituire la **variante \_ true** se l'oggetto [**IContextNode**](icontextnode.md) corrisponde ai criteri e **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="913ee-117">Implement [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="913ee-118">Per alcuni criteri, potrebbe essere necessario fornire un mezzo per inizializzare o gestire lo stato dell'oggetto **IMatchesCriteriaCallBack** .</span><span class="sxs-lookup"><span data-stu-id="913ee-118">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="913ee-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="913ee-119">Requirements</span></span>



| <span data-ttu-id="913ee-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="913ee-120">Requirement</span></span> | <span data-ttu-id="913ee-121">Valore</span><span class="sxs-lookup"><span data-stu-id="913ee-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="913ee-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="913ee-122">Minimum supported client</span></span><br/> | <span data-ttu-id="913ee-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="913ee-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="913ee-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="913ee-124">Minimum supported server</span></span><br/> | <span data-ttu-id="913ee-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="913ee-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="913ee-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="913ee-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="913ee-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="913ee-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="913ee-128">DLL</span><span class="sxs-lookup"><span data-stu-id="913ee-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="913ee-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="913ee-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="913ee-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="913ee-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913ee-131">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="913ee-131">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="913ee-132">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="913ee-132">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="913ee-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="913ee-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

