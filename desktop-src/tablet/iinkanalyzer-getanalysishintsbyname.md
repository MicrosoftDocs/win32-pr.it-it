---
description: Recupera tutti gli oggetti IContextNode hint di analisi collegati a IInkAnalyzer e con il nome specificato.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'Metodo IInkAnalyzer:: GetAnalysisHintsByName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226156"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a><span data-ttu-id="6aa3e-103">Metodo IInkAnalyzer:: GetAnalysisHintsByName</span><span class="sxs-lookup"><span data-stu-id="6aa3e-103">IInkAnalyzer::GetAnalysisHintsByName method</span></span>

<span data-ttu-id="6aa3e-104">Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) hint di analisi collegati a [**IInkAnalyzer**](iinkanalyzer.md) e con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-104">Retrieves all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md) and that have the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa3e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6aa3e-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="6aa3e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6aa3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa3e-107">*hintName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6aa3e-107">*hintName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa3e-108">Nome del suggerimento per il quale eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-108">The hint name for which to search.</span></span>

</dd> <dt>

<span data-ttu-id="6aa3e-109">*ppAnalysisHints* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6aa3e-109">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa3e-110">Hint di analisi [**IContextNode**](icontextnode.md) gli oggetti in [**IInkAnalyzer**](iinkanalyzer.md) con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-110">The analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) that have the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa3e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6aa3e-111">Return value</span></span>

<span data-ttu-id="6aa3e-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md) i valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aa3e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6aa3e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6aa3e-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAnalysisHints* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="6aa3e-115">Questo metodo restituisce una raccolta vuota se nessun nodo di hint di analisi di questo tipo è associato a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="6aa3e-115">This method returns an empty collection if no such analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="6aa3e-116">Un nodo di hint di analisi è un [**IContextNode**](icontextnode.md) con un tipo di nodo di contesto di AnalysisHint (vedere tipi di [nodo](context-node-types.md) [**IContextNode:: GetType**](icontextnode-gettype.md) e context).</span><span class="sxs-lookup"><span data-stu-id="6aa3e-116">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="6aa3e-117">Per aggiungere informazioni di contesto all'hint, utilizzare [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con il parametro *pPropertyDataId* impostato su uno degli identificatori univoci globali (Guid) nelle costanti delle [proprietà dell'hint di analisi](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa3e-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="6aa3e-118">Per individuare i valori delle proprietà impostati in un nodo di contesto, utilizzare [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="6aa3e-118">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="6aa3e-119">Per trovare il valore di una proprietà, usare [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="6aa3e-119">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa3e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aa3e-120">Requirements</span></span>



| <span data-ttu-id="6aa3e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aa3e-121">Requirement</span></span> | <span data-ttu-id="6aa3e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6aa3e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa3e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aa3e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa3e-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6aa3e-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6aa3e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aa3e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa3e-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6aa3e-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6aa3e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6aa3e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aa3e-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6aa3e-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6aa3e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6aa3e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aa3e-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aa3e-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6aa3e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6aa3e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa3e-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6aa3e-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6aa3e-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="6aa3e-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6aa3e-134">**Metodo IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="6aa3e-134">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="6aa3e-135">**IInkAnalyzer::D Metodo eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="6aa3e-135">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="6aa3e-136">**Metodo IInkAnalyzer:: GetAnalysisHints**</span><span class="sxs-lookup"><span data-stu-id="6aa3e-136">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="6aa3e-137">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="6aa3e-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

