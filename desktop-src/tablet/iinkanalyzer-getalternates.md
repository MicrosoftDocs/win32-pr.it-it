---
description: Recupera 10 alternative di analisi per tutti gli input penna associati a IInkAnalyzer.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'Metodo IInkAnalyzer:: getalternas (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307388"
---
# <a name="iinkanalyzergetalternates-method"></a><span data-ttu-id="be7f9-103">Metodo IInkAnalyzer:: getalters</span><span class="sxs-lookup"><span data-stu-id="be7f9-103">IInkAnalyzer::GetAlternates method</span></span>

<span data-ttu-id="be7f9-104">Recupera 10 alternative di analisi per tutti gli input penna associati a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="be7f9-104">Retrieves 10 analysis alternates for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="be7f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be7f9-105">Syntax</span></span>


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="be7f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be7f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7f9-107">*ppAlternates* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be7f9-107">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be7f9-108">Puntatore ai primi 10 oggetti [**IAnalysisAlternate**](ianalysisalternate.md) per tutto l'input penna associato a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="be7f9-108">A pointer to the top 10 [**IAnalysisAlternate**](ianalysisalternate.md) objects for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7f9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be7f9-109">Return value</span></span>

<span data-ttu-id="be7f9-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="be7f9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be7f9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="be7f9-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="be7f9-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAlternates* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="be7f9-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="be7f9-113">L'alternativa superiore viene restituita come prima alternativa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="be7f9-113">The top alternate is returned as the first alternate of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7f9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be7f9-114">Requirements</span></span>



| <span data-ttu-id="be7f9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7f9-115">Requirement</span></span> | <span data-ttu-id="be7f9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="be7f9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7f9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be7f9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="be7f9-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="be7f9-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be7f9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be7f9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="be7f9-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="be7f9-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be7f9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be7f9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="be7f9-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be7f9-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="be7f9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="be7f9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be7f9-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be7f9-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="be7f9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be7f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7f9-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="be7f9-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="be7f9-127">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="be7f9-127">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="be7f9-128">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="be7f9-128">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="be7f9-129">**Metodo IInkAnalyzer:: GetAlternatesForContextNodes**</span><span class="sxs-lookup"><span data-stu-id="be7f9-129">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="be7f9-130">**Metodo IInkAnalyzer:: GetAlternatesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="be7f9-130">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="be7f9-131">**Metodo IInkAnalyzer:: ModifyTopAlternate**</span><span class="sxs-lookup"><span data-stu-id="be7f9-131">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="be7f9-132">**Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation**</span><span class="sxs-lookup"><span data-stu-id="be7f9-132">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="be7f9-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="be7f9-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

