---
description: Recupera una raccolta ordinata di oggetti IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879330"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a><span data-ttu-id="c5ff8-103">Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority</span><span class="sxs-lookup"><span data-stu-id="c5ff8-103">IInkAnalyzer::GetInkAnalysisRecognizersByPriority method</span></span>

<span data-ttu-id="c5ff8-104">Recupera una raccolta ordinata di oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ff8-104">Retrieves an ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ff8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5ff8-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a><span data-ttu-id="c5ff8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5ff8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ff8-107">*ppInkAnalysisRecognizers* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c5ff8-107">*ppInkAnalysisRecognizers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff8-108">Raccolta ordinata di oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ff8-108">An ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ff8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5ff8-109">Return value</span></span>

<span data-ttu-id="c5ff8-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c5ff8-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ff8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5ff8-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c5ff8-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppInkAnalysisRecognizers* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c5ff8-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppInkAnalysisRecognizers* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="c5ff8-113">L'ordine dei riconoscitori in questa raccolta indica l'ordine in cui il [**IInkAnalyzer**](iinkanalyzer.md) valuta i riconoscitori disponibili.</span><span class="sxs-lookup"><span data-stu-id="c5ff8-113">The order of the recognizers in this collection indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available recognizers.</span></span> <span data-ttu-id="c5ff8-114">**IInkAnalyzer** usa il linguaggio dei tratti come criterio principale per l'applicazione di un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="c5ff8-114">The **IInkAnalyzer** uses the language of the strokes as its primary criterion for applying an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="c5ff8-115">Come criterio secondario, **IInkAnalyzer** Confronta le informazioni sui suggerimenti di analisi con le funzionalità supportate di un oggetto **IInkAnalysisRecognizer** (vedere [**IInkAnalysisRecognizer:: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span><span class="sxs-lookup"><span data-stu-id="c5ff8-115">As a secondary criterion, the **IInkAnalyzer** compares analysis hint information against an **IInkAnalysisRecognizer** object's supported capabilities (see [**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span></span> <span data-ttu-id="c5ff8-116">Per ulteriori informazioni sugli hint di analisi, vedere il [**Metodo IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md).</span><span class="sxs-lookup"><span data-stu-id="c5ff8-116">For more information about analysis hints, see [**IInkAnalyzer::CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).</span></span>

<span data-ttu-id="c5ff8-117">Se più di un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supporta un identificatore di lingua, [**IInkAnalyzer**](iinkanalyzer.md) usa un algoritmo "First-Fit" per selezionare il primo **IInkAnalysisRecognizer** per analizzare i tratti di tale lingua.</span><span class="sxs-lookup"><span data-stu-id="c5ff8-117">If more than one [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports a language identifier, the [**IInkAnalyzer**](iinkanalyzer.md) uses a "first-fit" algorithm to select the first **IInkAnalysisRecognizer** to analyze strokes of that language.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ff8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5ff8-118">Requirements</span></span>



| <span data-ttu-id="c5ff8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ff8-119">Requirement</span></span> | <span data-ttu-id="c5ff8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c5ff8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ff8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5ff8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ff8-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c5ff8-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c5ff8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5ff8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ff8-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c5ff8-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c5ff8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5ff8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ff8-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff8-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c5ff8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ff8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5ff8-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff8-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c5ff8-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5ff8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ff8-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c5ff8-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c5ff8-131">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="c5ff8-131">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="c5ff8-132">**Metodo IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="c5ff8-132">**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer Method**</span></span>](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="c5ff8-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c5ff8-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

