---
description: Libera un blocco di memoria allocato da un heap da RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Funzione RtlFreeHeap (Ntifs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523586"
---
# <a name="rtlfreeheap-function"></a><span data-ttu-id="45e54-103">RtlFreeHeap (funzione)</span><span class="sxs-lookup"><span data-stu-id="45e54-103">RtlFreeHeap function</span></span>

<span data-ttu-id="45e54-104">Libera un blocco di memoria allocato da un heap da [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="45e54-104">Frees a memory block that was allocated from a heap by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

## <a name="syntax"></a><span data-ttu-id="45e54-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45e54-105">Syntax</span></span>


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a><span data-ttu-id="45e54-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45e54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45e54-107">*HeapHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45e54-107">*HeapHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45e54-108">Handle per l'heap il cui blocco di memoria deve essere liberato.</span><span class="sxs-lookup"><span data-stu-id="45e54-108">A handle for the heap whose memory block is to be freed.</span></span> <span data-ttu-id="45e54-109">Questo parametro è un handle restituito da [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="45e54-109">This parameter is a handle returned by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>

</dd> <dt>

<span data-ttu-id="45e54-110">*Flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="45e54-110">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="45e54-111">Set di flag che controlla gli aspetti della liberazione di un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="45e54-111">A set of flags that controls aspects of freeing a memory block.</span></span> <span data-ttu-id="45e54-112">Se si specifica il valore seguente, viene eseguito l'override del valore corrispondente specificato nel parametro *Flags* quando l'heap è stato creato da [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="45e54-112">Specifying the following value overrides the corresponding value that was specified in the *Flags* parameter when the heap was created by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>



| <span data-ttu-id="45e54-113">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="45e54-113">Flag</span></span>                           | <span data-ttu-id="45e54-114">Significato</span><span class="sxs-lookup"><span data-stu-id="45e54-114">Meaning</span></span>                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e54-115">HEAP \_ senza \_ serializzazione</span><span class="sxs-lookup"><span data-stu-id="45e54-115">HEAP\_NO\_SERIALIZE</span></span><br/> | <span data-ttu-id="45e54-116">L'esclusione reciproca non verrà usata quando **RtlFreeHeap** accede all'heap.</span><span class="sxs-lookup"><span data-stu-id="45e54-116">Mutual exclusion will not be used when **RtlFreeHeap** is accessing the heap.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="45e54-117">*HeapBase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45e54-117">*HeapBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45e54-118">Puntatore al blocco di memoria da liberare.</span><span class="sxs-lookup"><span data-stu-id="45e54-118">A pointer to the memory block to free.</span></span> <span data-ttu-id="45e54-119">Questo puntatore viene restituito da [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="45e54-119">This pointer is returned by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45e54-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45e54-120">Return value</span></span>

<span data-ttu-id="45e54-121">Restituisce **true** se il blocco è stato liberato correttamente. In caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="45e54-121">Returns **TRUE** if the block was freed successfully; **FALSE** otherwise.</span></span>

> [!Note]  
> <span data-ttu-id="45e54-122">A partire da Windows 8, il valore restituito viene tipizzato come **Logical**, che ha dimensioni diverse rispetto a **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="45e54-122">Starting with Windows 8 the return value is typed as **LOGICAL**, which has a different size than **BOOLEAN**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45e54-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45e54-123">Requirements</span></span>



| <span data-ttu-id="45e54-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="45e54-124">Requirement</span></span> | <span data-ttu-id="45e54-125">Valore</span><span class="sxs-lookup"><span data-stu-id="45e54-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e54-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45e54-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45e54-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45e54-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="45e54-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45e54-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45e54-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45e54-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="45e54-130">Piattaforma di destinazione</span><span class="sxs-lookup"><span data-stu-id="45e54-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="45e54-131"><dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="45e54-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="45e54-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45e54-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="45e54-133"><dt>Ntifs. h (include Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45e54-133"><dt>Ntifs.h (include Ntifs.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="45e54-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="45e54-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="45e54-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45e54-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="45e54-136">DLL</span><span class="sxs-lookup"><span data-stu-id="45e54-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45e54-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45e54-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="45e54-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45e54-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45e54-139">**RtlAllocateHeap**</span><span class="sxs-lookup"><span data-stu-id="45e54-139">**RtlAllocateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[<span data-ttu-id="45e54-140">**RtlCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="45e54-140">**RtlCreateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[<span data-ttu-id="45e54-141">**RtlDestroyHeap**</span><span class="sxs-lookup"><span data-stu-id="45e54-141">**RtlDestroyHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
