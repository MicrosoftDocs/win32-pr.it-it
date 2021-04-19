---
description: Flag che indica se un'operazione di decommit è in corso.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Membro CBaseAllocator:: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326204"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a><span data-ttu-id="f2ec0-103">Membro bDecommitInProgress di CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="f2ec0-103">CBaseAllocator::m\_bDecommitInProgress member</span></span>

<span data-ttu-id="f2ec0-104">Flag che indica se un'operazione di decommit è in corso.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-104">Flag indicating whether a decommit operation is in progress.</span></span> <span data-ttu-id="f2ec0-105">Il valore è **true** dopo la chiamata del metodo [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , ma prima del rilascio di tutti i buffer.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-105">The value is **TRUE** after the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method is called, but before all the buffers have been released.</span></span> <span data-ttu-id="f2ec0-106">Se il valore è **true**, il metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-106">If the value is **TRUE**, the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method fails.</span></span> <span data-ttu-id="f2ec0-107">Inoltre, l'allocatore non deve eliminare se stesso mentre il valore è **true**.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-107">Also, the allocator should not deleted itself while the value is **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ec0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2ec0-108">Syntax</span></span>


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a><span data-ttu-id="f2ec0-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2ec0-109">Requirements</span></span>



| <span data-ttu-id="f2ec0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2ec0-110">Requirement</span></span> | <span data-ttu-id="f2ec0-111">Valore</span><span class="sxs-lookup"><span data-stu-id="f2ec0-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ec0-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2ec0-112">Header</span></span><br/>  | <dl> <span data-ttu-id="f2ec0-113"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2ec0-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f2ec0-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2ec0-114">Library</span></span><br/> | <dl> <span data-ttu-id="f2ec0-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2ec0-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ec0-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2ec0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ec0-117">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="f2ec0-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




