---
description: Prefisso di ogni buffer, in byte.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Membro CBaseAllocator:: m_lPrefix (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325787"
---
# <a name="cbaseallocatorm_lprefix-member"></a><span data-ttu-id="95fcf-103">Membro lPrefix di CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="95fcf-103">CBaseAllocator::m\_lPrefix member</span></span>

<span data-ttu-id="95fcf-104">Prefisso di ogni buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="95fcf-104">Prefix of each buffer, in bytes.</span></span> <span data-ttu-id="95fcf-105">Se il valore è diverso da zero, ogni puntatore del buffer restituito dal metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) è preceduto da un blocco di byte di dimensioni *m \_ lPrefix*.</span><span class="sxs-lookup"><span data-stu-id="95fcf-105">If the value is non-zero, each buffer pointer returned by the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method is preceded by a block of bytes of size *m\_lPrefix*.</span></span> <span data-ttu-id="95fcf-106">Questo blocco di memoria viene chiamato *prefisso*.</span><span class="sxs-lookup"><span data-stu-id="95fcf-106">This memory block is called the *prefix*.</span></span> <span data-ttu-id="95fcf-107">La variabile membro [**CBaseAllocator:: m \_ lSize**](cbaseallocator-m-lsize.md) non include il valore del prefisso.</span><span class="sxs-lookup"><span data-stu-id="95fcf-107">The [**CBaseAllocator::m\_lSize**](cbaseallocator-m-lsize.md) member variable does not include the prefix value.</span></span>

## <a name="syntax"></a><span data-ttu-id="95fcf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95fcf-108">Syntax</span></span>


```C++
long m_lPrefix;
```



## <a name="requirements"></a><span data-ttu-id="95fcf-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95fcf-109">Requirements</span></span>



| <span data-ttu-id="95fcf-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="95fcf-110">Requirement</span></span> | <span data-ttu-id="95fcf-111">Valore</span><span class="sxs-lookup"><span data-stu-id="95fcf-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fcf-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95fcf-112">Header</span></span><br/>  | <dl> <span data-ttu-id="95fcf-113"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95fcf-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95fcf-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="95fcf-114">Library</span></span><br/> | <dl> <span data-ttu-id="95fcf-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95fcf-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95fcf-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95fcf-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95fcf-117">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="95fcf-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




