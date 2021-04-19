---
description: "Flag che indica se il callback di rilascio è abilitato. Questo flag viene impostato nel metodo del costruttore. Se il valore è FALSE, la chiamata al metodo CBaseAllocator:: senotify comporta l'attivazione di un'asserzione (nelle build di debug)."
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Membro CBaseAllocator:: m_fEnableReleaseCallback (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333379"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a><span data-ttu-id="3d5b3-105">Membro fEnableReleaseCallback di CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="3d5b3-105">CBaseAllocator::m\_fEnableReleaseCallback member</span></span>

<span data-ttu-id="3d5b3-106">Flag che indica se il callback di rilascio è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-106">Flag indicating whether the release callback is enabled.</span></span> <span data-ttu-id="3d5b3-107">Questo flag viene impostato nel metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="3d5b3-107">This flag is set in the constructor method.</span></span> <span data-ttu-id="3d5b3-108">Se il valore è **false**, la chiamata al metodo [**CBaseAllocator:: senotify**](cbaseallocator-setnotify.md) comporta l'attivazione di un'asserzione (nelle build di debug).</span><span class="sxs-lookup"><span data-stu-id="3d5b3-108">If the value is **FALSE**, calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method causes an assertion to fire (in debug builds).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d5b3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d5b3-109">Syntax</span></span>


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a><span data-ttu-id="3d5b3-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d5b3-110">Requirements</span></span>



| <span data-ttu-id="3d5b3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d5b3-111">Requirement</span></span> | <span data-ttu-id="3d5b3-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5b3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5b3-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d5b3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3d5b3-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d5b3-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3d5b3-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d5b3-115">Library</span></span><br/> | <dl> <span data-ttu-id="3d5b3-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3d5b3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d5b3-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d5b3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5b3-118">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="3d5b3-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




