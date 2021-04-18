---
description: Metodo del distruttore.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Distruttore CMemAllocator. ~ CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327448"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="0675c-103">Distruttore CMemAllocator. ~ CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="0675c-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="0675c-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="0675c-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0675c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0675c-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="0675c-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="0675c-106">Remarks</span></span>

<span data-ttu-id="0675c-107">Questo metodo esegue l'override del distruttore della classe base per chiamare [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) e [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="0675c-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0675c-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0675c-108">Requirements</span></span>



| <span data-ttu-id="0675c-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="0675c-109">Requirement</span></span> | <span data-ttu-id="0675c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="0675c-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0675c-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0675c-111">Header</span></span><br/>  | <dl> <span data-ttu-id="0675c-112"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0675c-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0675c-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="0675c-113">Library</span></span><br/> | <dl> <span data-ttu-id="0675c-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0675c-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0675c-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0675c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0675c-116">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="0675c-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




