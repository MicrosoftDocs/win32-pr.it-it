---
description: La funzione SetCCInstPtr acquisisce un puntatore all'istanza del contesto.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: Funzione SetCCInstPtr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526754"
---
# <a name="setccinstptr-function"></a><span data-ttu-id="b7e85-103">SetCCInstPtr (funzione)</span><span class="sxs-lookup"><span data-stu-id="b7e85-103">SetCCInstPtr function</span></span>

<span data-ttu-id="b7e85-104">La funzione **SetCCInstPtr** acquisisce un puntatore all'istanza del contesto.</span><span class="sxs-lookup"><span data-stu-id="b7e85-104">The **SetCCInstPtr** function captures a context instance pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e85-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7e85-105">Syntax</span></span>


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a><span data-ttu-id="b7e85-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7e85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e85-107">*lpCurCaptureInst*</span><span class="sxs-lookup"><span data-stu-id="b7e85-107">*lpCurCaptureInst*</span></span> 
</dt> <dd>

<span data-ttu-id="b7e85-108">Puntatore ai dati dell'istanza aggiunti all'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b7e85-108">Pointer to the instance data added to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e85-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7e85-109">Return value</span></span>

<span data-ttu-id="b7e85-110">No.</span><span class="sxs-lookup"><span data-stu-id="b7e85-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e85-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b7e85-111">Remarks</span></span>

<span data-ttu-id="b7e85-112">Utilizzare questa funzione per archiviare un puntatore a un blocco allocato con la funzione **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="b7e85-112">Use this function to store a pointer to a block that was allocated with the **CCHeapAlloc** function.</span></span> <span data-ttu-id="b7e85-113">Ogni parser può impostare una singola istanza di dati in un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b7e85-113">Each parser can set a single instance of data on a capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e85-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7e85-114">Requirements</span></span>



| <span data-ttu-id="b7e85-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e85-115">Requirement</span></span> | <span data-ttu-id="b7e85-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b7e85-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e85-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7e85-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e85-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7e85-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b7e85-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7e85-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e85-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7e85-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b7e85-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7e85-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e85-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e85-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b7e85-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7e85-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7e85-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7e85-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b7e85-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e85-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e85-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e85-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7e85-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7e85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e85-128">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="b7e85-128">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="b7e85-129">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="b7e85-129">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="b7e85-130">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="b7e85-130">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="b7e85-131">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="b7e85-131">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="b7e85-132">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="b7e85-132">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




