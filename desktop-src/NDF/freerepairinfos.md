---
title: Funzione FreeRepairInfos (Ndattributils. h)
description: Consente di deallocare la memoria allocata internamente a una matrice di strutture RepairInfo.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- FreeRepairInfos funzione NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119394"
---
# <a name="freerepairinfos-function"></a><span data-ttu-id="a701d-104">FreeRepairInfos (funzione)</span><span class="sxs-lookup"><span data-stu-id="a701d-104">FreeRepairInfos function</span></span>

<span data-ttu-id="a701d-105">La funzione **FreeRepairInfos** consente di deallocare la memoria allocata internamente a una matrice di strutture [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="a701d-105">The **FreeRepairInfos** function deallocates the memory allocated internally to an array of [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structures.</span></span> <span data-ttu-id="a701d-106">Questa funzione chiama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per deallocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="a701d-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a701d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a701d-107">Syntax</span></span>


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="a701d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a701d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a701d-109">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a701d-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a701d-110">Tipo: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="a701d-110">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="a701d-111">Matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="a701d-111">The array of structures.</span></span> <span data-ttu-id="a701d-112">La memoria allocata a cui fanno riferimento queste strutture verrà liberata.</span><span class="sxs-lookup"><span data-stu-id="a701d-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="a701d-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="a701d-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="a701d-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="a701d-114">Type: **ULONG**</span></span>

<span data-ttu-id="a701d-115">Numero di strutture nella matrice a cui punta *pInfo*.</span><span class="sxs-lookup"><span data-stu-id="a701d-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="a701d-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="a701d-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="a701d-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="a701d-117">Type: **BOOL**</span></span>

<span data-ttu-id="a701d-118">True se è necessario eliminare anche la matrice di strutture. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="a701d-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a701d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a701d-119">Return value</span></span>

<span data-ttu-id="a701d-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a701d-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a701d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a701d-121">Requirements</span></span>



| <span data-ttu-id="a701d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a701d-122">Requirement</span></span> | <span data-ttu-id="a701d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a701d-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a701d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a701d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a701d-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a701d-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a701d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a701d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a701d-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a701d-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a701d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a701d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a701d-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="a701d-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a701d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a701d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a701d-131">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="a701d-131">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[<span data-ttu-id="a701d-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="a701d-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

