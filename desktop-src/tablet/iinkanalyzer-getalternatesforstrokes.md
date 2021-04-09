---
description: Recupera le alternative di analisi per i tratti con gli identificatori di tratto specificati.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'Metodo IInkAnalyzer:: GetAlternatesForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129458"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a><span data-ttu-id="10e9d-103">Metodo IInkAnalyzer:: GetAlternatesForStrokes</span><span class="sxs-lookup"><span data-stu-id="10e9d-103">IInkAnalyzer::GetAlternatesForStrokes method</span></span>

<span data-ttu-id="10e9d-104">Recupera le alternative di analisi per i tratti con gli identificatori di tratto specificati.</span><span class="sxs-lookup"><span data-stu-id="10e9d-104">Retrieves analysis alternates for the strokes with the specified stroke identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="10e9d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10e9d-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="10e9d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="10e9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e9d-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10e9d-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10e9d-108">Il numero di identificatori di tratto in *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="10e9d-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="10e9d-109">*plStrokes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10e9d-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10e9d-110">Matrice di identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="10e9d-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="10e9d-111">*ulMaximumAlternates* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10e9d-111">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10e9d-112">Numero massimo di alternative di analisi restituite.</span><span class="sxs-lookup"><span data-stu-id="10e9d-112">The maximum number of analysis alternatives returned.</span></span>

</dd> <dt>

<span data-ttu-id="10e9d-113">*ppAlternates* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="10e9d-113">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10e9d-114">Oggetto [**IAnalysisAlternates**](ianalysisalternates.md) che contiene le alternative di analisi.</span><span class="sxs-lookup"><span data-stu-id="10e9d-114">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e9d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10e9d-115">Return value</span></span>

<span data-ttu-id="10e9d-116">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="10e9d-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10e9d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="10e9d-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="10e9d-118">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppAlternates* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="10e9d-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="10e9d-119">Il [**IAnalysisAlternate**](ianalysisalternate.md) superiore viene restituito come prima alternativa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="10e9d-119">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="10e9d-120">Non è necessario che i tratti specificati rappresentino aree adiacenti del documento.</span><span class="sxs-lookup"><span data-stu-id="10e9d-120">The specified strokes do not have to represent adjacent areas of the document.</span></span>

## <a name="requirements"></a><span data-ttu-id="10e9d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10e9d-121">Requirements</span></span>



| <span data-ttu-id="10e9d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="10e9d-122">Requirement</span></span> | <span data-ttu-id="10e9d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="10e9d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10e9d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10e9d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="10e9d-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="10e9d-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="10e9d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10e9d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="10e9d-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="10e9d-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="10e9d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10e9d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e9d-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="10e9d-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="10e9d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="10e9d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10e9d-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10e9d-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="10e9d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10e9d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e9d-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="10e9d-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="10e9d-134">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="10e9d-134">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="10e9d-135">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="10e9d-135">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="10e9d-136">**Metodo IInkAnalyzer:: getalters**</span><span class="sxs-lookup"><span data-stu-id="10e9d-136">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="10e9d-137">**Metodo IInkAnalyzer:: GetAlternatesForContextNodes**</span><span class="sxs-lookup"><span data-stu-id="10e9d-137">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="10e9d-138">**Metodo IInkAnalyzer:: ModifyTopAlternate**</span><span class="sxs-lookup"><span data-stu-id="10e9d-138">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="10e9d-139">**Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation**</span><span class="sxs-lookup"><span data-stu-id="10e9d-139">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="10e9d-140">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="10e9d-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

