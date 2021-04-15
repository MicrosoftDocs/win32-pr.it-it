---
title: Funzione FreeHelperAttributes (Ndattributils. h)
description: Consente di deallocare la memoria allocata internamente a una matrice di \_ strutture di attributi helper.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes funzione NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475988"
---
# <a name="freehelperattributes-function"></a><span data-ttu-id="e9ff6-104">FreeHelperAttributes (funzione)</span><span class="sxs-lookup"><span data-stu-id="e9ff6-104">FreeHelperAttributes function</span></span>

<span data-ttu-id="e9ff6-105">La funzione **FreeHelperAttributes** consente di deallocare la memoria allocata internamente a una matrice di strutture di [**\_ attributi Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="e9ff6-105">The **FreeHelperAttributes** function deallocates the memory allocated internally to an array of [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structures.</span></span> <span data-ttu-id="e9ff6-106">Questa funzione chiama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per deallocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ff6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9ff6-107">Syntax</span></span>


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="e9ff6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9ff6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ff6-109">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9ff6-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ff6-110">Tipo: \**\* [**\_ attributo Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _</span><span class="sxs-lookup"><span data-stu-id="e9ff6-110">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="e9ff6-111">Matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-111">The array of structures.</span></span> <span data-ttu-id="e9ff6-112">La memoria allocata a cui fanno riferimento queste strutture verrà liberata.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="e9ff6-113">_HelperAttributeCount \*</span><span class="sxs-lookup"><span data-stu-id="e9ff6-113">_HelperAttributeCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ff6-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="e9ff6-114">Type: **ULONG**</span></span>

<span data-ttu-id="e9ff6-115">Numero di strutture nella matrice a cui punta *pInfo*.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="e9ff6-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="e9ff6-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ff6-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="e9ff6-117">Type: **BOOL**</span></span>

<span data-ttu-id="e9ff6-118">True se è necessario eliminare anche la matrice di strutture. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ff6-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9ff6-119">Return value</span></span>

<span data-ttu-id="e9ff6-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ff6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9ff6-121">Requirements</span></span>



| <span data-ttu-id="e9ff6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ff6-122">Requirement</span></span> | <span data-ttu-id="e9ff6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e9ff6-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ff6-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9ff6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ff6-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e9ff6-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9ff6-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9ff6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ff6-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e9ff6-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e9ff6-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9ff6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ff6-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ff6-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ff6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9ff6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ff6-131">**Helper ( \_ attributo)**</span><span class="sxs-lookup"><span data-stu-id="e9ff6-131">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[<span data-ttu-id="e9ff6-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="e9ff6-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

