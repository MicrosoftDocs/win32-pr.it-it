---
description: Recupera il numero di oggetti IInkAnalysisRecognizer in questa raccolta.
ms.assetid: dfb5c530-b481-4c60-b7fe-87fe162de270
title: 'Metodo IInkAnalysisRecognizers:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e65f8399c661d551e805abe5f1c5db33eb0b154a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526509"
---
# <a name="iinkanalysisrecognizersgetcount-method"></a><span data-ttu-id="24458-103">Metodo IInkAnalysisRecognizers:: GetCount</span><span class="sxs-lookup"><span data-stu-id="24458-103">IInkAnalysisRecognizers::GetCount method</span></span>

<span data-ttu-id="24458-104">Recupera il numero di oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="24458-104">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="24458-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24458-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="24458-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24458-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24458-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="24458-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="24458-108">Numero di oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="24458-108">The number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24458-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24458-109">Return value</span></span>

<span data-ttu-id="24458-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="24458-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24458-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24458-111">Requirements</span></span>



| <span data-ttu-id="24458-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="24458-112">Requirement</span></span> | <span data-ttu-id="24458-113">Valore</span><span class="sxs-lookup"><span data-stu-id="24458-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24458-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24458-114">Minimum supported client</span></span><br/> | <span data-ttu-id="24458-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="24458-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="24458-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24458-116">Minimum supported server</span></span><br/> | <span data-ttu-id="24458-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="24458-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="24458-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24458-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="24458-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="24458-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="24458-120">DLL</span><span class="sxs-lookup"><span data-stu-id="24458-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24458-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24458-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="24458-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24458-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24458-123">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="24458-123">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="24458-124">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="24458-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




