---
description: Il metodo StartUsingOutputPin Ottiene l'accesso al pin per un'operazione di flusso.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Metodo CDynamicOutputPin. StartUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332340"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a><span data-ttu-id="ca771-103">CDynamicOutputPin. StartUsingOutputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="ca771-103">CDynamicOutputPin.StartUsingOutputPin method</span></span>

<span data-ttu-id="ca771-104">Il `StartUsingOutputPin` metodo ottiene l'accesso al pin per un'operazione di flusso.</span><span class="sxs-lookup"><span data-stu-id="ca771-104">The `StartUsingOutputPin` method obtains access to the pin for a streaming operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca771-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca771-105">Syntax</span></span>


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="ca771-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca771-106">Parameters</span></span>

<span data-ttu-id="ca771-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ca771-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca771-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca771-108">Return value</span></span>

<span data-ttu-id="ca771-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca771-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ca771-110">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ca771-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ca771-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ca771-111">Return code</span></span>                                                                                           | <span data-ttu-id="ca771-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca771-112">Description</span></span>                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca771-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca771-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="ca771-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ca771-114">Success.</span></span><br/>                                               |
| <dl> <span data-ttu-id="ca771-115"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="ca771-115"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>          | <span data-ttu-id="ca771-116">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ca771-116">Unexpected error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ca771-117"><dt>**stato di VFW \_ E \_ \_ modificato**</dt></span><span class="sxs-lookup"><span data-stu-id="ca771-117"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="ca771-118">Il filtro è stato arrestato o è iniziato lo scaricamento del PIN.</span><span class="sxs-lookup"><span data-stu-id="ca771-118">The filter was stopped, or the pin has begun flushing.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca771-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca771-119">Remarks</span></span>

<span data-ttu-id="ca771-120">Chiamare questo metodo prima di chiamare i metodi che recapitano i dati al pin di input connesso o che modificano il tipo di supporto della connessione.</span><span class="sxs-lookup"><span data-stu-id="ca771-120">Call this method before calling any methods that deliver data to the connected input pin or that change the connection's media type.</span></span> <span data-ttu-id="ca771-121">Questa regola, ad esempio, si applica ai metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca771-121">For example, this rule applies to the following methods:</span></span>

-   [<span data-ttu-id="ca771-122">**CDynamicOutputPin::ChangeOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="ca771-122">**CDynamicOutputPin::ChangeOutputFormat**</span></span>](cdynamicoutputpin-changeoutputformat.md)
-   [<span data-ttu-id="ca771-123">**CDynamicOutputPin::ChangeMediaType**</span><span class="sxs-lookup"><span data-stu-id="ca771-123">**CDynamicOutputPin::ChangeMediaType**</span></span>](cdynamicoutputpin-changemediatype.md)
-   [<span data-ttu-id="ca771-124">**CDynamicOutputPin::D ynamicReconnect**</span><span class="sxs-lookup"><span data-stu-id="ca771-124">**CDynamicOutputPin::DynamicReconnect**</span></span>](cdynamicoutputpin-dynamicreconnect.md)
-   [<span data-ttu-id="ca771-125">**CBaseOutputPin::D Eliver**</span><span class="sxs-lookup"><span data-stu-id="ca771-125">**CBaseOutputPin::Deliver**</span></span>](cbaseoutputpin-deliver.md)
-   [<span data-ttu-id="ca771-126">**CBaseOutputPin::D eliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="ca771-126">**CBaseOutputPin::DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md)
-   [<span data-ttu-id="ca771-127">**CBaseOutputPin::D eliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="ca771-127">**CBaseOutputPin::DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)
-   [<span data-ttu-id="ca771-128">**IMemInputPin:: Receive**</span><span class="sxs-lookup"><span data-stu-id="ca771-128">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="ca771-129">**IMemInputPin:: ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="ca771-129">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="ca771-130">**IPin:: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="ca771-130">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="ca771-131">**IPin:: NewSegment**</span><span class="sxs-lookup"><span data-stu-id="ca771-131">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

<span data-ttu-id="ca771-132">Successivamente, chiamare il metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) per rilasciare l'accesso al pin.</span><span class="sxs-lookup"><span data-stu-id="ca771-132">Afterward, call the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method to release the access to the pin.</span></span>

<span data-ttu-id="ca771-133">Se il PIN è bloccato, `StartUsingOutputPin` attende che il PIN venga sbloccato.</span><span class="sxs-lookup"><span data-stu-id="ca771-133">If the pin is blocked, `StartUsingOutputPin` waits for the pin to become unblocked.</span></span> <span data-ttu-id="ca771-134">Se il filtro si interrompe mentre il metodo è in attesa, il metodo restituisce \_ immediatamente \_ lo stato VFW E \_ modificato.</span><span class="sxs-lookup"><span data-stu-id="ca771-134">If the filter stops while the method is waiting, the method immediately returns VFW\_E\_STATE\_CHANGED.</span></span> <span data-ttu-id="ca771-135">Il pin mantiene un conteggio del numero di volte `StartUsingOutputPin` in cui è stato chiamato senza una chiamata corrispondente a **StopUsingOutputPin**.</span><span class="sxs-lookup"><span data-stu-id="ca771-135">The pin maintains a count of how many times `StartUsingOutputPin` has been called without a corresponding call to **StopUsingOutputPin**.</span></span> <span data-ttu-id="ca771-136">Se un altro thread tenta di bloccare il pin mentre questo conteggio è diverso da zero, il pin imposta lo stato di blocco su "Pending".</span><span class="sxs-lookup"><span data-stu-id="ca771-136">If another thread tries to block the pin while this count is non-zero, the pin sets its blocking status to "pending."</span></span> <span data-ttu-id="ca771-137">Il PIN viene bloccato una volta completate tutte le operazioni di streaming, nella chiamata finale a **StopUsingOutputPin**.</span><span class="sxs-lookup"><span data-stu-id="ca771-137">The pin becomes blocked once all of the streaming operations have completed, in the final call to **StopUsingOutputPin**.</span></span>

<span data-ttu-id="ca771-138">Quando si chiama questo metodo, non è necessario mantenere la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical.</span><span class="sxs-lookup"><span data-stu-id="ca771-138">Do not hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section when you call this method.</span></span> <span data-ttu-id="ca771-139">In caso contrario, se il PIN è bloccato, non può mai essere sbloccato, causando un deadlock.</span><span class="sxs-lookup"><span data-stu-id="ca771-139">Otherwise, if the pin is blocked, it can never become unblocked, causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca771-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca771-140">Requirements</span></span>



| <span data-ttu-id="ca771-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca771-141">Requirement</span></span> | <span data-ttu-id="ca771-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ca771-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca771-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca771-143">Header</span></span><br/>  | <dl> <span data-ttu-id="ca771-144"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca771-144"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca771-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca771-145">Library</span></span><br/> | <dl> <span data-ttu-id="ca771-146"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ca771-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca771-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca771-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca771-148">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="ca771-148">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




