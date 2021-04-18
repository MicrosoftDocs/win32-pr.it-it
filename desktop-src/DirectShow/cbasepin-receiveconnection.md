---
description: 'Il metodo ReceiveConnection accetta una connessione da un altro pin. Questo metodo implementa il metodo IPin:: ReceiveConnection.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Metodo CBasePin. ReceiveConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330316"
---
# <a name="cbasepinreceiveconnection-method"></a><span data-ttu-id="06063-104">CBasePin. ReceiveConnection, metodo</span><span class="sxs-lookup"><span data-stu-id="06063-104">CBasePin.ReceiveConnection method</span></span>

<span data-ttu-id="06063-105">Il `ReceiveConnection` metodo accetta una connessione da un altro pin.</span><span class="sxs-lookup"><span data-stu-id="06063-105">The `ReceiveConnection` method accepts a connection from another pin.</span></span> <span data-ttu-id="06063-106">Questo metodo implementa il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .</span><span class="sxs-lookup"><span data-stu-id="06063-106">This method implements the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06063-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06063-107">Syntax</span></span>


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="06063-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06063-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06063-109">*pConnector*</span><span class="sxs-lookup"><span data-stu-id="06063-109">*pConnector*</span></span> 
</dt> <dd>

<span data-ttu-id="06063-110">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di connessione.</span><span class="sxs-lookup"><span data-stu-id="06063-110">Pointer to the connecting pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="06063-111">*PMT*</span><span class="sxs-lookup"><span data-stu-id="06063-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="06063-112">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="06063-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06063-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06063-113">Return value</span></span>

<span data-ttu-id="06063-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06063-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="06063-115">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="06063-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="06063-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="06063-116">Return code</span></span>                                                                                                | <span data-ttu-id="06063-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06063-117">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06063-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="06063-118"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="06063-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="06063-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="06063-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="06063-120"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="06063-121">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="06063-121">**NULL** pointer argument.</span></span><br/>                                              |
| <dl> <span data-ttu-id="06063-122"><dt>**VFW \_ E \_ già \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="06063-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="06063-123">Il PIN è già connesso.</span><span class="sxs-lookup"><span data-stu-id="06063-123">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="06063-124"><dt>**VFW \_ E \_ non \_ arrestato**</dt></span><span class="sxs-lookup"><span data-stu-id="06063-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>        | <span data-ttu-id="06063-125">Il filtro è attivo e il PIN non supporta la riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="06063-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="06063-126"><dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt></span><span class="sxs-lookup"><span data-stu-id="06063-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="06063-127">Il tipo di supporto specificato non è accettabile.</span><span class="sxs-lookup"><span data-stu-id="06063-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="06063-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="06063-128">Remarks</span></span>

<span data-ttu-id="06063-129">Il pin di output chiama questo metodo sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="06063-129">The output pin calls this method on the input pin.</span></span> <span data-ttu-id="06063-130">Se il pin di input restituisce un codice di errore, la connessione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="06063-130">If the input pin returns an error code, the connection fails.</span></span>

<span data-ttu-id="06063-131">Nella classe di base, questo metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="06063-131">In the base class, this method performs the following steps:</span></span>

-   <span data-ttu-id="06063-132">Controlla se il PIN è già connesso.</span><span class="sxs-lookup"><span data-stu-id="06063-132">Checks whether the pin is already connected.</span></span>
-   <span data-ttu-id="06063-133">Controlla se il filtro è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="06063-133">Checks whether the filter is stopped.</span></span>
-   <span data-ttu-id="06063-134">Chiama il metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) per verificare se il pin di connessione è adatto.</span><span class="sxs-lookup"><span data-stu-id="06063-134">Calls the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method to test whether the connecting pin is suitable.</span></span>
-   <span data-ttu-id="06063-135">Chiama il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) per verificare se il tipo di supporto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="06063-135">Calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to test whether the media type is acceptable.</span></span>

<span data-ttu-id="06063-136">Se tutti questi passaggi hanno esito positivo, il metodo chiama i metodi [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) e [**SetMediaType**](cbasepin-setmediatype.md) per completare la connessione.</span><span class="sxs-lookup"><span data-stu-id="06063-136">If all of these steps succeed, the method calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) and [**SetMediaType**](cbasepin-setmediatype.md) methods to complete the connection.</span></span> <span data-ttu-id="06063-137">Questi metodi archiviano il tipo di supporto e un puntatore al pin di output.</span><span class="sxs-lookup"><span data-stu-id="06063-137">These methods store the media type and a pointer to the output pin.</span></span>

<span data-ttu-id="06063-138">Se **CheckConnect** o **CheckMediaType** ha esito negativo, la classe base chiama il metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) per interrompere la connessione e quindi restituisce un codice di errore da `ReceiveConnection` .</span><span class="sxs-lookup"><span data-stu-id="06063-138">If **CheckConnect** or **CheckMediaType** fail, the base class calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to break the connection and then returns an error code from `ReceiveConnection`.</span></span>

## <a name="requirements"></a><span data-ttu-id="06063-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06063-139">Requirements</span></span>



| <span data-ttu-id="06063-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="06063-140">Requirement</span></span> | <span data-ttu-id="06063-141">Valore</span><span class="sxs-lookup"><span data-stu-id="06063-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06063-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06063-142">Header</span></span><br/>  | <dl> <span data-ttu-id="06063-143"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06063-143"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06063-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="06063-144">Library</span></span><br/> | <dl> <span data-ttu-id="06063-145"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06063-145"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06063-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06063-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06063-147">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="06063-147">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




