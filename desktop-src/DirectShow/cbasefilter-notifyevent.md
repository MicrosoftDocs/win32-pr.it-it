---
description: Il metodo NotifyEvent invia una notifica degli eventi al gestore del grafico dei filtri.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Metodo CBaseFilter. NotifyEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332079"
---
# <a name="cbasefilternotifyevent-method"></a><span data-ttu-id="0ef92-103">CBaseFilter. NotifyEvent, metodo</span><span class="sxs-lookup"><span data-stu-id="0ef92-103">CBaseFilter.NotifyEvent method</span></span>

<span data-ttu-id="0ef92-104">Il `NotifyEvent` metodo invia una notifica degli eventi al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="0ef92-104">The `NotifyEvent` method sends an event notification to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef92-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ef92-105">Syntax</span></span>


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a><span data-ttu-id="0ef92-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ef92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef92-107">*EventCode*</span><span class="sxs-lookup"><span data-stu-id="0ef92-107">*EventCode*</span></span> 
</dt> <dd>

<span data-ttu-id="0ef92-108">Codice di notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="0ef92-108">Event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0ef92-109">*EventParam1*</span><span class="sxs-lookup"><span data-stu-id="0ef92-109">*EventParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="0ef92-110">Primo parametro dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0ef92-110">First parameter of the event.</span></span>

</dd> <dt>

<span data-ttu-id="0ef92-111">*EventParam2*</span><span class="sxs-lookup"><span data-stu-id="0ef92-111">*EventParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="0ef92-112">Secondo parametro dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0ef92-112">Second parameter of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef92-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ef92-113">Return value</span></span>

<span data-ttu-id="0ef92-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ef92-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0ef92-115">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0ef92-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="0ef92-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0ef92-116">Return code</span></span>                                                                               | <span data-ttu-id="0ef92-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ef92-117">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ef92-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0ef92-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="0ef92-119">Il gestore del grafico del filtro non accetta le notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="0ef92-119">The filter graph manager is not accepting event notifications.</span></span><br/>                              |
| <dl> <span data-ttu-id="0ef92-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ef92-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="0ef92-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0ef92-121">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="0ef92-122"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0ef92-122"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="0ef92-123">Il filtro non dispone di un puntatore all'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="0ef92-123">Filter does not have a pointer to the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ef92-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ef92-124">Remarks</span></span>

<span data-ttu-id="0ef92-125">Per un elenco di codici di notifica e valori di parametri, vedere [codici di notifica degli eventi](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0ef92-125">For a list of notification codes and parameter values, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="0ef92-126">Nella classe di base, se il codice dell'evento è EC \_ completo, il metodo imposta il parametro *EventParam2* su un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro.</span><span class="sxs-lookup"><span data-stu-id="0ef92-126">In the base class, if the event code is EC\_COMPLETE, the method sets the *EventParam2* parameter to a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef92-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ef92-127">Requirements</span></span>



| <span data-ttu-id="0ef92-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ef92-128">Requirement</span></span> | <span data-ttu-id="0ef92-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0ef92-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef92-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ef92-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef92-131"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef92-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ef92-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ef92-132">Library</span></span><br/> | <dl> <span data-ttu-id="0ef92-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef92-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef92-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ef92-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef92-135">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="0ef92-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




