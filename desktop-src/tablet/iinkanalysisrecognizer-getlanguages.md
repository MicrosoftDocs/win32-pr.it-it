---
description: Recupera gli identificatori per le impostazioni locali supportate da questo IInkAnalysisRecognizer.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'Metodo IInkAnalysisRecognizer:: GetLanguages (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879353"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a><span data-ttu-id="6fc9a-103">Metodo IInkAnalysisRecognizer:: GetLanguages</span><span class="sxs-lookup"><span data-stu-id="6fc9a-103">IInkAnalysisRecognizer::GetLanguages method</span></span>

<span data-ttu-id="6fc9a-104">Recupera gli identificatori per le impostazioni locali supportate da questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc9a-104">Retrieves the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc9a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fc9a-105">Syntax</span></span>


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a><span data-ttu-id="6fc9a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fc9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc9a-107">*pulLanguagesCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6fc9a-107">*pulLanguagesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc9a-108">Il numero di identificatori in *ppulLanguages*.</span><span class="sxs-lookup"><span data-stu-id="6fc9a-108">The number of identifiers in *ppulLanguages*.</span></span>

</dd> <dt>

<span data-ttu-id="6fc9a-109">*ppulLanguages* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6fc9a-109">*ppulLanguages* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc9a-110">Puntatore agli identificatori per le impostazioni locali supportate da questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc9a-110">A pointer to the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc9a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fc9a-111">Return value</span></span>

<span data-ttu-id="6fc9a-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6fc9a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6fc9a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fc9a-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6fc9a-114">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppulLanguages* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="6fc9a-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppulLanguages* when you no longer need the information.</span></span>

 

<span data-ttu-id="6fc9a-115">Questo metodo restituisce una matrice vuota per i riconoscitori di oggetto e di movimento.</span><span class="sxs-lookup"><span data-stu-id="6fc9a-115">This method returns an empty array for object and gesture recognizers.</span></span>

<span data-ttu-id="6fc9a-116">Per altre informazioni sugli identificatori di lingua, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="6fc9a-116">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc9a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fc9a-117">Requirements</span></span>



| <span data-ttu-id="6fc9a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc9a-118">Requirement</span></span> | <span data-ttu-id="6fc9a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6fc9a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc9a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fc9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc9a-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6fc9a-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6fc9a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fc9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc9a-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6fc9a-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6fc9a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fc9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc9a-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9a-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6fc9a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6fc9a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fc9a-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9a-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6fc9a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fc9a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc9a-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="6fc9a-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="6fc9a-130">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="6fc9a-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

