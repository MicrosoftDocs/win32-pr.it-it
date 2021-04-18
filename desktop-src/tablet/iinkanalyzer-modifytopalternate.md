---
description: Modifica l'alternanza principale corrente nell'alternativa specificata e cancella il tipo di conferma per tutti gli oggetti IContextNode associati all'alternativa.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'Metodo IInkAnalyzer:: ModifyTopAlternate (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307379"
---
# <a name="iinkanalyzermodifytopalternate-method"></a><span data-ttu-id="25dca-103">Metodo IInkAnalyzer:: ModifyTopAlternate</span><span class="sxs-lookup"><span data-stu-id="25dca-103">IInkAnalyzer::ModifyTopAlternate method</span></span>

<span data-ttu-id="25dca-104">Modifica l'alternanza principale corrente nell'alternativa specificata e cancella il tipo di conferma per tutti gli oggetti [**IContextNode**](icontextnode.md) associati all'alternativa.</span><span class="sxs-lookup"><span data-stu-id="25dca-104">Changes the current top alternate to the specified alternate and clears the confirmation type for all [**IContextNode**](icontextnode.md) objects associated with the alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="25dca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25dca-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="25dca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25dca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25dca-107">*pAlternate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25dca-107">*pAlternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25dca-108">Oggetto [**IAnalysisAlternate**](ianalysisalternate.md) contenente la nuova alternativa principale.</span><span class="sxs-lookup"><span data-stu-id="25dca-108">The [**IAnalysisAlternate**](ianalysisalternate.md) object containing the new top alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25dca-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25dca-109">Return value</span></span>

<span data-ttu-id="25dca-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="25dca-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25dca-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="25dca-111">Remarks</span></span>

<span data-ttu-id="25dca-112">Per ottenere le alternative di analisi, usare il metodo [**IInkAnalyzer:: Getalternas**](iinkanalyzer-getalternates.md), il metodo [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o il metodo [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="25dca-112">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="25dca-113">Per ottenere gli oggetti [**IContextNode**](icontextnode.md) associati a un'alternativa di analisi, usare il [**Metodo IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="25dca-113">To get the [**IContextNode**](icontextnode.md) objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="25dca-114">Per modificare il tipo di conferma per un nodo di contesto, utilizzare [**IContextNode:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="25dca-114">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25dca-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25dca-115">Requirements</span></span>



| <span data-ttu-id="25dca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25dca-116">Requirement</span></span> | <span data-ttu-id="25dca-117">Valore</span><span class="sxs-lookup"><span data-stu-id="25dca-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25dca-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25dca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25dca-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="25dca-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="25dca-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25dca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25dca-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="25dca-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="25dca-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25dca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25dca-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="25dca-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="25dca-124">DLL</span><span class="sxs-lookup"><span data-stu-id="25dca-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25dca-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25dca-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="25dca-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25dca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25dca-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="25dca-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="25dca-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="25dca-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="25dca-129">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="25dca-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="25dca-130">**ConfirmationType**</span><span class="sxs-lookup"><span data-stu-id="25dca-130">**ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="25dca-131">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="25dca-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




