---
description: Il metodo di decommit consente di eseguire il commit dell'allocatore. Questo metodo implementa il metodo IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Metodo CBaseAllocator. decommit (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328270"
---
# <a name="cbaseallocatordecommit-method"></a><span data-ttu-id="7a024-104">CBaseAllocator. decommit (metodo)</span><span class="sxs-lookup"><span data-stu-id="7a024-104">CBaseAllocator.Decommit method</span></span>

<span data-ttu-id="7a024-105">Il `Decommit` metodo consente di eseguire il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="7a024-105">The `Decommit` method decommits the allocator.</span></span> <span data-ttu-id="7a024-106">Questo metodo implementa il metodo [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .</span><span class="sxs-lookup"><span data-stu-id="7a024-106">This method implements the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a024-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a024-107">Syntax</span></span>


```C++
HRESULT Decommit();
```



## <a name="parameters"></a><span data-ttu-id="7a024-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a024-108">Parameters</span></span>

<span data-ttu-id="7a024-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7a024-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a024-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a024-110">Return value</span></span>

<span data-ttu-id="7a024-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7a024-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a024-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a024-112">Remarks</span></span>

<span data-ttu-id="7a024-113">Dopo la chiamata a questo metodo, le chiamate al metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7a024-113">After this method is called, calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method will fail.</span></span> <span data-ttu-id="7a024-114">Man mano che vengono rilasciati, gli esempi vengono restituiti all'elenco di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="7a024-114">As samples are released, they get returned to the free list.</span></span> <span data-ttu-id="7a024-115">Quando viene restituito l'ultimo esempio, l'allocatore chiama il metodo [**CBaseAllocator:: Free**](cbaseallocator-free.md) , che rilascia la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="7a024-115">When the last sample is returned, the allocator calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method, which releases the allocated memory.</span></span> <span data-ttu-id="7a024-116">Nella classe di base, **Free** è un metodo virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="7a024-116">(In the base class, **Free** is a pure virtual method.)</span></span>

<span data-ttu-id="7a024-117">Questo metodo rilascia inoltre tutti i thread bloccati sulle chiamate a **GetBuffer** .</span><span class="sxs-lookup"><span data-stu-id="7a024-117">In addition, this method releases any threads that are blocked on **GetBuffer** calls.</span></span> <span data-ttu-id="7a024-118">Le chiamate a **GetBuffer** hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7a024-118">The calls to **GetBuffer** fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a024-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a024-119">Requirements</span></span>



| <span data-ttu-id="7a024-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a024-120">Requirement</span></span> | <span data-ttu-id="7a024-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7a024-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a024-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a024-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7a024-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a024-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a024-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a024-124">Library</span></span><br/> | <dl> <span data-ttu-id="7a024-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7a024-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a024-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a024-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a024-127">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="7a024-127">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




