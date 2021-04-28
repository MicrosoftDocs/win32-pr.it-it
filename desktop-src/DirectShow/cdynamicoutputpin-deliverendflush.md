---
description: "Metodo CDynamicOutputPin.DeliverEndFlush: il metodo DeliverEndFlush richiede al pin di input connesso di terminare un'operazione di scaricamento."
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Metodo CDynamicOutputPin.DeliverEndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095709"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="12902-103">Metodo CDynamicOutputPin.DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="12902-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="12902-104">Il `DeliverEndFlush` metodo richiede al pin di input connesso di terminare un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="12902-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="12902-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12902-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="12902-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12902-106">Parameters</span></span>

<span data-ttu-id="12902-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="12902-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12902-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12902-108">Return value</span></span>

<span data-ttu-id="12902-109">Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="12902-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="12902-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="12902-110">Remarks</span></span>

<span data-ttu-id="12902-111">Questo metodo esegue l'override [**del metodo CBaseOutputPin::D eliverEndFlush.**](cbaseoutputpin-deliverendflush.md)</span><span class="sxs-lookup"><span data-stu-id="12902-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="12902-112">Reimposta l'evento [**\_ HStopEvent CDynamicOutputPin::m.**](cdynamicoutputpin-m-hstopevent.md)</span><span class="sxs-lookup"><span data-stu-id="12902-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="12902-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12902-113">Requirements</span></span>



| <span data-ttu-id="12902-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="12902-114">Requirement</span></span> | <span data-ttu-id="12902-115">Valore</span><span class="sxs-lookup"><span data-stu-id="12902-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12902-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12902-116">Header</span></span><br/>  | <dl> <span data-ttu-id="12902-117"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="12902-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="12902-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="12902-118">Library</span></span><br/> | <dl> <span data-ttu-id="12902-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="12902-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12902-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12902-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12902-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="12902-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




