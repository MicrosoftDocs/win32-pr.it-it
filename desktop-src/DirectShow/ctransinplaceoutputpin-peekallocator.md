---
description: Il metodo PeekAllocator restituisce un puntatore all'allocatore del PIN. Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Metodo CTransInPlaceOutputPin. PeekAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326170"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="0a013-104">CTransInPlaceOutputPin. PeekAllocator, metodo</span><span class="sxs-lookup"><span data-stu-id="0a013-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="0a013-105">Il `PeekAllocator` metodo restituisce un puntatore all'allocatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="0a013-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="0a013-106">Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0a013-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a013-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a013-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="0a013-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a013-108">Parameters</span></span>

<span data-ttu-id="0a013-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0a013-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a013-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a013-110">Return value</span></span>

<span data-ttu-id="0a013-111">Restituisce la variabile membro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="0a013-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a013-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a013-112">Requirements</span></span>



| <span data-ttu-id="0a013-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a013-113">Requirement</span></span> | <span data-ttu-id="0a013-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0a013-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a013-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a013-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0a013-116"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a013-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a013-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a013-117">Library</span></span><br/> | <dl> <span data-ttu-id="0a013-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0a013-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a013-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a013-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a013-120">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0a013-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




