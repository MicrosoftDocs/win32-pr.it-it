---
description: Recupera l'oggetto IAnalysisAlternate in corrispondenza dell'indice specificato all'interno dell'insieme.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'Metodo IAnalysisAlternates:: GetAnalysisAlternate (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307475"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a><span data-ttu-id="f9bcd-103">Metodo IAnalysisAlternates:: GetAnalysisAlternate</span><span class="sxs-lookup"><span data-stu-id="f9bcd-103">IAnalysisAlternates::GetAnalysisAlternate method</span></span>

<span data-ttu-id="f9bcd-104">Recupera l'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) in corrispondenza dell'indice specificato all'interno dell'insieme.</span><span class="sxs-lookup"><span data-stu-id="f9bcd-104">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9bcd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9bcd-105">Syntax</span></span>


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="f9bcd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9bcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9bcd-107">*ulIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9bcd-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9bcd-108">Indice in base zero dell'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f9bcd-108">The zero-based index of the [**IAnalysisAlternate**](ianalysisalternate.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="f9bcd-109">*ppAlternate* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f9bcd-109">*ppAlternate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9bcd-110">Puntatore all'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) in corrispondenza dell'indice specificato all'interno dell'insieme.</span><span class="sxs-lookup"><span data-stu-id="f9bcd-110">A pointer to the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9bcd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9bcd-111">Return value</span></span>

<span data-ttu-id="f9bcd-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f9bcd-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9bcd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9bcd-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f9bcd-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppAlternate* quando non è più necessario usare l'alternativa di analisi.</span><span class="sxs-lookup"><span data-stu-id="f9bcd-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternate* when you no longer need to use the analysis alternate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f9bcd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9bcd-115">Requirements</span></span>



| <span data-ttu-id="f9bcd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9bcd-116">Requirement</span></span> | <span data-ttu-id="f9bcd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f9bcd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9bcd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9bcd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9bcd-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f9bcd-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f9bcd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9bcd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9bcd-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f9bcd-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f9bcd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9bcd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9bcd-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f9bcd-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f9bcd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f9bcd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9bcd-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9bcd-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f9bcd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9bcd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9bcd-127">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="f9bcd-127">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="f9bcd-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="f9bcd-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

