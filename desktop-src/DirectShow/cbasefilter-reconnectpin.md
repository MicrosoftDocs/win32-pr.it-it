---
description: Il metodo ReconnectPin interrompe una connessione al PIN esistente e la riconnette allo stesso pin, usando un tipo di supporto specificato.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Metodo CBaseFilter. ReconnectPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324278"
---
# <a name="cbasefilterreconnectpin-method"></a><span data-ttu-id="2b661-103">CBaseFilter. ReconnectPin, metodo</span><span class="sxs-lookup"><span data-stu-id="2b661-103">CBaseFilter.ReconnectPin method</span></span>

<span data-ttu-id="2b661-104">Il `ReconnectPin` metodo interrompe una connessione al PIN esistente e la riconnette allo stesso pin, usando un tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="2b661-104">The `ReconnectPin` method breaks an existing pin connection and reconnects it to the same pin, using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b661-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b661-105">Syntax</span></span>


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2b661-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b661-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b661-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="2b661-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2b661-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="2b661-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2b661-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="2b661-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2b661-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto o **null**.</span><span class="sxs-lookup"><span data-stu-id="2b661-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b661-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b661-111">Return value</span></span>

<span data-ttu-id="2b661-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b661-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2b661-113">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2b661-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="2b661-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2b661-114">Return code</span></span>                                                                                   | <span data-ttu-id="2b661-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b661-115">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b661-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b661-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2b661-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2b661-117">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="2b661-118"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="2b661-118"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="2b661-119">la variabile membro [**\_ pGraph m**](cbasefilter-m-pgraph.md) è **null**.</span><span class="sxs-lookup"><span data-stu-id="2b661-119">[**m\_pGraph**](cbasefilter-m-pgraph.md) member variable is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b661-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b661-120">Remarks</span></span>

<span data-ttu-id="2b661-121">Questo metodo chiama il metodo [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) in gestione grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="2b661-121">This method calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span> <span data-ttu-id="2b661-122">Se l'interfaccia [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) non è disponibile, il metodo chiama [**IFilterGraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span><span class="sxs-lookup"><span data-stu-id="2b661-122">If the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface is not available, the method calls [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b661-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b661-123">Requirements</span></span>



| <span data-ttu-id="2b661-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b661-124">Requirement</span></span> | <span data-ttu-id="2b661-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2b661-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b661-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b661-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2b661-127"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b661-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2b661-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="2b661-128">Library</span></span><br/> | <dl> <span data-ttu-id="2b661-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2b661-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b661-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b661-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b661-131">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="2b661-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




