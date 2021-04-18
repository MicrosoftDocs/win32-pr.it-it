---
description: Recupera il numero di oggetti IAnalysisAlternate contenuti nella raccolta IAnalysisAlternates.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'Metodo IAnalysisAlternates:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6300ff994d7bd49461e9be39aa433586ecaabc75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307473"
---
# <a name="ianalysisalternatesgetcount-method"></a><span data-ttu-id="93780-103">Metodo IAnalysisAlternates:: GetCount</span><span class="sxs-lookup"><span data-stu-id="93780-103">IAnalysisAlternates::GetCount method</span></span>

<span data-ttu-id="93780-104">Recupera il numero di oggetti [**IAnalysisAlternate**](ianalysisalternate.md) contenuti nella raccolta [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="93780-104">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="93780-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93780-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="93780-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93780-107">*pulCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="93780-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93780-108">Intero senza segno a 32 bit impostato sul numero di oggetti [**IAnalysisAlternate**](ianalysisalternate.md) contenuti nella raccolta [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="93780-108">An unsigned 32-bit integer that is set to the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93780-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93780-109">Return value</span></span>

<span data-ttu-id="93780-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="93780-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93780-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93780-111">Requirements</span></span>



| <span data-ttu-id="93780-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="93780-112">Requirement</span></span> | <span data-ttu-id="93780-113">Valore</span><span class="sxs-lookup"><span data-stu-id="93780-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93780-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93780-114">Minimum supported client</span></span><br/> | <span data-ttu-id="93780-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="93780-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="93780-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93780-116">Minimum supported server</span></span><br/> | <span data-ttu-id="93780-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="93780-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="93780-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93780-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="93780-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="93780-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="93780-120">DLL</span><span class="sxs-lookup"><span data-stu-id="93780-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93780-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93780-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="93780-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93780-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93780-123">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="93780-123">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="93780-124">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="93780-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




