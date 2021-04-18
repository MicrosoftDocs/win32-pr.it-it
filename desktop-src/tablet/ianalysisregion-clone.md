---
description: Crea una copia di IAnalysisRegion.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'Metodo IAnalysisRegion:: Clone (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307472"
---
# <a name="ianalysisregionclone-method"></a><span data-ttu-id="0928c-103">Metodo IAnalysisRegion:: Clone</span><span class="sxs-lookup"><span data-stu-id="0928c-103">IAnalysisRegion::Clone method</span></span>

<span data-ttu-id="0928c-104">Crea una copia di [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="0928c-104">Creates a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0928c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0928c-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="0928c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0928c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0928c-107">*pClonedRegion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0928c-107">*pClonedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0928c-108">Puntatore a una copia di [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="0928c-108">A pointer to a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0928c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0928c-109">Return value</span></span>

<span data-ttu-id="0928c-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0928c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0928c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0928c-111">Remarks</span></span>

<span data-ttu-id="0928c-112">Questo metodo è eqivalent al metodo nomiSystem. Windows. Ink. AnalysisCore. AnalysisRegionBase. Clone nel .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0928c-112">This method is eqivalent to theSystem.Windows.Ink.AnalysisCore.AnalysisRegionBase.Clone Method in the .NET Framework.</span></span>

> [!Caution]  
> <span data-ttu-id="0928c-113">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *pClonedRegion* quando non è più necessario usare l'area di analisi clonata.</span><span class="sxs-lookup"><span data-stu-id="0928c-113">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pClonedRegion* when you no longer need to use the cloned analysis region.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0928c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0928c-114">Requirements</span></span>



| <span data-ttu-id="0928c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0928c-115">Requirement</span></span> | <span data-ttu-id="0928c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0928c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0928c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0928c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0928c-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0928c-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0928c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0928c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0928c-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0928c-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0928c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0928c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0928c-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0928c-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0928c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0928c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0928c-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0928c-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0928c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0928c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0928c-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="0928c-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="0928c-127">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="0928c-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

