---
description: Recupera un valore che indica se IAnalysisRegion rappresenta un'area vuota.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'Metodo IAnalysisRegion:: IsEmpty (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307462"
---
# <a name="ianalysisregionisempty-method"></a><span data-ttu-id="e1138-103">Metodo IAnalysisRegion:: IsEmpty</span><span class="sxs-lookup"><span data-stu-id="e1138-103">IAnalysisRegion::IsEmpty method</span></span>

<span data-ttu-id="e1138-104">Recupera un valore che indica se [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area vuota.</span><span class="sxs-lookup"><span data-stu-id="e1138-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an empty region.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1138-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1138-105">Syntax</span></span>


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a><span data-ttu-id="e1138-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1138-107">*pfIsEmpty* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e1138-107">*pfIsEmpty* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1138-108">**Variante \_ TRUE** se l'area rappresentata è vuota. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e1138-108">**VARIANT\_TRUE** if the represented region is empty; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1138-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1138-109">Return value</span></span>

<span data-ttu-id="e1138-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e1138-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1138-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1138-111">Requirements</span></span>



| <span data-ttu-id="e1138-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1138-112">Requirement</span></span> | <span data-ttu-id="e1138-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e1138-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1138-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1138-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e1138-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e1138-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e1138-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1138-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e1138-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e1138-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e1138-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1138-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1138-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e1138-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e1138-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e1138-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1138-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1138-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e1138-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1138-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1138-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="e1138-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="e1138-124">**Metodo IAnalysisRegion:: infinite**</span><span class="sxs-lookup"><span data-stu-id="e1138-124">**IAnalysisRegion::IsInfinite Method**</span></span>](ianalysisregion-isinfinite.md)
</dt> <dt>

[<span data-ttu-id="e1138-125">**Metodo IAnalysisRegion:: MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="e1138-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="e1138-126">**Metodo IAnalysisRegion:: MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="e1138-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="e1138-127">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="e1138-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




