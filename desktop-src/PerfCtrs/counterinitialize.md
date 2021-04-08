---
description: Registra il provider e inizializza gli insiemi di contatori.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: CounterInitialize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967521"
---
# <a name="counterinitialize-function"></a><span data-ttu-id="6dc83-103">CounterInitialize (funzione)</span><span class="sxs-lookup"><span data-stu-id="6dc83-103">CounterInitialize function</span></span>

<span data-ttu-id="6dc83-104">Registra il provider e inizializza gli insiemi di contatori.</span><span class="sxs-lookup"><span data-stu-id="6dc83-104">Registers the provider and initializes the counter sets.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dc83-105">Syntax</span></span>


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="6dc83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6dc83-106">Parameters</span></span>

<span data-ttu-id="6dc83-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="6dc83-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6dc83-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6dc83-108">Return value</span></span>

<span data-ttu-id="6dc83-109">Restituisce \_ l'errore in caso di esito positivo; in caso contrario, un codice di errore Win32 standard.</span><span class="sxs-lookup"><span data-stu-id="6dc83-109">Returns ERROR\_SUCCESS on success; otherwise, a standard Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dc83-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6dc83-110">Remarks</span></span>

<span data-ttu-id="6dc83-111">Il provider chiama questa funzione.</span><span class="sxs-lookup"><span data-stu-id="6dc83-111">Your provider calls this function.</span></span> <span data-ttu-id="6dc83-112">La funzione include le chiamate alla funzione [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) e alla funzione [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="6dc83-112">The function includes calls to the [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) function and the [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) function.</span></span>

<span data-ttu-id="6dc83-113">Lo strumento [**CTRPP**](ctrpp.md) genera questa funzione inline quando si specifica l'argomento **-o** .</span><span class="sxs-lookup"><span data-stu-id="6dc83-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="6dc83-114">Il nome della funzione include una stringa di *prefisso* se si specifica l'argomento **-Prefix** .</span><span class="sxs-lookup"><span data-stu-id="6dc83-114">The function's name include a *prefix* string if you specify the **-prefix** argument.</span></span>

<span data-ttu-id="6dc83-115">Se si specificano gli argomenti **-MemoryRoutines** o **-NotificationCallback** (o si specifica l'attributo di **callback** per l'elemento [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), la firma **CounterInitialize** apportata come segue:</span><span class="sxs-lookup"><span data-stu-id="6dc83-115">If you specify the **-MemoryRoutines** or **-NotificationCallback** arguments (or specify the **callback** attribute for the [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) element), the **CounterInitialize** signature changes to the following:</span></span>

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

<span data-ttu-id="6dc83-116">dove</span><span class="sxs-lookup"><span data-stu-id="6dc83-116">where,</span></span>

<dl> <dt>

<span data-ttu-id="6dc83-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span><span class="sxs-lookup"><span data-stu-id="6dc83-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span></span>
</dt> <dd>

<span data-ttu-id="6dc83-118">Nome della funzione di callback [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) implementata per ricevere la notifica delle richieste del consumer (ad esempio, le richieste di aggiungere o rimuovere i contatori dalla query).</span><span class="sxs-lookup"><span data-stu-id="6dc83-118">The name of your [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) callback function that you implement to receive notification of consumer requests (for example, requests to add or remove counters from the query).</span></span> <span data-ttu-id="6dc83-119">Impostare su **null** se non si implementa la funzione di callback *ControlCallback* .</span><span class="sxs-lookup"><span data-stu-id="6dc83-119">Set to **NULL** if you do not implement the *ControlCallback* callback function.</span></span>

</dd> <dt>

<span data-ttu-id="6dc83-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span><span class="sxs-lookup"><span data-stu-id="6dc83-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span></span>
</dt> <dd>

<span data-ttu-id="6dc83-121">Nome della funzione di callback [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) chiamata da Perflib per allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="6dc83-121">The name of your [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) callback function that PERFLIB calls to allocate memory.</span></span> <span data-ttu-id="6dc83-122">Impostare su **null** se non è stato specificato l'argomento **-MemoryRoutines** .</span><span class="sxs-lookup"><span data-stu-id="6dc83-122">Set to **NULL** if you did not specify the **-MemoryRoutines** argument.</span></span>

</dd> <dt>

<span data-ttu-id="6dc83-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span><span class="sxs-lookup"><span data-stu-id="6dc83-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span></span>
</dt> <dd>

<span data-ttu-id="6dc83-124">Nome della funzione di callback [*freememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) chiamata da Perflib per liberare la memoria allocata tramite la funzione [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) .</span><span class="sxs-lookup"><span data-stu-id="6dc83-124">The name of your [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) callback function that PERFLIB calls to free the memory allocated using the [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) function.</span></span> <span data-ttu-id="6dc83-125">Impostare su **null** se *MemoryAllocationFunction* è **null**.</span><span class="sxs-lookup"><span data-stu-id="6dc83-125">Set to **NULL** if *MemoryAllocationFunction* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6dc83-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span><span class="sxs-lookup"><span data-stu-id="6dc83-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span></span>
</dt> <dd>

<span data-ttu-id="6dc83-127">Informazioni di contesto da passare all'allocazione di memoria e alle routine gratuite.</span><span class="sxs-lookup"><span data-stu-id="6dc83-127">Context information to pass to your memory allocation and free routines.</span></span> <span data-ttu-id="6dc83-128">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6dc83-128">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dc83-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6dc83-129">Requirements</span></span>



| <span data-ttu-id="6dc83-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dc83-130">Requirement</span></span> | <span data-ttu-id="6dc83-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6dc83-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6dc83-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dc83-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc83-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6dc83-133">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6dc83-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dc83-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc83-135">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6dc83-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

