---
description: 'Distruttore CBaseAllocator.~CBaseAllocator : metodo del distruttore.'
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Distruttore CBaseAllocator.~CBaseAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096419"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="820c3-103">Distruttore CBaseAllocator.~CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="820c3-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="820c3-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="820c3-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="820c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="820c3-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="820c3-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="820c3-106">Remarks</span></span>

<span data-ttu-id="820c3-107">Chiamare sempre il [**metodo CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) prima di eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="820c3-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="820c3-108">Il distruttore della classe base non può chiamare **Decommit** perché tale metodo chiama il metodo virtuale [**puro CBaseAllocator::Free.**](cbaseallocator-free.md)</span><span class="sxs-lookup"><span data-stu-id="820c3-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="820c3-109">Le classi derivate devono eseguire l'override di questo distruttore e **chiamare Decommit**.</span><span class="sxs-lookup"><span data-stu-id="820c3-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="820c3-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="820c3-110">Requirements</span></span>



| <span data-ttu-id="820c3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="820c3-111">Requirement</span></span> | <span data-ttu-id="820c3-112">Valore</span><span class="sxs-lookup"><span data-stu-id="820c3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="820c3-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="820c3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="820c3-114"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="820c3-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="820c3-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="820c3-115">Library</span></span><br/> | <dl> <span data-ttu-id="820c3-116"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="820c3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="820c3-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="820c3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="820c3-118">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="820c3-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




