---
description: Recupera il numero di oggetti IContextNode contenuti in questa raccolta.
ms.assetid: 7cc60bea-9a4c-4ac8-ad1a-0fca5e941c5e
title: 'Metodo IContextNodes:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d694849b3436f9f30a687579362d01a111ace80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129483"
---
# <a name="icontextnodesgetcount-method"></a><span data-ttu-id="a1e05-103">Metodo IContextNodes:: GetCount</span><span class="sxs-lookup"><span data-stu-id="a1e05-103">IContextNodes::GetCount method</span></span>

<span data-ttu-id="a1e05-104">Recupera il numero di oggetti [**IContextNode**](icontextnode.md) contenuti in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="a1e05-104">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e05-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1e05-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="a1e05-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1e05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e05-107">*pulCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1e05-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e05-108">Numero di oggetti [**IContextNode**](icontextnode.md) contenuti in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="a1e05-108">The number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e05-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1e05-109">Return value</span></span>

<span data-ttu-id="a1e05-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a1e05-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e05-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1e05-111">Requirements</span></span>



| <span data-ttu-id="a1e05-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1e05-112">Requirement</span></span> | <span data-ttu-id="a1e05-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a1e05-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e05-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1e05-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e05-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a1e05-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a1e05-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1e05-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e05-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a1e05-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a1e05-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1e05-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e05-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1e05-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1e05-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a1e05-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1e05-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1e05-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a1e05-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1e05-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e05-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="a1e05-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="a1e05-124">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="a1e05-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




