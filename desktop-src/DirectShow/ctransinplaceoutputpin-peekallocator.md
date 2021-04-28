---
description: "Metodo CTransInPlaceOutputPin.PeekAllocator: il metodo PeekAllocator restituisce un puntatore all'allocatore del pin. Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia ."
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Metodo CTransInPlaceOutputPin.PeekAllocator (Transip.h)
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
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084599"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="a7214-104">Metodo CTransInPlaceOutputPin.PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="a7214-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="a7214-105">Il `PeekAllocator` metodo restituisce un puntatore all'allocatore del pin.</span><span class="sxs-lookup"><span data-stu-id="a7214-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="a7214-106">Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia .</span><span class="sxs-lookup"><span data-stu-id="a7214-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7214-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7214-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="a7214-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7214-108">Parameters</span></span>

<span data-ttu-id="a7214-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a7214-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7214-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7214-110">Return value</span></span>

<span data-ttu-id="a7214-111">Restituisce la [**variabile membro CBaseOutputPin::m \_ pAllocator.**](cbaseoutputpin-m-pallocator.md)</span><span class="sxs-lookup"><span data-stu-id="a7214-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7214-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7214-112">Requirements</span></span>



| <span data-ttu-id="a7214-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7214-113">Requirement</span></span> | <span data-ttu-id="a7214-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a7214-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7214-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7214-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a7214-116"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7214-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7214-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="a7214-117">Library</span></span><br/> | <dl> <span data-ttu-id="a7214-118"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a7214-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7214-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7214-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7214-120">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="a7214-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




