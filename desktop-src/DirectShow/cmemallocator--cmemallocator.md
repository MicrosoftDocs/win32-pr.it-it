---
description: Distruttore CMemAllocator.~CMemAllocator - Metodo del distruttore.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Distruttore CMemAllocator.~CMemAllocator (Amfilter.h)
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
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095409"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="91b83-103">Distruttore CMemAllocator.~CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="91b83-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="91b83-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="91b83-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91b83-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="91b83-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="91b83-106">Remarks</span></span>

<span data-ttu-id="91b83-107">Questo metodo esegue l'override del distruttore della classe base per chiamare [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) e [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="91b83-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91b83-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91b83-108">Requirements</span></span>



| <span data-ttu-id="91b83-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="91b83-109">Requirement</span></span> | <span data-ttu-id="91b83-110">Valore</span><span class="sxs-lookup"><span data-stu-id="91b83-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91b83-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91b83-111">Header</span></span><br/>  | <dl> <span data-ttu-id="91b83-112"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="91b83-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="91b83-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="91b83-113">Library</span></span><br/> | <dl> <span data-ttu-id="91b83-114"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="91b83-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91b83-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91b83-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b83-116">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="91b83-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




