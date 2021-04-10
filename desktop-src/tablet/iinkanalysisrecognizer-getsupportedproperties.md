---
description: Recupera gli identificatori univoci globali (GUID) per le proprietà che questo IInkAnalysisRecognizer può generare per i risultati dell'analisi.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'Metodo IInkAnalysisRecognizer:: GetSupportedProperties (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966724"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a><span data-ttu-id="d44ff-103">Metodo IInkAnalysisRecognizer:: GetSupportedProperties</span><span class="sxs-lookup"><span data-stu-id="d44ff-103">IInkAnalysisRecognizer::GetSupportedProperties method</span></span>

<span data-ttu-id="d44ff-104">Recupera gli identificatori univoci globali (GUID) per le proprietà che questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) può generare per i risultati dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="d44ff-104">Retrieves the globally unique identifiers (GUIDs) for the properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

## <a name="syntax"></a><span data-ttu-id="d44ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d44ff-105">Syntax</span></span>


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="d44ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d44ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d44ff-107">*pulPropertiesCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d44ff-107">*pulPropertiesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d44ff-108">Numero di GUID in *ppProperties*.</span><span class="sxs-lookup"><span data-stu-id="d44ff-108">The number of GUIDs in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="d44ff-109">*ppProperties* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d44ff-109">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d44ff-110">Puntatore ai GUID delle proprietà che questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) può generare per i risultati dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="d44ff-110">A pointer to the GUIDs of properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d44ff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d44ff-111">Return value</span></span>

<span data-ttu-id="d44ff-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d44ff-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d44ff-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d44ff-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d44ff-114">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppProperties* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="d44ff-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppProperties* when you no longer need the information.</span></span>

 

<span data-ttu-id="d44ff-115">Un riconoscitore può supportare le metriche delle righe, i numeri di riga, i livelli di confidenza e così via.</span><span class="sxs-lookup"><span data-stu-id="d44ff-115">A recognizer can support line metrics, line numbers, confidence levels, and so on.</span></span> <span data-ttu-id="d44ff-116">Per un elenco completo delle proprietà che un riconoscimento può supportare, vedere [costanti RecognitionProperty](recognitionproperty-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d44ff-116">For a complete list of the properties that a recognizer can support, see [RecognitionProperty Constants](recognitionproperty-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d44ff-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d44ff-117">Requirements</span></span>



| <span data-ttu-id="d44ff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d44ff-118">Requirement</span></span> | <span data-ttu-id="d44ff-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d44ff-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d44ff-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d44ff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d44ff-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d44ff-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d44ff-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d44ff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d44ff-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d44ff-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d44ff-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d44ff-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d44ff-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d44ff-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d44ff-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d44ff-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d44ff-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d44ff-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d44ff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d44ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d44ff-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="d44ff-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="d44ff-130">Costanti RecognitionProperty</span><span class="sxs-lookup"><span data-stu-id="d44ff-130">RecognitionProperty Constants</span></span>](recognitionproperty-constants.md)
</dt> <dt>

[<span data-ttu-id="d44ff-131">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="d44ff-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

