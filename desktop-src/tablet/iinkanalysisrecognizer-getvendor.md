---
description: Recupera il nome del fornitore del IInkAnalysisRecognizer.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'Metodo IInkAnalysisRecognizer:: getvendor (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129474"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a><span data-ttu-id="fedab-103">Metodo IInkAnalysisRecognizer:: getvendor</span><span class="sxs-lookup"><span data-stu-id="fedab-103">IInkAnalysisRecognizer::GetVendor method</span></span>

<span data-ttu-id="fedab-104">Recupera il nome del fornitore del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="fedab-104">Retrieves the vendor name of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fedab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fedab-105">Syntax</span></span>


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a><span data-ttu-id="fedab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fedab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fedab-107">*pbstrVendor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fedab-107">*pbstrVendor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fedab-108">Nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="fedab-108">The name of the vendor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fedab-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fedab-109">Return value</span></span>

<span data-ttu-id="fedab-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fedab-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fedab-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fedab-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fedab-112">Per evitare una perdita di memoria, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) su \* *pbstrVendor* quando non è più necessario usare la stringa.</span><span class="sxs-lookup"><span data-stu-id="fedab-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrVendor* when you no longer need to use the string.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fedab-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fedab-113">Requirements</span></span>



| <span data-ttu-id="fedab-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fedab-114">Requirement</span></span> | <span data-ttu-id="fedab-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fedab-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fedab-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fedab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fedab-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fedab-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fedab-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fedab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fedab-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fedab-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fedab-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fedab-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fedab-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fedab-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fedab-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fedab-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fedab-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fedab-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fedab-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fedab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fedab-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="fedab-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="fedab-126">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="fedab-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

