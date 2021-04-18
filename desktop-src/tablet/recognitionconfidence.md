---
description: Indica il livello di confidenza del IInkAnalyzer nell'accuratezza del risultato del riconoscimento.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Enumerazione RecognitionConfidence (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318687"
---
# <a name="recognitionconfidence-enumeration"></a><span data-ttu-id="464da-103">Enumerazione RecognitionConfidence</span><span class="sxs-lookup"><span data-stu-id="464da-103">RecognitionConfidence enumeration</span></span>

<span data-ttu-id="464da-104">Indica il livello di confidenza del [**IInkAnalyzer**](iinkanalyzer.md) nell'accuratezza del risultato del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="464da-104">Indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the recognition result.</span></span>

## <a name="syntax"></a><span data-ttu-id="464da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="464da-105">Syntax</span></span>


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a><span data-ttu-id="464da-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="464da-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="464da-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ forte**</span><span class="sxs-lookup"><span data-stu-id="464da-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence\_Strong**</span></span>
</dt> <dd>

<span data-ttu-id="464da-108">Confidenza assoluta nel risultato o in alternativa.</span><span class="sxs-lookup"><span data-stu-id="464da-108">Strong confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="464da-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ intermedio**</span><span class="sxs-lookup"><span data-stu-id="464da-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence\_Intermediate**</span></span>
</dt> <dd>

<span data-ttu-id="464da-110">Confidenza intermedia nel risultato o in alternativa.</span><span class="sxs-lookup"><span data-stu-id="464da-110">Intermediate confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="464da-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ poor**</span><span class="sxs-lookup"><span data-stu-id="464da-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence\_Poor**</span></span>
</dt> <dd>

<span data-ttu-id="464da-112">Scarsa confidenza nel risultato o in alternativa.</span><span class="sxs-lookup"><span data-stu-id="464da-112">Poor confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="464da-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="464da-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="464da-114">Il [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) che ha generato il testo riconosciuto non supporta i livelli di confidenza.</span><span class="sxs-lookup"><span data-stu-id="464da-114">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that generated the recognized text does not support confidence levels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="464da-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="464da-115">Remarks</span></span>

<span data-ttu-id="464da-116">[**IInkAnalyzer**](iinkanalyzer.md) utilizza uno o più oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) per convertire la grafia in testo.</span><span class="sxs-lookup"><span data-stu-id="464da-116">The [**IInkAnalyzer**](iinkanalyzer.md) uses one or more [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects to convert handwriting to text.</span></span>

## <a name="requirements"></a><span data-ttu-id="464da-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="464da-117">Requirements</span></span>



| <span data-ttu-id="464da-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="464da-118">Requirement</span></span> | <span data-ttu-id="464da-119">Valore</span><span class="sxs-lookup"><span data-stu-id="464da-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="464da-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="464da-120">Minimum supported client</span></span><br/> | <span data-ttu-id="464da-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="464da-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="464da-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="464da-122">Minimum supported server</span></span><br/> | <span data-ttu-id="464da-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="464da-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="464da-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="464da-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="464da-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="464da-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="464da-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="464da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464da-127">**Metodo IAnalysisAlternate:: GetRecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="464da-127">**IAnalysisAlternate::GetRecognitionConfidence Method**</span></span>](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="464da-128">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="464da-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="464da-129">Proprietà del nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="464da-129">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="464da-130">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="464da-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




