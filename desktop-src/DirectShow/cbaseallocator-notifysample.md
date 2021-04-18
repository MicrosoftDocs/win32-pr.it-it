---
description: Il metodo NotifySample rilascia tutti i thread in attesa di esempi.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Metodo CBaseAllocator. NotifySample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331805"
---
# <a name="cbaseallocatornotifysample-method"></a><span data-ttu-id="7c574-103">CBaseAllocator. NotifySample, metodo</span><span class="sxs-lookup"><span data-stu-id="7c574-103">CBaseAllocator.NotifySample method</span></span>

<span data-ttu-id="7c574-104">Il `NotifySample` metodo rilascia tutti i thread in attesa di esempi.</span><span class="sxs-lookup"><span data-stu-id="7c574-104">The `NotifySample` method releases any threads that are waiting for samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c574-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c574-105">Syntax</span></span>


```C++
void NotifySample();
```



## <a name="parameters"></a><span data-ttu-id="7c574-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c574-106">Parameters</span></span>

<span data-ttu-id="7c574-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7c574-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c574-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c574-108">Return value</span></span>

<span data-ttu-id="7c574-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7c574-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c574-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c574-110">Remarks</span></span>

<span data-ttu-id="7c574-111">Quando sono presenti thread in attesa di campioni, il valore di [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) è maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="7c574-111">When there are threads waiting for samples, the value of [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) is greater than zero.</span></span> <span data-ttu-id="7c574-112">Se *m \_ lWaiting* è maggiore di zero, questo metodo chiama la funzione **ReleaseSemaphore** sul semaforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) , attivando eventuali thread in attesa.</span><span class="sxs-lookup"><span data-stu-id="7c574-112">If *m\_lWaiting* is greater than zero, this method calls the **ReleaseSemaphore** function on the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore, activating any waiting threads.</span></span> <span data-ttu-id="7c574-113">Reimposta anche *m \_ lWaiting* su zero.</span><span class="sxs-lookup"><span data-stu-id="7c574-113">It also resets *m\_lWaiting* to zero.</span></span>

<span data-ttu-id="7c574-114">Questo metodo viene chiamato dall'interno del metodo [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) , quando un campione viene restituito all'elenco di disponibilità. e dal metodo [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , quando viene eseguito il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="7c574-114">This method is called from within the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method, when a sample is returned to the free list; and from the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method, when the allocator is decommitted.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c574-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c574-115">Requirements</span></span>



| <span data-ttu-id="7c574-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c574-116">Requirement</span></span> | <span data-ttu-id="7c574-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7c574-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c574-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c574-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7c574-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c574-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7c574-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c574-120">Library</span></span><br/> | <dl> <span data-ttu-id="7c574-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7c574-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c574-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c574-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c574-123">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="7c574-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




