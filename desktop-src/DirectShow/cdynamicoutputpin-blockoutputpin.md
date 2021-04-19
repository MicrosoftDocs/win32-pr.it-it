---
description: Il metodo BlockOutputPin blocca il PIN.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Metodo CDynamicOutputPin. BlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333457"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a><span data-ttu-id="76092-103">CDynamicOutputPin. BlockOutputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="76092-103">CDynamicOutputPin.BlockOutputPin method</span></span>

<span data-ttu-id="76092-104">Il `BlockOutputPin` metodo blocca il PIN.</span><span class="sxs-lookup"><span data-stu-id="76092-104">The `BlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="76092-105">Quando il PIN è bloccato, il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) attende che il PIN venga sbloccato.</span><span class="sxs-lookup"><span data-stu-id="76092-105">While the pin is blocked, the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method waits for the pin to become unblocked.</span></span> <span data-ttu-id="76092-106">Lo stato bloccato impedisce al pin di output di consegnare esempi, modificare il formato di output o riconnettersi.</span><span class="sxs-lookup"><span data-stu-id="76092-106">The blocked state prevents the output pin from delivering samples, changing its output format, or reconnecting itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="76092-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76092-107">Syntax</span></span>


```C++
void BlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="76092-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="76092-108">Parameters</span></span>

<span data-ttu-id="76092-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="76092-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76092-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76092-110">Return value</span></span>

<span data-ttu-id="76092-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="76092-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76092-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="76092-112">Remarks</span></span>

<span data-ttu-id="76092-113">Prima di chiamare questo metodo, conservare la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical.</span><span class="sxs-lookup"><span data-stu-id="76092-113">Before calling this method, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span> <span data-ttu-id="76092-114">Non chiamare questo metodo se un thread di streaming usa il PIN, per recapitare i dati o per modificare la connessione.</span><span class="sxs-lookup"><span data-stu-id="76092-114">Do not call this method if a streaming thread is using the pin, either to deliver data or to change the connection.</span></span> <span data-ttu-id="76092-115">Per verificare se un thread di streaming sta usando il PIN, chiamare il metodo [**CDynamicOutputPin:: StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="76092-115">To check whether a streaming thread is using the pin, call the [**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="76092-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76092-116">Requirements</span></span>



| <span data-ttu-id="76092-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="76092-117">Requirement</span></span> | <span data-ttu-id="76092-118">Valore</span><span class="sxs-lookup"><span data-stu-id="76092-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76092-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76092-119">Header</span></span><br/>  | <dl> <span data-ttu-id="76092-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76092-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="76092-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="76092-121">Library</span></span><br/> | <dl> <span data-ttu-id="76092-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="76092-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76092-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76092-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76092-124">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="76092-124">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




