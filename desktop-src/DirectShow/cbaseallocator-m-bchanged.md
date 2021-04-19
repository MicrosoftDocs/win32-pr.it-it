---
description: Flag che indica se i requisiti del buffer sono stati modificati.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Membro CBaseAllocator:: m_bChanged (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331556"
---
# <a name="cbaseallocatorm_bchanged-member"></a><span data-ttu-id="da75b-103">Membro bChanged di CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="da75b-103">CBaseAllocator::m\_bChanged member</span></span>

<span data-ttu-id="da75b-104">Flag che indica se i requisiti del buffer sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="da75b-104">Flag indicating whether the buffer requirements have changed.</span></span> <span data-ttu-id="da75b-105">Il metodo [**CBaseAllocator:: seproperties**](cbaseallocator-setproperties.md) imposta il valore su **true**.</span><span class="sxs-lookup"><span data-stu-id="da75b-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets the value to **TRUE**.</span></span> <span data-ttu-id="da75b-106">In una classe derivata, il metodo virtuale pure [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) deve impostare di nuovo il valore su **false**.</span><span class="sxs-lookup"><span data-stu-id="da75b-106">In a derived class, the pure virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) should set the value back to **FALSE**.</span></span> <span data-ttu-id="da75b-107">Una volta allocati i buffer, non è necessario riallocarli mentre *m \_ BChanged* è **false**.</span><span class="sxs-lookup"><span data-stu-id="da75b-107">Once buffers have been allocated, there is no need to re-allocate them while *m\_bChanged* is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="da75b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da75b-108">Syntax</span></span>


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a><span data-ttu-id="da75b-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da75b-109">Requirements</span></span>



| <span data-ttu-id="da75b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="da75b-110">Requirement</span></span> | <span data-ttu-id="da75b-111">Valore</span><span class="sxs-lookup"><span data-stu-id="da75b-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da75b-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da75b-112">Header</span></span><br/>  | <dl> <span data-ttu-id="da75b-113"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da75b-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="da75b-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="da75b-114">Library</span></span><br/> | <dl> <span data-ttu-id="da75b-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="da75b-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da75b-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da75b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da75b-117">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="da75b-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




