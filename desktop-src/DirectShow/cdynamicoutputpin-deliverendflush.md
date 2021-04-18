---
description: Il metodo DeliverEndFlush richiede al pin di input connesso di terminare un'operazione di svuotamento.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Metodo CDynamicOutputPin. DeliverEndFlush (Amfilter. h)
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
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324792"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="e5089-103">CDynamicOutputPin. DeliverEndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="e5089-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="e5089-104">Il `DeliverEndFlush` metodo richiede al pin di input connesso di terminare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="e5089-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5089-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5089-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="e5089-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5089-106">Parameters</span></span>

<span data-ttu-id="e5089-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e5089-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5089-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5089-108">Return value</span></span>

<span data-ttu-id="e5089-109">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="e5089-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5089-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5089-110">Remarks</span></span>

<span data-ttu-id="e5089-111">Questo metodo esegue l'override del metodo [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="e5089-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="e5089-112">Reimposta l'evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="e5089-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5089-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5089-113">Requirements</span></span>



| <span data-ttu-id="e5089-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5089-114">Requirement</span></span> | <span data-ttu-id="e5089-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e5089-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5089-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5089-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e5089-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5089-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e5089-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5089-118">Library</span></span><br/> | <dl> <span data-ttu-id="e5089-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e5089-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5089-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5089-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5089-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="e5089-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




