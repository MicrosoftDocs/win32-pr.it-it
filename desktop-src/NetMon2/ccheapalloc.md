---
description: La funzione CCHeapAlloc alloca memoria in base a un'acquisizione.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Funzione CCHeapAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881442"
---
# <a name="ccheapalloc-function"></a><span data-ttu-id="4f7c0-103">CCHeapAlloc (funzione)</span><span class="sxs-lookup"><span data-stu-id="4f7c0-103">CCHeapAlloc function</span></span>

<span data-ttu-id="4f7c0-104">La funzione **CCHeapAlloc** alloca memoria in base a un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4f7c0-104">The **CCHeapAlloc** function allocates memory on a capture-by-capture basis.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f7c0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f7c0-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="4f7c0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f7c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f7c0-107">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="4f7c0-107">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="4f7c0-108">Lunghezza della memoria richiesta allocata.</span><span class="sxs-lookup"><span data-stu-id="4f7c0-108">Requested length of memory allocated.</span></span>

</dd> <dt>

<span data-ttu-id="4f7c0-109">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="4f7c0-109">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="4f7c0-110">Indica se la memoria allocata è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="4f7c0-110">Indicator of whether allocated memory was initialized.</span></span> <span data-ttu-id="4f7c0-111">Se il valore del parametro è **true**, la memoria allocata viene inizializzata su zero.</span><span class="sxs-lookup"><span data-stu-id="4f7c0-111">If the parameter value is **TRUE**, the allocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f7c0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f7c0-112">Return value</span></span>

<span data-ttu-id="4f7c0-113">Se la funzione ha esito positivo, il valore restituito è un puntatore alla memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="4f7c0-113">If the function is successful, the return value is a pointer to the allocated memory.</span></span> <span data-ttu-id="4f7c0-114">Al termine dell'utilizzo della memoria allocata, liberare la memoria chiamando la funzione [**CCHeapFree**](ccheapfree.md) .</span><span class="sxs-lookup"><span data-stu-id="4f7c0-114">When you have finished using the allocated memory, free the memory by calling the [**CCHeapFree**](ccheapfree.md) function.</span></span>

<span data-ttu-id="4f7c0-115">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="4f7c0-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f7c0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f7c0-116">Requirements</span></span>



| <span data-ttu-id="4f7c0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f7c0-117">Requirement</span></span> | <span data-ttu-id="4f7c0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4f7c0-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f7c0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f7c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f7c0-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f7c0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4f7c0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f7c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f7c0-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f7c0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4f7c0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f7c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f7c0-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f7c0-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4f7c0-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f7c0-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f7c0-126"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f7c0-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4f7c0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4f7c0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f7c0-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f7c0-128"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f7c0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f7c0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f7c0-130">**SetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="4f7c0-130">**SetCCInstPtr**</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="4f7c0-131">**GetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="4f7c0-131">**GetCCInstPtr**</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="4f7c0-132">**CCHeapFree**</span><span class="sxs-lookup"><span data-stu-id="4f7c0-132">**CCHeapFree**</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="4f7c0-133">**CCHeapReAlloc**</span><span class="sxs-lookup"><span data-stu-id="4f7c0-133">**CCHeapReAlloc**</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="4f7c0-134">**CCHeapSize**</span><span class="sxs-lookup"><span data-stu-id="4f7c0-134">**CCHeapSize**</span></span>](ccheapsize.md)
</dt> </dl>

 

 




