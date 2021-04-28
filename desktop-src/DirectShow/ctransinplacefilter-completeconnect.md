---
description: 'Metodo CTransInPlaceFilter.CompleteConnect: il metodo CompleteConnect completa una connessione pin.'
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Metodo CTransInPlaceFilter.CompleteConnect (Transip.h)
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
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084789"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a><span data-ttu-id="8f8b3-103">Metodo CTransInPlaceFilter.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="8f8b3-103">CTransInPlaceFilter.CompleteConnect method</span></span>

<span data-ttu-id="8f8b3-104">Il `CompleteConnect` metodo completa una connessione pin.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f8b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f8b3-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="8f8b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f8b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f8b3-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="8f8b3-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="8f8b3-108">Membro del [**tipo enumerato PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica quale pin nel filtro sta effettuando la connessione.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="8f8b3-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="8f8b3-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="8f8b3-110">Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f8b3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f8b3-111">Return value</span></span>

<span data-ttu-id="8f8b3-112">Restituisce un **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="8f8b3-112">Returns an **HRESULT**.</span></span> <span data-ttu-id="8f8b3-113">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8f8b3-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8f8b3-114">Return code</span></span>                                                                                           | <span data-ttu-id="8f8b3-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f8b3-115">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="8f8b3-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b3-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="8f8b3-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-117">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="8f8b3-118"><dt>**VFW \_ E NON IN \_ \_ \_ GRAPH**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b3-118"><dt>**VFW\_E\_NOT\_IN\_GRAPH**</dt></span></span> </dl> | <span data-ttu-id="8f8b3-119">Il filtro non è in un grafico filtri.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-119">The filter is not in a filter graph.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f8b3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f8b3-120">Remarks</span></span>

<span data-ttu-id="8f8b3-121">Questo metodo esegue l'override [**del metodo CTransformFilter::CompleteConnect.**](ctransformfilter-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="8f8b3-121">This method overrides the [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method.</span></span>

<span data-ttu-id="8f8b3-122">Il comportamento del filtro dipende dall'ordine delle connessioni pin:</span><span class="sxs-lookup"><span data-stu-id="8f8b3-122">The behavior of the filter depends on the order of the pin connections:</span></span>

-   <span data-ttu-id="8f8b3-123">Se il pin di input è connesso per primo, la connessione usa un allocatore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-123">If the input pin is connected first, the connection uses a temporary allocator.</span></span> <span data-ttu-id="8f8b3-124">Quando il pin di output è connesso, il filtro riconnette il pin di input.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-124">When the output pin is connected, the filter reconnects the input pin.</span></span> <span data-ttu-id="8f8b3-125">Riconnettendo il pin di input, il filtro upstream rinegozia l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-125">Reconnecting the input pin causes the upstream filter to renegotiate the allocator.</span></span> <span data-ttu-id="8f8b3-126">A questo punto, il pin di input propone un allocatore dal filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-126">At that point, the input pin proposes an allocator from the downstream filter.</span></span> <span data-ttu-id="8f8b3-127">Per altre informazioni, vedere [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span><span class="sxs-lookup"><span data-stu-id="8f8b3-127">For more information, see [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span></span>
-   <span data-ttu-id="8f8b3-128">Se il pin di output è connesso per primo, il pin di output non seleziona un allocatore.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-128">If the output pin is connected first, the output pin does not select an allocator.</span></span> <span data-ttu-id="8f8b3-129">Quando il pin di input è connesso, negozia un allocatore per entrambe le connessioni.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-129">When the input pin is connected, it negotiates an allocator for both connections.</span></span> <span data-ttu-id="8f8b3-130">Se i tipi di supporti di input e output non sono uguali, il filtro riconnette il pin di output usando il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-130">If the input and output media types are not the same, the filter reconnects the output pin using the input type.</span></span>

<span data-ttu-id="8f8b3-131">Il filtro esegue tutte le riconnessioni dei pin chiamando il [**metodo CBaseFilter::ReconnectPin.**](cbasefilter-reconnectpin.md)</span><span class="sxs-lookup"><span data-stu-id="8f8b3-131">The filter performs all pin reconnections by calling the [**CBaseFilter::ReconnectPin**](cbasefilter-reconnectpin.md) method.</span></span> <span data-ttu-id="8f8b3-132">Il **metodo ReconnectPin,** a sua volta, chiama il metodo [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) nel gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="8f8b3-132">The **ReconnectPin** method, in turn, calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f8b3-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f8b3-133">Requirements</span></span>



| <span data-ttu-id="8f8b3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f8b3-134">Requirement</span></span> | <span data-ttu-id="8f8b3-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8f8b3-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f8b3-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f8b3-136">Header</span></span><br/>  | <dl> <span data-ttu-id="8f8b3-137"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b3-137"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8f8b3-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="8f8b3-138">Library</span></span><br/> | <dl> <span data-ttu-id="8f8b3-139"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b3-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f8b3-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f8b3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8b3-141">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="8f8b3-141">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




