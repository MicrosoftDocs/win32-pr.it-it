---
description: Il metodo PeekAllocator restituisce un puntatore all'allocatore del PIN. Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Metodo CTransInPlaceInputPin. PeekAllocator (Transip. h)
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
ms.openlocfilehash: 22358dd776a0536cfbae819ec7cace02dd1775a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326188"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="f74ee-104">CTransInPlaceInputPin. PeekAllocator, metodo</span><span class="sxs-lookup"><span data-stu-id="f74ee-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="f74ee-105">Il `PeekAllocator` metodo restituisce un puntatore all'allocatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="f74ee-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="f74ee-106">Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f74ee-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f74ee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f74ee-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="f74ee-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f74ee-108">Parameters</span></span>

<span data-ttu-id="f74ee-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f74ee-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f74ee-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f74ee-110">Return value</span></span>

<span data-ttu-id="f74ee-111">Restituisce la variabile membro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="f74ee-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f74ee-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f74ee-112">Requirements</span></span>



| <span data-ttu-id="f74ee-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f74ee-113">Requirement</span></span> | <span data-ttu-id="f74ee-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f74ee-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f74ee-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f74ee-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f74ee-116"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f74ee-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f74ee-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="f74ee-117">Library</span></span><br/> | <dl> <span data-ttu-id="f74ee-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f74ee-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f74ee-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f74ee-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f74ee-120">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="f74ee-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




