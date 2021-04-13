---
description: Determina se l'area del IAnalysisRegion interseca il rettangolo specificato.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'Metodo IAnalysisRegion:: IntersectsWith (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526551"
---
# <a name="ianalysisregionintersectswith-method"></a><span data-ttu-id="23f57-103">Metodo IAnalysisRegion:: IntersectsWith</span><span class="sxs-lookup"><span data-stu-id="23f57-103">IAnalysisRegion::IntersectsWith method</span></span>

<span data-ttu-id="23f57-104">Determina se l'area del [**IAnalysisRegion**](ianalysisregion.md) interseca il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="23f57-104">Determines whether the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f57-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23f57-105">Syntax</span></span>


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a><span data-ttu-id="23f57-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23f57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f57-107">*pRectangle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23f57-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f57-108">Puntatore al rettangolo con il quale eseguire il confronto, in coordinate dello spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="23f57-108">A pointer to the rectangle with which to compare, in ink-space coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="23f57-109">*pfIsIntersecting* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23f57-109">*pfIsIntersecting* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23f57-110">**Variante \_ TRUE** se l'area di [**IAnalysisRegion**](ianalysisregion.md) si interseca con il rettangolo specificato. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="23f57-110">**VARIANT\_TRUE** if the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f57-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23f57-111">Return value</span></span>

<span data-ttu-id="23f57-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="23f57-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23f57-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="23f57-113">Remarks</span></span>

<span data-ttu-id="23f57-114">Il confronto si trova nelle coordinate dello spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="23f57-114">The comparison is in ink-space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f57-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23f57-115">Requirements</span></span>



| <span data-ttu-id="23f57-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f57-116">Requirement</span></span> | <span data-ttu-id="23f57-117">Valore</span><span class="sxs-lookup"><span data-stu-id="23f57-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f57-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23f57-118">Minimum supported client</span></span><br/> | <span data-ttu-id="23f57-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="23f57-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="23f57-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23f57-120">Minimum supported server</span></span><br/> | <span data-ttu-id="23f57-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="23f57-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="23f57-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23f57-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="23f57-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="23f57-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="23f57-124">DLL</span><span class="sxs-lookup"><span data-stu-id="23f57-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23f57-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23f57-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="23f57-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23f57-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f57-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="23f57-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="23f57-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="23f57-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




