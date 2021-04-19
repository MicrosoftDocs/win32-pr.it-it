---
description: 'Il metodo Connect connette il pin a un altro pin. Questo metodo implementa il metodo IPin:: Connect.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: Metodo CBasePin. Connect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333006"
---
# <a name="cbasepinconnect-method"></a><span data-ttu-id="59efe-104">Metodo CBasePin. Connect</span><span class="sxs-lookup"><span data-stu-id="59efe-104">CBasePin.Connect method</span></span>

<span data-ttu-id="59efe-105">Il `Connect` metodo connette il pin a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="59efe-105">The `Connect` method connects the pin to another pin.</span></span> <span data-ttu-id="59efe-106">Questo metodo implementa il metodo [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .</span><span class="sxs-lookup"><span data-stu-id="59efe-106">This method implements the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59efe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59efe-107">Syntax</span></span>


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="59efe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="59efe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59efe-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="59efe-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="59efe-110">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di ricezione.</span><span class="sxs-lookup"><span data-stu-id="59efe-110">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="59efe-111">*PMT*</span><span class="sxs-lookup"><span data-stu-id="59efe-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="59efe-112">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="59efe-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type for the connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59efe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59efe-113">Return value</span></span>

<span data-ttu-id="59efe-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59efe-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="59efe-115">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="59efe-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="59efe-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="59efe-116">Return code</span></span>                                                                                                  | <span data-ttu-id="59efe-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59efe-117">Description</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59efe-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="59efe-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="59efe-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="59efe-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="59efe-120"><dt>**VFW \_ E \_ già \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="59efe-120"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>    | <span data-ttu-id="59efe-121">Il PIN è già connesso.</span><span class="sxs-lookup"><span data-stu-id="59efe-121">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="59efe-122"><dt>**VFW \_ E \_ nessun \_ \_ tipo accettabile**</dt></span><span class="sxs-lookup"><span data-stu-id="59efe-122"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="59efe-123">Impossibile trovare un tipo di supporto accettabile.</span><span class="sxs-lookup"><span data-stu-id="59efe-123">Could not find an acceptable media type.</span></span><br/>                                |
| <dl> <span data-ttu-id="59efe-124"><dt>**VFW \_ E \_ non \_ arrestato**</dt></span><span class="sxs-lookup"><span data-stu-id="59efe-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>          | <span data-ttu-id="59efe-125">Il filtro è attivo e il PIN non supporta la riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="59efe-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="59efe-126"><dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt></span><span class="sxs-lookup"><span data-stu-id="59efe-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl>   | <span data-ttu-id="59efe-127">Il tipo di supporto specificato non è accettabile.</span><span class="sxs-lookup"><span data-stu-id="59efe-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="59efe-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="59efe-128">Remarks</span></span>

<span data-ttu-id="59efe-129">Il parametro *PMT* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="59efe-129">The *pmt* parameter can be **NULL**.</span></span> <span data-ttu-id="59efe-130">Può inoltre specificare un tipo di supporto parziale, con un valore GUID \_ null per il tipo principale, il sottotipo o il formato.</span><span class="sxs-lookup"><span data-stu-id="59efe-130">It can also specify a partial media type, with a value of GUID\_NULL for the major type, subtype, or format.</span></span>

<span data-ttu-id="59efe-131">Nella classe di base, questo metodo verifica se il PIN è già connesso e se il filtro è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="59efe-131">In the base class, this method tests whether the pin is already connected and whether the filter is stopped.</span></span> <span data-ttu-id="59efe-132">Delega il resto del processo di connessione al metodo [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="59efe-132">It delegates the rest of the connection process to the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="59efe-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59efe-133">Requirements</span></span>



| <span data-ttu-id="59efe-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="59efe-134">Requirement</span></span> | <span data-ttu-id="59efe-135">Valore</span><span class="sxs-lookup"><span data-stu-id="59efe-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59efe-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59efe-136">Header</span></span><br/>  | <dl> <span data-ttu-id="59efe-137"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59efe-137"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="59efe-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="59efe-138">Library</span></span><br/> | <dl> <span data-ttu-id="59efe-139"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59efe-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59efe-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59efe-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59efe-141">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="59efe-141">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




