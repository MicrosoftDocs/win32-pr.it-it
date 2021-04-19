---
description: Se è stata raggiunta la fine del flusso, il metodo SendEndOfStream pianifica un \_ evento di completamento EC per il gestore del grafico dei filtri.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Metodo CBaseRenderer. SendEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326428"
---
# <a name="cbaserenderersendendofstream-method"></a><span data-ttu-id="c2170-103">CBaseRenderer. SendEndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="c2170-103">CBaseRenderer.SendEndOfStream method</span></span>

<span data-ttu-id="c2170-104">Se è stata raggiunta la fine del flusso, il `SendEndOfStream` metodo pianifica un \_ evento di completamento EC per il gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="c2170-104">If end-of-stream was reached, the `SendEndOfStream` method schedules an EC\_COMPLETE event for the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2170-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2170-105">Syntax</span></span>


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="c2170-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2170-106">Parameters</span></span>

<span data-ttu-id="c2170-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c2170-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2170-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2170-108">Return value</span></span>

<span data-ttu-id="c2170-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2170-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c2170-110">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c2170-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="c2170-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c2170-111">Return code</span></span>                                                                             | <span data-ttu-id="c2170-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2170-112">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2170-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c2170-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c2170-114">Il gestore del grafico del filtro non accetta le notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="c2170-114">The filter graph manager is not accepting event notifications.</span></span><br/> |
| <dl> <span data-ttu-id="c2170-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c2170-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c2170-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c2170-116">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c2170-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2170-117">Remarks</span></span>

<span data-ttu-id="c2170-118">Il filtro potrebbe ricevere una notifica di fine flusso prima dell'ora di arresto dell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="c2170-118">The filter might receive an end-of-stream notification before the current sample's stop time.</span></span> <span data-ttu-id="c2170-119">In tal caso, il filtro deve attendere prima di inviare una notifica di [**\_ completamento della EC**](ec-complete.md) al gestore del grafo dei filtri.</span><span class="sxs-lookup"><span data-stu-id="c2170-119">If so, the filter should wait before posting an [**EC\_COMPLETE**](ec-complete.md) notification to the filter graph manager.</span></span>

<span data-ttu-id="c2170-120">Di conseguenza:</span><span class="sxs-lookup"><span data-stu-id="c2170-120">Therefore:</span></span>

-   <span data-ttu-id="c2170-121">Se il filtro ha ricevuto una notifica di fine del flusso (EOS) iniziale, questo metodo pianifica un evento del timer.</span><span class="sxs-lookup"><span data-stu-id="c2170-121">If the filter has received an early end-of-stream (EOS) notification, this method schedules a timer event.</span></span> <span data-ttu-id="c2170-122">Quando l'evento timer viene attivato, il filtro Invia l' \_ evento di completamento EC.</span><span class="sxs-lookup"><span data-stu-id="c2170-122">When the timer event is activated, the filter posts the EC\_COMPLETE event.</span></span>
-   <span data-ttu-id="c2170-123">Se il filtro ha ricevuto una notifica EOS che non era anticipata, questo metodo invia \_ immediatamente l'evento di completamento EC.</span><span class="sxs-lookup"><span data-stu-id="c2170-123">If the filter has received an EOS notification that was not early, this method posts the EC\_COMPLETE event immediately.</span></span>
-   <span data-ttu-id="c2170-124">Se il filtro non dispone di alcuna notifica EOS in sospeso, il metodo restituisce senza eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="c2170-124">If the filter does not have any pending EOS notification, the method returns without doing anything.</span></span>

<span data-ttu-id="c2170-125">Il metodo di callback del timer è [**CBaseRenderer:: TimerCallback**](cbaserenderer-timercallback.md).</span><span class="sxs-lookup"><span data-stu-id="c2170-125">The timer callback method is [**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md).</span></span> <span data-ttu-id="c2170-126">Per recapitare l' \_ evento EC completo, il filtro chiama il metodo [**CBaseRenderer:: NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="c2170-126">To deliver the EC\_COMPLETE event, the filter calls the [**CBaseRenderer::NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2170-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2170-127">Requirements</span></span>



| <span data-ttu-id="c2170-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2170-128">Requirement</span></span> | <span data-ttu-id="c2170-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c2170-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2170-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2170-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c2170-131"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2170-131"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c2170-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c2170-132">Library</span></span><br/> | <dl> <span data-ttu-id="c2170-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c2170-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2170-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2170-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2170-135">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="c2170-135">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




