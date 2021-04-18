---
description: Recupera il nome del riconoscimento.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'Metodo IInkAnalysisRecognizer:: GetName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fe263878d1fd5e914cf033111997d297a20c54f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307407"
---
# <a name="iinkanalysisrecognizergetname-method"></a><span data-ttu-id="306cb-103">Metodo IInkAnalysisRecognizer:: GetName</span><span class="sxs-lookup"><span data-stu-id="306cb-103">IInkAnalysisRecognizer::GetName method</span></span>

<span data-ttu-id="306cb-104">Recupera il nome del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="306cb-104">Retrieves the name of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="306cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="306cb-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="306cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="306cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="306cb-107">*pbstrName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="306cb-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="306cb-108">Nome del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="306cb-108">The name of the recognizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="306cb-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="306cb-109">Return value</span></span>

<span data-ttu-id="306cb-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="306cb-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="306cb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="306cb-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="306cb-112">Per evitare una perdita di memoria, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) su \* *pbstrName* quando non è più necessario usare la stringa.</span><span class="sxs-lookup"><span data-stu-id="306cb-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrName* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="306cb-113">Il nome è localizzato per la lingua indipendente dall'area supportata dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="306cb-113">The name is localized for the region-neutral language that the recognizer supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="306cb-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="306cb-114">Requirements</span></span>



| <span data-ttu-id="306cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="306cb-115">Requirement</span></span> | <span data-ttu-id="306cb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="306cb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="306cb-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="306cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="306cb-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="306cb-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="306cb-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="306cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="306cb-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="306cb-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="306cb-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="306cb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="306cb-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="306cb-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="306cb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="306cb-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="306cb-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="306cb-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="306cb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="306cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="306cb-126">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="306cb-126">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="306cb-127">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="306cb-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

