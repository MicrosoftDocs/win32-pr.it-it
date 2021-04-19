---
description: Metodo del distruttore.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Distruttore CBaseAllocator. ~ CBaseAllocator (Amfilter. h)
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
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324043"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="540a9-103">Distruttore CBaseAllocator. ~ CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="540a9-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="540a9-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="540a9-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="540a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="540a9-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="540a9-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="540a9-106">Remarks</span></span>

<span data-ttu-id="540a9-107">Chiamare sempre il metodo [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) prima di eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="540a9-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="540a9-108">Il distruttore della classe base non può chiamare il metodo **decommit**, perché il metodo chiama il metodo virtuale pure [**CBaseAllocator:: Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="540a9-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="540a9-109">Le classi derivate devono eseguire l'override di questo distruttore e chiamare **decommit**.</span><span class="sxs-lookup"><span data-stu-id="540a9-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="540a9-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="540a9-110">Requirements</span></span>



| <span data-ttu-id="540a9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="540a9-111">Requirement</span></span> | <span data-ttu-id="540a9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="540a9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="540a9-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="540a9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="540a9-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="540a9-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="540a9-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="540a9-115">Library</span></span><br/> | <dl> <span data-ttu-id="540a9-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="540a9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="540a9-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="540a9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="540a9-118">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="540a9-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




