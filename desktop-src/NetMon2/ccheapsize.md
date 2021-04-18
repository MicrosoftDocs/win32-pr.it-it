---
description: La funzione CCHeapSize restituisce le dimensioni della memoria allocata dalla funzione CCHeapAlloc.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Funzione CCHeapSize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314183"
---
# <a name="ccheapsize-function"></a><span data-ttu-id="b505f-103">CCHeapSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="b505f-103">CCHeapSize function</span></span>

<span data-ttu-id="b505f-104">La funzione **CCHeapSize** restituisce le dimensioni della memoria allocata dalla funzione **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="b505f-104">The **CCHeapSize** function returns the size of the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b505f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b505f-105">Syntax</span></span>


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="b505f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b505f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b505f-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="b505f-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="b505f-108">Puntatore alla memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="b505f-108">Pointer to the allocated memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b505f-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b505f-109">Return value</span></span>

<span data-ttu-id="b505f-110">Se la funzione ha esito positivo, il valore restituito corrisponde alla dimensione del blocco di memoria richiesto misurato in byte.</span><span class="sxs-lookup"><span data-stu-id="b505f-110">If the function is successful, the return value is the size of the requested memory block   measured in bytes.</span></span>

<span data-ttu-id="b505f-111">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="b505f-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b505f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b505f-112">Requirements</span></span>



| <span data-ttu-id="b505f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b505f-113">Requirement</span></span> | <span data-ttu-id="b505f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b505f-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b505f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b505f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b505f-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b505f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b505f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b505f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b505f-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b505f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b505f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b505f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b505f-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b505f-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b505f-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="b505f-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="b505f-122"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b505f-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b505f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b505f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b505f-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b505f-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b505f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b505f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b505f-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="b505f-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="b505f-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="b505f-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="b505f-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="b505f-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="b505f-129">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="b505f-129">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="b505f-130">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="b505f-130">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> </dl>

 

 




