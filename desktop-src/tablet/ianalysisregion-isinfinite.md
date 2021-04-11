---
description: Recupera un valore che indica se IAnalysisRegion rappresenta un'area infinita.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'Metodo IAnalysisRegion:: infinite (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226175"
---
# <a name="ianalysisregionisinfinite-method"></a><span data-ttu-id="f2e4b-103">Metodo IAnalysisRegion:: infinite</span><span class="sxs-lookup"><span data-stu-id="f2e4b-103">IAnalysisRegion::IsInfinite method</span></span>

<span data-ttu-id="f2e4b-104">Recupera un valore che indica se [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area infinita.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite region.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e4b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2e4b-105">Syntax</span></span>


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a><span data-ttu-id="f2e4b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2e4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e4b-107">*pfIsInfinite* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2e4b-107">*pfIsInfinite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e4b-108">**Variante \_ TRUE** se l'area rappresentata è infinita; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-108">**VARIANT\_TRUE** if the represented region is infinite; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e4b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2e4b-109">Return value</span></span>

<span data-ttu-id="f2e4b-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f2e4b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e4b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2e4b-111">Requirements</span></span>



| <span data-ttu-id="f2e4b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e4b-112">Requirement</span></span> | <span data-ttu-id="f2e4b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f2e4b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e4b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2e4b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e4b-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f2e4b-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f2e4b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2e4b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e4b-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f2e4b-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f2e4b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2e4b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e4b-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e4b-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f2e4b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f2e4b-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2e4b-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2e4b-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f2e4b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2e4b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e4b-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="f2e4b-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-124">**Metodo IAnalysisRegion:: IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="f2e4b-124">**IAnalysisRegion::IsEmpty Method**</span></span>](ianalysisregion-isempty.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-125">**Metodo IAnalysisRegion:: MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="f2e4b-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-126">**Metodo IAnalysisRegion:: MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="f2e4b-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-127">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="f2e4b-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




