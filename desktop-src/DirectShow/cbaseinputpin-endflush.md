---
description: "Il metodo EndFlush termina un'operazione di svuotamento. Implementa il metodo IPin:: EndFlush."
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Metodo CBaseInputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326067"
---
# <a name="cbaseinputpinendflush-method"></a><span data-ttu-id="8eb72-104">CBaseInputPin. EndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="8eb72-104">CBaseInputPin.EndFlush method</span></span>

<span data-ttu-id="8eb72-105">Il `EndFlush` metodo termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="8eb72-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="8eb72-106">Implementa il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="8eb72-106">Implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb72-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8eb72-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="8eb72-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8eb72-108">Parameters</span></span>

<span data-ttu-id="8eb72-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8eb72-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8eb72-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8eb72-110">Return value</span></span>

<span data-ttu-id="8eb72-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8eb72-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eb72-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8eb72-112">Remarks</span></span>

<span data-ttu-id="8eb72-113">Questo metodo imposta il flag [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) su **true**, che consente al metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) di accettare esempi.</span><span class="sxs-lookup"><span data-stu-id="8eb72-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which enables the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to accept samples.</span></span>

<span data-ttu-id="8eb72-114">La classe derivata deve eseguire l'override di questo metodo ed eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8eb72-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="8eb72-115">Liberare i dati memorizzati nel buffer e attendere che tutti gli esempi in coda vengano eliminati.</span><span class="sxs-lookup"><span data-stu-id="8eb72-115">Free any buffered data and wait for all queued samples to be discarded.</span></span>
2.  <span data-ttu-id="8eb72-116">Cancellare le notifiche [**\_ complete di EC**](ec-complete.md) in sospeso.</span><span class="sxs-lookup"><span data-stu-id="8eb72-116">Clear any pending [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>
3.  <span data-ttu-id="8eb72-117">Chiamare il metodo della classe base.</span><span class="sxs-lookup"><span data-stu-id="8eb72-117">Call the base class method.</span></span>
4.  <span data-ttu-id="8eb72-118">Chiamare [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) nei pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="8eb72-118">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on downstream input pins.</span></span> <span data-ttu-id="8eb72-119">Se il PIN non ha ancora recapitato alcun campione multimediale a valle, è possibile ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="8eb72-119">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="8eb72-120">Se i pin di output derivano dalla classe [**CBaseOutputPin**](cbaseoutputpin.md) , è possibile chiamare il metodo [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="8eb72-120">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb72-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eb72-121">Requirements</span></span>



| <span data-ttu-id="8eb72-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb72-122">Requirement</span></span> | <span data-ttu-id="8eb72-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8eb72-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb72-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8eb72-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8eb72-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8eb72-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8eb72-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="8eb72-126">Library</span></span><br/> | <dl> <span data-ttu-id="8eb72-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8eb72-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eb72-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8eb72-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb72-129">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="8eb72-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




