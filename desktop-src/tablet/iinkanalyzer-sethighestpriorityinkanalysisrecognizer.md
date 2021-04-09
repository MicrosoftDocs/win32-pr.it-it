---
description: Sposta il IInkAnalysisRecognizer specificato nella prima posizione dell'elenco di riconoscitori di input penna dell'oggetto IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'Metodo IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879326"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a><span data-ttu-id="ce6e9-103">Metodo IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer</span><span class="sxs-lookup"><span data-stu-id="ce6e9-103">IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer method</span></span>

<span data-ttu-id="ce6e9-104">Sposta il [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) specificato nella prima posizione dell'elenco di riconoscitori di input penna dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="ce6e9-104">Moves the specified [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to the first position in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce6e9-105">Syntax</span></span>


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="ce6e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce6e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce6e9-107">*pInkAnalysisRecognizer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce6e9-107">*pInkAnalysisRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce6e9-108">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) da inserire nella prima posizione.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-108">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to place in the first position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce6e9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce6e9-109">Return value</span></span>

<span data-ttu-id="ce6e9-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ce6e9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce6e9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce6e9-111">Remarks</span></span>

<span data-ttu-id="ce6e9-112">Per ottenere l'elenco dei riconoscitori di input penna in ordine di priorità, chiamare il [**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span><span class="sxs-lookup"><span data-stu-id="ce6e9-112">To get the list of ink recognizers in priority order, call [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span></span>

<span data-ttu-id="ce6e9-113">Questo metodo non influisce sull'ordine degli altri oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nell'elenco di riconoscitori di input penna dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="ce6e9-113">This method does not affect the order of the rest of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

<span data-ttu-id="ce6e9-114">L'ordine dei riconoscitori Ink restituiti dal [**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indica l'ordine in cui [**IInkAnalyzer**](iinkanalyzer.md) valuta gli oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponibili.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-114">The order of the ink recognizers returned by [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

<span data-ttu-id="ce6e9-115">L'utilizzo dei riconoscitori Ink viene valutato in base al relativo ordine nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-115">Use of the ink recognizers is evaluated based on their order in the list.</span></span>

<span data-ttu-id="ce6e9-116">Durante l'analisi dell'input penna, [**IInkAnalyzer**](iinkanalyzer.md) scorre i riconoscitori dell'input penna nell'elenco finché non trova un riconoscimento che supporta la lingua e altre proprietà dei tratti.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-116">During ink analysis, the [**IInkAnalyzer**](iinkanalyzer.md) iterates through the ink recognizers in its list until it finds a recognizer that supports the language and other properties of the strokes.</span></span> <span data-ttu-id="ce6e9-117">Questo riconoscimento viene utilizzato per il riconoscimento dell'input penna per tali tratti.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-117">This recognizer is used for ink recognition for those strokes.</span></span>

<span data-ttu-id="ce6e9-118">Se [**IInkAnalyzer**](iinkanalyzer.md) non trova un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) che supporta un set di tratti durante l'analisi, **IInkAnalyzer** genera un [**IAnalysisWarning**](ianalysiswarning.md) con un codice di avviso di **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (vedere [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span><span class="sxs-lookup"><span data-stu-id="ce6e9-118">If the [**IInkAnalyzer**](iinkanalyzer.md) does not find an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that supports a set of strokes during analysis, the **IInkAnalyzer** generates an [**IAnalysisWarning**](ianalysiswarning.md) with a warning code of **AnalysisWarningCode\_InkAnalysisRecognizerNotInstalled** (see [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6e9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce6e9-119">Requirements</span></span>



| <span data-ttu-id="ce6e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce6e9-120">Requirement</span></span> | <span data-ttu-id="ce6e9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ce6e9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6e9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce6e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6e9-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ce6e9-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ce6e9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce6e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6e9-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ce6e9-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ce6e9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce6e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6e9-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ce6e9-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ce6e9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ce6e9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce6e9-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce6e9-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ce6e9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce6e9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6e9-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ce6e9-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ce6e9-132">**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**</span><span class="sxs-lookup"><span data-stu-id="ce6e9-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="ce6e9-133">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="ce6e9-133">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="ce6e9-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="ce6e9-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="ce6e9-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ce6e9-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




