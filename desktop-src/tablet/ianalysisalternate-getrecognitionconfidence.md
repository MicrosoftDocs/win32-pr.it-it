---
description: Ottiene un valore che indica il livello di attendibilità di IInkAnalyzer nell'accuratezza di IAnalysisAlternate.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'Metodo IAnalysisAlternate:: GetRecognitionConfidence (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751882"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a><span data-ttu-id="b014c-103">Metodo IAnalysisAlternate:: GetRecognitionConfidence</span><span class="sxs-lookup"><span data-stu-id="b014c-103">IAnalysisAlternate::GetRecognitionConfidence method</span></span>

<span data-ttu-id="b014c-104">Ottiene un valore che indica il livello di attendibilità di [**IInkAnalyzer**](iinkanalyzer.md) nell'accuratezza di [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="b014c-104">Gets a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b014c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b014c-105">Syntax</span></span>


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a><span data-ttu-id="b014c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b014c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b014c-107">*pConfidence* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b014c-107">*pConfidence* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b014c-108">Puntatore a un' [**Enumerazione InkRecognitionConfidence**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) che indica il livello di confidenza del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nell'accuratezza dell'alternativa del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b014c-108">A pointer to an [**InkRecognitionConfidence Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) that indicates the level of confidence that the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) has in the accuracy of the recognition alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b014c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b014c-109">Return value</span></span>

<span data-ttu-id="b014c-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b014c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b014c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b014c-111">Requirements</span></span>



| <span data-ttu-id="b014c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b014c-112">Requirement</span></span> | <span data-ttu-id="b014c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b014c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b014c-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b014c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b014c-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b014c-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b014c-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b014c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b014c-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b014c-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b014c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b014c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b014c-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b014c-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b014c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b014c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b014c-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b014c-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b014c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b014c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b014c-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="b014c-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="b014c-124">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b014c-124">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b014c-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="b014c-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b014c-126">**RecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="b014c-126">**RecognitionConfidence**</span></span>](recognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="b014c-127">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b014c-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




