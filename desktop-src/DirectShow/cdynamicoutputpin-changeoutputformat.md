---
description: Il metodo ChangeOutputFormat modifica dinamicamente il tipo di supporto per la connessione e recapita nuove informazioni sul segmento.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Metodo CDynamicOutputPin. ChangeOutputFormat (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333452"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a><span data-ttu-id="fb6f8-103">CDynamicOutputPin. ChangeOutputFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="fb6f8-103">CDynamicOutputPin.ChangeOutputFormat method</span></span>

<span data-ttu-id="fb6f8-104">Il `ChangeOutputFormat` metodo modifica dinamicamente il tipo di supporto per la connessione e recapita nuove informazioni sul segmento.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-104">The `ChangeOutputFormat` method dynamically changes the media type for the connection, and delivers new segment information.</span></span> <span data-ttu-id="fb6f8-105">La modifica può verificarsi durante l'esecuzione del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="fb6f8-106">Una volta chiamato questo metodo, non è possibile recapitare gli esempi con il vecchio tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="fb6f8-107">Il chiamante deve assicurarsi che non siano presenti esempi obsoleti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6f8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb6f8-108">Syntax</span></span>


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a><span data-ttu-id="fb6f8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb6f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb6f8-110">*PMT*</span><span class="sxs-lookup"><span data-stu-id="fb6f8-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6f8-111">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> <dt>

<span data-ttu-id="fb6f8-112">*tSegmentStart*</span><span class="sxs-lookup"><span data-stu-id="fb6f8-112">*tSegmentStart*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6f8-113">Ora di inizio del segmento.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-113">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="fb6f8-114">*tSegmentStop*</span><span class="sxs-lookup"><span data-stu-id="fb6f8-114">*tSegmentStop*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6f8-115">Ora di arresto del segmento.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-115">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="fb6f8-116">*dSegmentRate*</span><span class="sxs-lookup"><span data-stu-id="fb6f8-116">*dSegmentRate*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6f8-117">Frequenza segmento.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-117">Segment rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb6f8-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb6f8-118">Return value</span></span>

<span data-ttu-id="fb6f8-119">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb6f8-119">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fb6f8-120">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-120">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="fb6f8-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fb6f8-121">Return code</span></span>                                                                                           | <span data-ttu-id="fb6f8-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb6f8-122">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb6f8-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb6f8-123"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="fb6f8-124">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-124">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="fb6f8-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="fb6f8-125"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="fb6f8-126">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-126">Failure.</span></span> <span data-ttu-id="fb6f8-127">Probabilmente il filtro proprietario non ha chiamato [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="fb6f8-127">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="fb6f8-128"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="fb6f8-128"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="fb6f8-129">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-129">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="fb6f8-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb6f8-130">Remarks</span></span>

<span data-ttu-id="fb6f8-131">Questo metodo modifica il tipo di formato durante l'esecuzione del filtro.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-131">This method changes the format type while the filter is running.</span></span> <span data-ttu-id="fb6f8-132">Se il pin downstream accetta il nuovo formato, non è necessaria alcuna riconnessione.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-132">If the downstream pin accepts the new format, no reconnection is necessary.</span></span> <span data-ttu-id="fb6f8-133">In caso contrario, il metodo tenterà di riconnettere il PIN.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-133">Otherwise, the method attempts to reconnect the pin.</span></span> <span data-ttu-id="fb6f8-134">Se il metodo modifica correttamente il formato, recapita le informazioni sul nuovo segmento.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-134">If the method successfully changes the format, it delivers the new segment information.</span></span> <span data-ttu-id="fb6f8-135">Questo metodo chiama il metodo [**CDynamicOutputPin:: ChangeMediaType**](cdynamicoutputpin-changemediatype.md) per eseguire la modifica del formato.</span><span class="sxs-lookup"><span data-stu-id="fb6f8-135">This method calls the [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) method to perform the format change.</span></span>

<span data-ttu-id="fb6f8-136">Prima di chiamare questo metodo, è necessario chiamare il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="fb6f8-136">You must call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6f8-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb6f8-137">Requirements</span></span>



| <span data-ttu-id="fb6f8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb6f8-138">Requirement</span></span> | <span data-ttu-id="fb6f8-139">Valore</span><span class="sxs-lookup"><span data-stu-id="fb6f8-139">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6f8-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb6f8-140">Header</span></span><br/>  | <dl> <span data-ttu-id="fb6f8-141"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb6f8-141"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fb6f8-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="fb6f8-142">Library</span></span><br/> | <dl> <span data-ttu-id="fb6f8-143"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fb6f8-143"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6f8-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb6f8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6f8-145">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="fb6f8-145">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




