---
description: Restituisce TRUE se il thread corrente è il proprietario della sezione critica specificata.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Funzione CritCheckIn (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327190"
---
# <a name="critcheckin-function"></a><span data-ttu-id="e6dfc-103">CritCheckIn (funzione)</span><span class="sxs-lookup"><span data-stu-id="e6dfc-103">CritCheckIn function</span></span>

<span data-ttu-id="e6dfc-104">Restituisce **true** se il thread corrente è il proprietario della sezione critica specificata.</span><span class="sxs-lookup"><span data-stu-id="e6dfc-104">Returns **TRUE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6dfc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6dfc-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="e6dfc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6dfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6dfc-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="e6dfc-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="e6dfc-108">Puntatore a una sezione critica [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="e6dfc-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6dfc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6dfc-109">Return value</span></span>

<span data-ttu-id="e6dfc-110">Nelle compilazioni di debug, restituisce **true** se il thread corrente è il proprietario di questa sezione critica o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e6dfc-110">In debug builds, returns **TRUE** if the current thread is the owner of this critical section, or **FALSE** otherwise.</span></span> <span data-ttu-id="e6dfc-111">Nelle compilazioni finali restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="e6dfc-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6dfc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6dfc-112">Remarks</span></span>

<span data-ttu-id="e6dfc-113">Questa funzione è particolarmente utile all'interno della macro [**Assert**](assert.md) per verificare se un thread è proprietario di un determinato blocco.</span><span class="sxs-lookup"><span data-stu-id="e6dfc-113">This function is especially useful within the [**ASSERT**](assert.md) macro, to test whether a thread owns a given lock.</span></span>

## <a name="examples"></a><span data-ttu-id="e6dfc-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="e6dfc-114">Examples</span></span>

<span data-ttu-id="e6dfc-115">Nell'esempio di codice seguente viene illustrato come utilizzare questa funzione:</span><span class="sxs-lookup"><span data-stu-id="e6dfc-115">The following code example shows how to use this function:</span></span>


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a><span data-ttu-id="e6dfc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6dfc-116">Requirements</span></span>



| <span data-ttu-id="e6dfc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6dfc-117">Requirement</span></span> | <span data-ttu-id="e6dfc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e6dfc-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6dfc-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6dfc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e6dfc-120"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6dfc-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e6dfc-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6dfc-121">Library</span></span><br/> | <dl> <span data-ttu-id="e6dfc-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6dfc-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6dfc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6dfc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6dfc-124">Funzioni di debug della sezione critica</span><span class="sxs-lookup"><span data-stu-id="e6dfc-124">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




