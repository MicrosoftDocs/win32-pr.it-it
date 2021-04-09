---
title: Funzione FreeRootCauseInfos (Ndattributils. h)
description: Consente di deallocare la memoria allocata internamente a una matrice di strutture RootCauseInfo.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- FreeRootCauseInfos funzione NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740895"
---
# <a name="freerootcauseinfos-function"></a><span data-ttu-id="75b22-104">FreeRootCauseInfos (funzione)</span><span class="sxs-lookup"><span data-stu-id="75b22-104">FreeRootCauseInfos function</span></span>

<span data-ttu-id="75b22-105">La funzione **FreeRootCauseInfos** consente di deallocare la memoria allocata internamente a una matrice di strutture [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="75b22-105">The **FreeRootCauseInfos** function deallocates the memory allocated internally to an array of [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structures.</span></span> <span data-ttu-id="75b22-106">Questa funzione chiama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per deallocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="75b22-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b22-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75b22-107">Syntax</span></span>


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="75b22-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="75b22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b22-109">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b22-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b22-110">Tipo: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="75b22-110">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="75b22-111">Matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="75b22-111">The array of structures.</span></span> <span data-ttu-id="75b22-112">La memoria allocata a cui fanno riferimento queste strutture verrà liberata.</span><span class="sxs-lookup"><span data-stu-id="75b22-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="75b22-113">_RootCauseCount \*</span><span class="sxs-lookup"><span data-stu-id="75b22-113">_RootCauseCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="75b22-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="75b22-114">Type: **ULONG**</span></span>

<span data-ttu-id="75b22-115">Numero di strutture nella matrice a cui punta *pInfo*.</span><span class="sxs-lookup"><span data-stu-id="75b22-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="75b22-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="75b22-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="75b22-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="75b22-117">Type: **BOOL**</span></span>

<span data-ttu-id="75b22-118">True se è necessario eliminare anche la matrice di strutture. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="75b22-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b22-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75b22-119">Return value</span></span>

<span data-ttu-id="75b22-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="75b22-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b22-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75b22-121">Requirements</span></span>



| <span data-ttu-id="75b22-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b22-122">Requirement</span></span> | <span data-ttu-id="75b22-123">Valore</span><span class="sxs-lookup"><span data-stu-id="75b22-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b22-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75b22-124">Minimum supported client</span></span><br/> | <span data-ttu-id="75b22-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="75b22-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75b22-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75b22-126">Minimum supported server</span></span><br/> | <span data-ttu-id="75b22-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="75b22-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="75b22-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75b22-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b22-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b22-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b22-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75b22-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b22-131">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="75b22-131">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[<span data-ttu-id="75b22-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="75b22-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

