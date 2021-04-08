---
description: La funzione GetCCInstPtr restituisce il puntatore ai dati dell'istanza aggiunti al contesto di acquisizione.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Funzione GetCCInstPtr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750090"
---
# <a name="getccinstptr-function"></a><span data-ttu-id="6317d-103">GetCCInstPtr (funzione)</span><span class="sxs-lookup"><span data-stu-id="6317d-103">GetCCInstPtr function</span></span>

<span data-ttu-id="6317d-104">La funzione **GetCCInstPtr** restituisce il puntatore ai dati dell'istanza aggiunti al contesto di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6317d-104">The **GetCCInstPtr** function returns the pointer to the instance data added to the capture context.</span></span>

## <a name="syntax"></a><span data-ttu-id="6317d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6317d-105">Syntax</span></span>


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a><span data-ttu-id="6317d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6317d-106">Parameters</span></span>

<span data-ttu-id="6317d-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="6317d-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6317d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6317d-108">Return value</span></span>

<span data-ttu-id="6317d-109">Se la funzione ha esito positivo, il valore restituito è un puntatore ai dati dell'istanza di un'acquisizione specifica.</span><span class="sxs-lookup"><span data-stu-id="6317d-109">If the function is successful, the return value is a pointer to the instance data of a specific capture.</span></span>

<span data-ttu-id="6317d-110">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="6317d-110">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6317d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6317d-111">Requirements</span></span>



| <span data-ttu-id="6317d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6317d-112">Requirement</span></span> | <span data-ttu-id="6317d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6317d-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6317d-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6317d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6317d-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6317d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6317d-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6317d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6317d-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6317d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6317d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6317d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6317d-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6317d-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="6317d-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="6317d-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="6317d-121"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6317d-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6317d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6317d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6317d-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6317d-123"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6317d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6317d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6317d-125">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="6317d-125">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="6317d-126">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="6317d-126">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="6317d-127">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="6317d-127">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="6317d-128">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="6317d-128">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="6317d-129">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="6317d-129">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




