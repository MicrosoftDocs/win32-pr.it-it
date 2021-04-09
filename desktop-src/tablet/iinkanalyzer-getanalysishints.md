---
description: Ottiene tutti gli oggetti IContextNode hint di analisi collegati a IInkAnalyzer.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'Metodo IInkAnalyzer:: GetAnalysisHints (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129455"
---
# <a name="iinkanalyzergetanalysishints-method"></a><span data-ttu-id="2213d-103">Metodo IInkAnalyzer:: GetAnalysisHints</span><span class="sxs-lookup"><span data-stu-id="2213d-103">IInkAnalyzer::GetAnalysisHints method</span></span>

<span data-ttu-id="2213d-104">Ottiene tutti gli oggetti [**IContextNode**](icontextnode.md) hint di analisi collegati a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="2213d-104">Gets all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2213d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2213d-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="2213d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2213d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2213d-107">*ppAnalysisHints* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2213d-107">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2213d-108">Puntatore a tutti gli oggetti [**IContextNode**](icontextnode.md) hint di analisi in [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="2213d-108">A pointer to all the analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2213d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2213d-109">Return value</span></span>

<span data-ttu-id="2213d-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2213d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2213d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2213d-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="2213d-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAnalysisHints* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2213d-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="2213d-113">Questo metodo restituisce una raccolta vuota se nessun nodo hint di analisi è associato a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="2213d-113">This method returns an empty collection if no analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="2213d-114">Un nodo di hint di analisi è un [**IContextNode**](icontextnode.md) con un tipo di nodo di contesto di AnalysisHint (vedere tipi di [nodo](context-node-types.md) [**IContextNode:: GetType**](icontextnode-gettype.md) e context).</span><span class="sxs-lookup"><span data-stu-id="2213d-114">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="2213d-115">Per aggiungere informazioni di contesto all'hint, utilizzare [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con il parametro *pPropertyDataId* impostato su uno degli identificatori univoci globali (Guid) nelle costanti delle [proprietà dell'hint di analisi](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="2213d-115">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="2213d-116">Per individuare i valori delle proprietà impostati in un nodo di contesto, utilizzare [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="2213d-116">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="2213d-117">Per trovare il valore di una proprietà, usare [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="2213d-117">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2213d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2213d-118">Requirements</span></span>



| <span data-ttu-id="2213d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2213d-119">Requirement</span></span> | <span data-ttu-id="2213d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2213d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2213d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2213d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2213d-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2213d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2213d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2213d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2213d-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2213d-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2213d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2213d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2213d-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2213d-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2213d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2213d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2213d-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2213d-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2213d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2213d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2213d-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="2213d-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2213d-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="2213d-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2213d-132">**Metodo IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="2213d-132">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="2213d-133">**IInkAnalyzer::D Metodo eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="2213d-133">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="2213d-134">**Metodo IInkAnalyzer:: GetAnalysisHintsByName**</span><span class="sxs-lookup"><span data-stu-id="2213d-134">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="2213d-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="2213d-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

