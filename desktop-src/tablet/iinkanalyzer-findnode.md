---
description: Recupera l'oggetto IContextNode per un identificatore univoco globale (GUID) specificato.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'Metodo IInkAnalyzer:: FindNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049517"
---
# <a name="iinkanalyzerfindnode-method"></a><span data-ttu-id="be993-103">Metodo IInkAnalyzer:: FindNode</span><span class="sxs-lookup"><span data-stu-id="be993-103">IInkAnalyzer::FindNode method</span></span>

<span data-ttu-id="be993-104">Recupera l'oggetto [**IContextNode**](icontextnode.md) per un identificatore univoco globale (Guid) specificato.</span><span class="sxs-lookup"><span data-stu-id="be993-104">Retrieves the [**IContextNode**](icontextnode.md) object for a specified globally unique identifier (GUID).</span></span>

## <a name="syntax"></a><span data-ttu-id="be993-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be993-105">Syntax</span></span>


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a><span data-ttu-id="be993-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be993-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be993-107">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be993-107">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be993-108">Identificatore per l'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="be993-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="be993-109">*ppContextNodeFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be993-109">*ppContextNodeFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be993-110">Puntatore all'oggetto [**IContextNode**](icontextnode.md) con l'identificatore *PID* .</span><span class="sxs-lookup"><span data-stu-id="be993-110">A pointer to the [**IContextNode**](icontextnode.md) object with the *pId* identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be993-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be993-111">Return value</span></span>

<span data-ttu-id="be993-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="be993-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be993-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="be993-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="be993-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="be993-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="be993-115">Se tale oggetto [**IContextNode**](icontextnode.md) non esiste come discendente del nodo radice [**IInkAnalyzer**](iinkanalyzer.md) , viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="be993-115">If no such [**IContextNode**](icontextnode.md) object exists as a descendant of the [**IInkAnalyzer**](iinkanalyzer.md) root node, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="be993-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be993-116">Requirements</span></span>



| <span data-ttu-id="be993-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="be993-117">Requirement</span></span> | <span data-ttu-id="be993-118">Valore</span><span class="sxs-lookup"><span data-stu-id="be993-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be993-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be993-119">Minimum supported client</span></span><br/> | <span data-ttu-id="be993-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="be993-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be993-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be993-121">Minimum supported server</span></span><br/> | <span data-ttu-id="be993-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="be993-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be993-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be993-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="be993-124"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be993-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="be993-125">DLL</span><span class="sxs-lookup"><span data-stu-id="be993-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be993-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be993-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="be993-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be993-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be993-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="be993-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="be993-129">**Metodo IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="be993-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="be993-130">**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="be993-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="be993-131">**Metodo IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="be993-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="be993-132">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="be993-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="be993-133">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="be993-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="be993-134">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="be993-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="be993-135">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="be993-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="be993-136">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="be993-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="be993-137">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="be993-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

