---
description: La funzione CCHeapReAlloc consente di riallocare la memoria allocata dalla funzione CCHeapAlloc.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Funzione CCHeapReAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756452"
---
# <a name="ccheaprealloc-function"></a><span data-ttu-id="2db4e-103">CCHeapReAlloc (funzione)</span><span class="sxs-lookup"><span data-stu-id="2db4e-103">CCHeapReAlloc function</span></span>

<span data-ttu-id="2db4e-104">La funzione **CCHeapReAlloc** consente di riallocare la memoria allocata dalla funzione **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="2db4e-104">The **CCHeapReAlloc** function reallocates memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db4e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2db4e-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="2db4e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2db4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db4e-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="2db4e-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="2db4e-108">Puntatore alla memoria allocata originale.</span><span class="sxs-lookup"><span data-stu-id="2db4e-108">Pointer to the original allocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="2db4e-109">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="2db4e-109">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="2db4e-110">Dimensione della memoria riallocata, misurata in byte.</span><span class="sxs-lookup"><span data-stu-id="2db4e-110">Size of the reallocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2db4e-111">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="2db4e-111">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="2db4e-112">Indica se la memoria riallocata è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="2db4e-112">Indicator of whether reallocated memory was initialized.</span></span> <span data-ttu-id="2db4e-113">Se il valore del parametro è **true**, la nuova memoria riallocata viene inizializzata su zero.</span><span class="sxs-lookup"><span data-stu-id="2db4e-113">If the parameter value is **TRUE**, the newly reallocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db4e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2db4e-114">Return value</span></span>

<span data-ttu-id="2db4e-115">Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria riallocata.</span><span class="sxs-lookup"><span data-stu-id="2db4e-115">If the function is successful, the return value is a pointer to the reallocated memory.</span></span>

<span data-ttu-id="2db4e-116">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="2db4e-116">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2db4e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2db4e-117">Requirements</span></span>



| <span data-ttu-id="2db4e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2db4e-118">Requirement</span></span> | <span data-ttu-id="2db4e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2db4e-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2db4e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2db4e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2db4e-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2db4e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2db4e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2db4e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2db4e-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2db4e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2db4e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2db4e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db4e-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db4e-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2db4e-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="2db4e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2db4e-127"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2db4e-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2db4e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2db4e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2db4e-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2db4e-129"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2db4e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2db4e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db4e-131">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="2db4e-131">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="2db4e-132">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="2db4e-132">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="2db4e-133">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="2db4e-133">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="2db4e-134">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="2db4e-134">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="2db4e-135">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="2db4e-135">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




