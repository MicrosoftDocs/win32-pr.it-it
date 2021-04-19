---
description: Numero di buffer da fornire.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Membro CBaseAllocator:: m_lCount (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329872"
---
# <a name="cbaseallocatorm_lcount-member"></a><span data-ttu-id="206f3-103">Membro lCount di CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="206f3-103">CBaseAllocator::m\_lCount member</span></span>

<span data-ttu-id="206f3-104">Numero di buffer da fornire.</span><span class="sxs-lookup"><span data-stu-id="206f3-104">Number of buffers to provide.</span></span> <span data-ttu-id="206f3-105">Il metodo [**CBaseAllocator:: seproperties**](cbaseallocator-setproperties.md) imposta questo valore.</span><span class="sxs-lookup"><span data-stu-id="206f3-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets this value.</span></span> <span data-ttu-id="206f3-106">I buffer non vengono allocati fino a quando non viene chiamato il metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="206f3-106">The buffers are not allocated until the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method is called.</span></span> <span data-ttu-id="206f3-107">Il numero corrente di buffer allocati viene specificato dalla variabile membro [**CBaseAllocator:: m \_ lAllocated**](cbaseallocator-m-lallocated.md) .</span><span class="sxs-lookup"><span data-stu-id="206f3-107">The current number of allocated buffers is specified by the [**CBaseAllocator::m\_lAllocated**](cbaseallocator-m-lallocated.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="206f3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="206f3-108">Syntax</span></span>


```C++
long m_lCount;
```



## <a name="requirements"></a><span data-ttu-id="206f3-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="206f3-109">Requirements</span></span>



| <span data-ttu-id="206f3-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="206f3-110">Requirement</span></span> | <span data-ttu-id="206f3-111">Valore</span><span class="sxs-lookup"><span data-stu-id="206f3-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="206f3-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="206f3-112">Header</span></span><br/>  | <dl> <span data-ttu-id="206f3-113"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="206f3-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="206f3-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="206f3-114">Library</span></span><br/> | <dl> <span data-ttu-id="206f3-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="206f3-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206f3-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="206f3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206f3-117">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="206f3-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




