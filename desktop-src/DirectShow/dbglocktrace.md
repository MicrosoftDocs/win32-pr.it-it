---
description: Abilita o Disabilita la registrazione di debug di una sezione critica specificata.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Funzione DbgLockTrace (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327525"
---
# <a name="dbglocktrace-function"></a><span data-ttu-id="96bd4-103">DbgLockTrace (funzione)</span><span class="sxs-lookup"><span data-stu-id="96bd4-103">DbgLockTrace function</span></span>

<span data-ttu-id="96bd4-104">Abilita o Disabilita la registrazione di debug di una sezione critica specificata.</span><span class="sxs-lookup"><span data-stu-id="96bd4-104">Enables or disables debug logging of a given critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="96bd4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96bd4-105">Syntax</span></span>


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a><span data-ttu-id="96bd4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96bd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96bd4-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="96bd4-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="96bd4-108">Puntatore a una sezione critica [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="96bd4-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> <dt>

<span data-ttu-id="96bd4-109">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="96bd4-109">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="96bd4-110">Valore che specifica se la registrazione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="96bd4-110">Value specifying whether logging is enabled.</span></span> <span data-ttu-id="96bd4-111">Usare **true** per abilitare la registrazione o **false** per disabilitarla.</span><span class="sxs-lookup"><span data-stu-id="96bd4-111">Use **TRUE** to enable logging or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96bd4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96bd4-112">Return value</span></span>

<span data-ttu-id="96bd4-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="96bd4-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96bd4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="96bd4-114">Remarks</span></span>

<span data-ttu-id="96bd4-115">Usare questa funzione per tracciare una sezione critica specifica.</span><span class="sxs-lookup"><span data-stu-id="96bd4-115">Use this function to trace a specific critical section.</span></span> <span data-ttu-id="96bd4-116">Per impostazione predefinita, la registrazione del debug delle sezioni critiche è disabilitata a causa del numero elevato di sezioni critiche.</span><span class="sxs-lookup"><span data-stu-id="96bd4-116">By default, debug logging of critical sections is disabled, because of the large number of critical sections.</span></span>

<span data-ttu-id="96bd4-117">Per tracciare una sezione critica, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="96bd4-117">To trace a critical section, perform the following steps:</span></span>

1.  <span data-ttu-id="96bd4-118">Definire DEBUG o \_ debug prima di includere le intestazioni DirectShow.</span><span class="sxs-lookup"><span data-stu-id="96bd4-118">Define DEBUG or \_DEBUG before you include the DirectShow headers.</span></span>
2.  <span data-ttu-id="96bd4-119">Abilitare la registrazione di debug per le sezioni critiche, chiamando [**DbgSetModuleLevel**](dbgsetmodulelevel.md) con il flag di blocco del log \_ .</span><span class="sxs-lookup"><span data-stu-id="96bd4-119">Enable debug logging for critical sections, by calling [**DbgSetModuleLevel**](dbgsetmodulelevel.md) with the LOG\_LOCKING flag.</span></span>
3.  <span data-ttu-id="96bd4-120">Chiamare **DbgLockTrace** nella sezione critica che si desidera tracciare.</span><span class="sxs-lookup"><span data-stu-id="96bd4-120">Call **DbgLockTrace** on the critical section you want to trace.</span></span>

<span data-ttu-id="96bd4-121">Nelle compilazioni finali, la funzione **DbgLockTrace** non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="96bd4-121">In retail builds, the **DbgLockTrace** function has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="96bd4-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="96bd4-122">Examples</span></span>

<span data-ttu-id="96bd4-123">Nell'esempio di codice riportato di seguito viene illustrato come tracciare una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="96bd4-123">The following code example shows how to trace a critical section.</span></span>


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a><span data-ttu-id="96bd4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96bd4-124">Requirements</span></span>



| <span data-ttu-id="96bd4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="96bd4-125">Requirement</span></span> | <span data-ttu-id="96bd4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="96bd4-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96bd4-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96bd4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="96bd4-128"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96bd4-128"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="96bd4-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="96bd4-129">Library</span></span><br/> | <dl> <span data-ttu-id="96bd4-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="96bd4-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96bd4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96bd4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96bd4-132">Funzioni di debug della sezione critica</span><span class="sxs-lookup"><span data-stu-id="96bd4-132">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




