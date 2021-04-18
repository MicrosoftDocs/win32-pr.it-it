---
description: Il metodo di attesa incrementa il numero di thread in attesa.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Metodo CBaseAllocator. sewaiting (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331797"
---
# <a name="cbaseallocatorsetwaiting-method"></a><span data-ttu-id="16383-103">Metodo CBaseAllocator. sewaiting</span><span class="sxs-lookup"><span data-stu-id="16383-103">CBaseAllocator.SetWaiting method</span></span>

<span data-ttu-id="16383-104">Il `SetWaiting` metodo incrementa il conteggio dei thread in attesa.</span><span class="sxs-lookup"><span data-stu-id="16383-104">The `SetWaiting` method increments the count of waiting threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="16383-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16383-105">Syntax</span></span>


```C++
void SetWaiting();
```



## <a name="parameters"></a><span data-ttu-id="16383-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16383-106">Parameters</span></span>

<span data-ttu-id="16383-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="16383-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16383-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16383-108">Return value</span></span>

<span data-ttu-id="16383-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="16383-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16383-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="16383-110">Remarks</span></span>

<span data-ttu-id="16383-111">Questo metodo incrementa la variabile membro [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) .</span><span class="sxs-lookup"><span data-stu-id="16383-111">This method increments the [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) member variable.</span></span> <span data-ttu-id="16383-112">Se un thread è bloccato nel metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) , l'allocatore chiama `SetWaiting` e quindi attende la segnalazione del semaforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) .</span><span class="sxs-lookup"><span data-stu-id="16383-112">If a thread is blocked in the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method, the allocator calls `SetWaiting` and then waits for the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore to be signaled.</span></span> <span data-ttu-id="16383-113">Il metodo [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) segnala il semaforo e imposta *m \_ lWaiting* di nuovo su zero.</span><span class="sxs-lookup"><span data-stu-id="16383-113">The [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method signals the semaphore and sets *m\_lWaiting* back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="16383-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16383-114">Requirements</span></span>



| <span data-ttu-id="16383-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="16383-115">Requirement</span></span> | <span data-ttu-id="16383-116">Valore</span><span class="sxs-lookup"><span data-stu-id="16383-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16383-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16383-117">Header</span></span><br/>  | <dl> <span data-ttu-id="16383-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16383-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="16383-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="16383-119">Library</span></span><br/> | <dl> <span data-ttu-id="16383-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="16383-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16383-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16383-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16383-122">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="16383-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




