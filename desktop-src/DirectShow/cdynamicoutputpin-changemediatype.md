---
description: Il metodo ChangeMediaType modifica dinamicamente il tipo di supporto per la connessione.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Metodo CDynamicOutputPin. ChangeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333453"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a><span data-ttu-id="97a65-103">CDynamicOutputPin. ChangeMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="97a65-103">CDynamicOutputPin.ChangeMediaType method</span></span>

<span data-ttu-id="97a65-104">Il `ChangeMediaType` metodo modifica dinamicamente il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="97a65-104">The `ChangeMediaType` method dynamically changes the media type for the connection.</span></span> <span data-ttu-id="97a65-105">La modifica può verificarsi durante l'esecuzione del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="97a65-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="97a65-106">Una volta chiamato questo metodo, non è possibile recapitare gli esempi con il vecchio tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="97a65-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="97a65-107">Il chiamante deve assicurarsi che non siano presenti esempi obsoleti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="97a65-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a65-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97a65-108">Syntax</span></span>


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="97a65-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="97a65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97a65-110">*PMT*</span><span class="sxs-lookup"><span data-stu-id="97a65-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="97a65-111">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="97a65-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97a65-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97a65-112">Return value</span></span>

<span data-ttu-id="97a65-113">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="97a65-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="97a65-114">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="97a65-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="97a65-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="97a65-115">Return code</span></span>                                                                                           | <span data-ttu-id="97a65-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97a65-116">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="97a65-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="97a65-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="97a65-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="97a65-118">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="97a65-119"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="97a65-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="97a65-120">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97a65-120">Failure.</span></span> <span data-ttu-id="97a65-121">Probabilmente il filtro proprietario non ha chiamato [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="97a65-121">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="97a65-122"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="97a65-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="97a65-123">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="97a65-123">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="97a65-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="97a65-124">Remarks</span></span>

<span data-ttu-id="97a65-125">Chiamare il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="97a65-125">Call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

<span data-ttu-id="97a65-126">Questo metodo controlla prima di tutto se il pin di input downstream può accettare il nuovo formato senza riconnettersi.</span><span class="sxs-lookup"><span data-stu-id="97a65-126">This method first checks whether the downstream input pin can accept the new format without reconnecting.</span></span> <span data-ttu-id="97a65-127">Viene eseguita una query sul pin di input per l'interfaccia [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="97a65-127">It queries the input pin for the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="97a65-128">Se il pin di input supporta **IPinConnection**, il metodo chiama il metodo [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) con il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="97a65-128">If the input pin supports **IPinConnection**, the method calls the [**IPinConnection::DynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) method with the proposed media type.</span></span> <span data-ttu-id="97a65-129">Se il pin di input accetta il nuovo tipo di supporto, il metodo chiama il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e rinegozia i requisiti dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="97a65-129">If the input pin accepts the new media type, the method calls the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method and renegotiates the allocator requirements.</span></span>

<span data-ttu-id="97a65-130">D'altra parte, se il pin downstream non supporta **IPinConnection** o se rifiuta il nuovo tipo di supporto, il metodo chiama il metodo [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) per eseguire una riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="97a65-130">On the other hand, if the downstream pin does not support **IPinConnection**, or if it rejects the new media type, the method calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to perform a dynamic reconnection.</span></span>

## <a name="requirements"></a><span data-ttu-id="97a65-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97a65-131">Requirements</span></span>



| <span data-ttu-id="97a65-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="97a65-132">Requirement</span></span> | <span data-ttu-id="97a65-133">Valore</span><span class="sxs-lookup"><span data-stu-id="97a65-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a65-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97a65-134">Header</span></span><br/>  | <dl> <span data-ttu-id="97a65-135"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97a65-135"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="97a65-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="97a65-136">Library</span></span><br/> | <dl> <span data-ttu-id="97a65-137"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="97a65-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97a65-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97a65-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a65-139">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="97a65-139">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




