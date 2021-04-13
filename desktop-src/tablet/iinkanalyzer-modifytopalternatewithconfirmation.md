---
description: Modifica l'alternanza principale corrente nel IAnalysisAlternate specificato.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343691"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a><span data-ttu-id="8d6cd-103">Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation</span><span class="sxs-lookup"><span data-stu-id="8d6cd-103">IInkAnalyzer::ModifyTopAlternateWithConfirmation method</span></span>

<span data-ttu-id="8d6cd-104">Modifica l'alternanza principale corrente nel [**IAnalysisAlternate**](ianalysisalternate.md)specificato.</span><span class="sxs-lookup"><span data-stu-id="8d6cd-104">Changes the current top alternate to the specified [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d6cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d6cd-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a><span data-ttu-id="8d6cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d6cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d6cd-107">*alternativa* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d6cd-107">*alternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d6cd-108">Alternativa dell'analisi da impostare come nuova alternativa principale.</span><span class="sxs-lookup"><span data-stu-id="8d6cd-108">The analysis alternate to set as the new top alternate.</span></span>

</dd> <dt>

<span data-ttu-id="8d6cd-109">*fconfirmAutomatically* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d6cd-109">*fconfirmAutomatically* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d6cd-110">**Variante \_ TRUE** per impostare tutti i nodi di contesto foglia dell'input penna che corrispondono all'alternativa di analisi a un tipo di conferma **ConfirmationType \_ NodeTypeAndProperties** (vedere [**IContextNode::**](icontextnode-isconfirmed.md) istrued and [**ConfirmationType**](confirmationtype.md)); **Variante \_ FALSE** per impostare tutti i nodi di contesto foglia dell'input penna che corrispondono all'analisi alternativa a un tipo di conferma **ConfirmationType \_ None**.</span><span class="sxs-lookup"><span data-stu-id="8d6cd-110">**VARIANT\_TRUE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_NodeTypeAndProperties** (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md) and [**ConfirmationType**](confirmationtype.md)); **VARIANT\_FALSE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_None**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d6cd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d6cd-111">Return value</span></span>

<span data-ttu-id="8d6cd-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8d6cd-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d6cd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d6cd-113">Remarks</span></span>

<span data-ttu-id="8d6cd-114">Per ottenere le alternative di analisi, usare il metodo [**IInkAnalyzer:: Getalternas**](iinkanalyzer-getalternates.md), il metodo [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o il metodo [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="8d6cd-114">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="8d6cd-115">Per ottenere gli oggetti nodo di contesto associati a un'alternativa di analisi, usare il [**Metodo IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="8d6cd-115">To get the context node objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="8d6cd-116">Per modificare il tipo di conferma per un nodo di contesto, utilizzare [**IContextNode:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="8d6cd-116">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d6cd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d6cd-117">Requirements</span></span>



| <span data-ttu-id="8d6cd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d6cd-118">Requirement</span></span> | <span data-ttu-id="8d6cd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8d6cd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d6cd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d6cd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d6cd-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8d6cd-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8d6cd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d6cd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d6cd-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8d6cd-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8d6cd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d6cd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d6cd-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cd-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8d6cd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8d6cd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d6cd-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cd-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8d6cd-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d6cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d6cd-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8d6cd-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8d6cd-130">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="8d6cd-130">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="8d6cd-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="8d6cd-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8d6cd-132">**ConfirmationType di analisi dell'input penna**</span><span class="sxs-lookup"><span data-stu-id="8d6cd-132">**Ink Analysis ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="8d6cd-133">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8d6cd-133">Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




