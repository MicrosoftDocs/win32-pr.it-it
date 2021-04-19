---
description: Il metodo CompleteConnect completa una connessione pin.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Metodo CTransInPlaceFilter. CompleteConnect (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdc9d1d5567cda2e4b0fd4a351136405493ef61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332979"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a><span data-ttu-id="d8d79-103">CTransInPlaceFilter. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="d8d79-103">CTransInPlaceFilter.CompleteConnect method</span></span>

<span data-ttu-id="d8d79-104">Il `CompleteConnect` metodo completa una connessione pin.</span><span class="sxs-lookup"><span data-stu-id="d8d79-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8d79-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="d8d79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8d79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d79-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="d8d79-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d79-108">Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica quale pin del filtro sta effettuando la connessione.</span><span class="sxs-lookup"><span data-stu-id="d8d79-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="d8d79-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="d8d79-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d79-110">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="d8d79-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8d79-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8d79-111">Return value</span></span>

<span data-ttu-id="d8d79-112">Restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d8d79-112">Returns an **HRESULT**.</span></span> <span data-ttu-id="d8d79-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d8d79-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d8d79-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d8d79-114">Return code</span></span>                                                                                           | <span data-ttu-id="d8d79-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8d79-115">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="d8d79-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8d79-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="d8d79-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d8d79-117">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="d8d79-118"><dt>**VFW \_ E \_ non \_ in \_ Graph**</dt></span><span class="sxs-lookup"><span data-stu-id="d8d79-118"><dt>**VFW\_E\_NOT\_IN\_GRAPH**</dt></span></span> </dl> | <span data-ttu-id="d8d79-119">Il filtro non è in un grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="d8d79-119">The filter is not in a filter graph.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d8d79-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8d79-120">Remarks</span></span>

<span data-ttu-id="d8d79-121">Questo metodo esegue l'override del metodo [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="d8d79-121">This method overrides the [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method.</span></span>

<span data-ttu-id="d8d79-122">Il comportamento del filtro dipende dall'ordine delle connessioni pin:</span><span class="sxs-lookup"><span data-stu-id="d8d79-122">The behavior of the filter depends on the order of the pin connections:</span></span>

-   <span data-ttu-id="d8d79-123">Se il pin di input è connesso per primo, la connessione usa un allocatore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="d8d79-123">If the input pin is connected first, the connection uses a temporary allocator.</span></span> <span data-ttu-id="d8d79-124">Quando il pin di output è connesso, il filtro riconnette il pin di input.</span><span class="sxs-lookup"><span data-stu-id="d8d79-124">When the output pin is connected, the filter reconnects the input pin.</span></span> <span data-ttu-id="d8d79-125">Riconnettendo il pin di input, il filtro upstream rinegozierà l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="d8d79-125">Reconnecting the input pin causes the upstream filter to renegotiate the allocator.</span></span> <span data-ttu-id="d8d79-126">A questo punto, il pin di input propone un allocatore dal filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="d8d79-126">At that point, the input pin proposes an allocator from the downstream filter.</span></span> <span data-ttu-id="d8d79-127">Per ulteriori informazioni, vedere [**CTransInPlaceInputPin:: Getallocator**](ctransinplaceinputpin-getallocator.md).</span><span class="sxs-lookup"><span data-stu-id="d8d79-127">For more information, see [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span></span>
-   <span data-ttu-id="d8d79-128">Se il pin di output è connesso per primo, il pin di output non seleziona un allocatore.</span><span class="sxs-lookup"><span data-stu-id="d8d79-128">If the output pin is connected first, the output pin does not select an allocator.</span></span> <span data-ttu-id="d8d79-129">Quando il pin di input è connesso, negozia un allocatore per entrambe le connessioni.</span><span class="sxs-lookup"><span data-stu-id="d8d79-129">When the input pin is connected, it negotiates an allocator for both connections.</span></span> <span data-ttu-id="d8d79-130">Se i tipi di supporto di input e di output non sono uguali, il filtro riconnette il pin di output usando il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="d8d79-130">If the input and output media types are not the same, the filter reconnects the output pin using the input type.</span></span>

<span data-ttu-id="d8d79-131">Il filtro esegue tutte le riconnessioni pin chiamando il metodo [**CBaseFilter:: ReconnectPin**](cbasefilter-reconnectpin.md) .</span><span class="sxs-lookup"><span data-stu-id="d8d79-131">The filter performs all pin reconnections by calling the [**CBaseFilter::ReconnectPin**](cbasefilter-reconnectpin.md) method.</span></span> <span data-ttu-id="d8d79-132">Il metodo **ReconnectPin** , a sua volta, chiama il metodo [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) in gestione grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="d8d79-132">The **ReconnectPin** method, in turn, calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d79-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8d79-133">Requirements</span></span>



| <span data-ttu-id="d8d79-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8d79-134">Requirement</span></span> | <span data-ttu-id="d8d79-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d8d79-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d79-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8d79-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d8d79-137"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8d79-137"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8d79-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8d79-138">Library</span></span><br/> | <dl> <span data-ttu-id="d8d79-139"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d8d79-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d79-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8d79-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d79-141">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="d8d79-141">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




