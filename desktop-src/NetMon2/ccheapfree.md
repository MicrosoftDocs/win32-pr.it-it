---
description: La funzione CCHeapFree rilascia la memoria allocata dalla funzione CCHeapAlloc.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Funzione CCHeapFree (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131859"
---
# <a name="ccheapfree-function"></a><span data-ttu-id="9ee9e-103">CCHeapFree (funzione)</span><span class="sxs-lookup"><span data-stu-id="9ee9e-103">CCHeapFree function</span></span>

<span data-ttu-id="9ee9e-104">La funzione **CCHeapFree** rilascia la memoria allocata dalla funzione **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="9ee9e-104">The **CCHeapFree** function releases the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ee9e-105">Syntax</span></span>


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="9ee9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ee9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ee9e-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="9ee9e-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee9e-108">Puntatore alla memoria rilasciata da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9ee9e-108">Pointer to the memory that this function releases.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ee9e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ee9e-109">Return value</span></span>

<span data-ttu-id="9ee9e-110">Se la funzione **CCHeapFree** ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="9ee9e-110">If the **CCHeapFree** function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="9ee9e-111">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="9ee9e-111">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ee9e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ee9e-112">Requirements</span></span>



| <span data-ttu-id="9ee9e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ee9e-113">Requirement</span></span> | <span data-ttu-id="9ee9e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9ee9e-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee9e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ee9e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee9e-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ee9e-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9ee9e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ee9e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee9e-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ee9e-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9ee9e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ee9e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ee9e-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ee9e-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9ee9e-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ee9e-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ee9e-122"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ee9e-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ee9e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9ee9e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ee9e-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ee9e-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee9e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ee9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee9e-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="9ee9e-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="9ee9e-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="9ee9e-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="9ee9e-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="9ee9e-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="9ee9e-129">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="9ee9e-129">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="9ee9e-130">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="9ee9e-130">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




