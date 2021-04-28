---
description: "Metodo CTransInPlaceInputPin.PeekAllocator: il metodo PeekAllocator restituisce un puntatore all'allocatore del pin. Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia ."
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Metodo CTransInPlaceInputPin.PeekAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7a5f7cb0fbe754890b1d7930bb54c6fca47afa5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084669"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="46273-104">Metodo CTransInPlaceInputPin.PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="46273-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="46273-105">Il `PeekAllocator` metodo restituisce un puntatore all'allocatore del pin.</span><span class="sxs-lookup"><span data-stu-id="46273-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="46273-106">Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia .</span><span class="sxs-lookup"><span data-stu-id="46273-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="46273-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46273-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="46273-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46273-108">Parameters</span></span>

<span data-ttu-id="46273-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="46273-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46273-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46273-110">Return value</span></span>

<span data-ttu-id="46273-111">Restituisce la [**variabile membro CBaseInputPin::m \_ pAllocator.**](cbaseinputpin-m-pallocator.md)</span><span class="sxs-lookup"><span data-stu-id="46273-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="46273-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46273-112">Requirements</span></span>



| <span data-ttu-id="46273-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="46273-113">Requirement</span></span> | <span data-ttu-id="46273-114">Valore</span><span class="sxs-lookup"><span data-stu-id="46273-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46273-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46273-115">Header</span></span><br/>  | <dl> <span data-ttu-id="46273-116"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="46273-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46273-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="46273-117">Library</span></span><br/> | <dl> <span data-ttu-id="46273-118"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="46273-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46273-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46273-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46273-120">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="46273-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




