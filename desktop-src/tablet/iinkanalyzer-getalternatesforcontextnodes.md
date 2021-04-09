---
description: Recupera le alternative di analisi per i nodi in una raccolta IContextNodes specificata.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'Metodo IInkAnalyzer:: GetAlternatesForContextNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129459"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a><span data-ttu-id="637d3-103">Metodo IInkAnalyzer:: GetAlternatesForContextNodes</span><span class="sxs-lookup"><span data-stu-id="637d3-103">IInkAnalyzer::GetAlternatesForContextNodes method</span></span>

<span data-ttu-id="637d3-104">Recupera le alternative di analisi per i nodi in una raccolta [**IContextNodes**](icontextnodes.md) specificata.</span><span class="sxs-lookup"><span data-stu-id="637d3-104">Retrieves analysis alternates for the nodes in a specified [**IContextNodes**](icontextnodes.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="637d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="637d3-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="637d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="637d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="637d3-107">*pContextNodes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="637d3-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="637d3-108">Raccolta [**IContextNodes**](icontextnodes.md) per la quale vengono restituite le alternative di analisi.</span><span class="sxs-lookup"><span data-stu-id="637d3-108">The [**IContextNodes**](icontextnodes.md) collection for which the analysis alternatives are returned.</span></span>

</dd> <dt>

<span data-ttu-id="637d3-109">*ulMaximumAlternates* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="637d3-109">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="637d3-110">Numero massimo di alternative da restituire.</span><span class="sxs-lookup"><span data-stu-id="637d3-110">The maximum number of alternatives to return.</span></span>

</dd> <dt>

<span data-ttu-id="637d3-111">*ppAlternates* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="637d3-111">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="637d3-112">Oggetto [**IAnalysisAlternates**](ianalysisalternates.md) che contiene le alternative di analisi.</span><span class="sxs-lookup"><span data-stu-id="637d3-112">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="637d3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="637d3-113">Return value</span></span>

<span data-ttu-id="637d3-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="637d3-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="637d3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="637d3-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="637d3-116">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAlternates* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="637d3-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="637d3-117">Il [**IAnalysisAlternate**](ianalysisalternate.md) superiore viene restituito come prima alternativa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="637d3-117">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="637d3-118">Gli oggetti [**IContextNode**](icontextnode.md) in *pContextNodes* non devono necessariamente rappresentare aree adiacenti del documento.</span><span class="sxs-lookup"><span data-stu-id="637d3-118">The [**IContextNode**](icontextnode.md) objects in *pContextNodes* do not have to represent adjacent areas of the document.</span></span>

<span data-ttu-id="637d3-119">Per ogni hint di analisi nei nodi, [**IInkAnalyzer**](iinkanalyzer.md) restituisce solo l'alternativa superiore.</span><span class="sxs-lookup"><span data-stu-id="637d3-119">For each analysis hint in nodes, the [**IInkAnalyzer**](iinkanalyzer.md) returns only the top alternate.</span></span>

## <a name="requirements"></a><span data-ttu-id="637d3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="637d3-120">Requirements</span></span>



| <span data-ttu-id="637d3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="637d3-121">Requirement</span></span> | <span data-ttu-id="637d3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="637d3-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="637d3-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="637d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="637d3-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="637d3-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="637d3-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="637d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="637d3-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="637d3-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="637d3-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="637d3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="637d3-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="637d3-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="637d3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="637d3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="637d3-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="637d3-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="637d3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="637d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637d3-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="637d3-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="637d3-133">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="637d3-133">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="637d3-134">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="637d3-134">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="637d3-135">**Metodo IInkAnalyzer:: getalters**</span><span class="sxs-lookup"><span data-stu-id="637d3-135">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="637d3-136">**Metodo IInkAnalyzer:: GetAlternatesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="637d3-136">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="637d3-137">**Metodo IInkAnalyzer:: ModifyTopAlternate**</span><span class="sxs-lookup"><span data-stu-id="637d3-137">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="637d3-138">**Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation**</span><span class="sxs-lookup"><span data-stu-id="637d3-138">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="637d3-139">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="637d3-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

