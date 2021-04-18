---
description: La classe CAMSchedule implementa un'utilità di pianificazione per gli orologi di riferimento.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Classe CAMSchedule (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330549"
---
# <a name="camschedule-class"></a><span data-ttu-id="0999d-103">Classe CAMSchedule</span><span class="sxs-lookup"><span data-stu-id="0999d-103">CAMSchedule class</span></span>

<span data-ttu-id="0999d-104">La `CAMSchedule` classe implementa un'utilità di pianificazione per gli orologi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0999d-104">The `CAMSchedule` class implements a scheduler for reference clocks.</span></span>



| <span data-ttu-id="0999d-105">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="0999d-105">Public Methods</span></span>                                             | <span data-ttu-id="0999d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0999d-106">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0999d-107">**CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="0999d-107">**CAMSchedule**</span></span>](camschedule-camschedule.md)             | <span data-ttu-id="0999d-108">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="0999d-108">Constructor method.</span></span>                                                                  |
| [<span data-ttu-id="0999d-109">**~ CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="0999d-109">**~CAMSchedule**</span></span>](camschedule--camschedule.md)           | <span data-ttu-id="0999d-110">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="0999d-110">Destructor method.</span></span> <span data-ttu-id="0999d-111">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="0999d-111">Virtual.</span></span>                                                          |
| [<span data-ttu-id="0999d-112">**GetAdviseCount**</span><span class="sxs-lookup"><span data-stu-id="0999d-112">**GetAdviseCount**</span></span>](camschedule-getadvisecount.md)       | <span data-ttu-id="0999d-113">Recupera il numero di richieste di notifica in sospeso.</span><span class="sxs-lookup"><span data-stu-id="0999d-113">Retrieves the number of pending advise requests.</span></span>                                     |
| [<span data-ttu-id="0999d-114">**GetNextAdviseTime**</span><span class="sxs-lookup"><span data-stu-id="0999d-114">**GetNextAdviseTime**</span></span>](camschedule-getnextadvisetime.md) | <span data-ttu-id="0999d-115">Recupera l'ora della successiva richiesta di notifica.</span><span class="sxs-lookup"><span data-stu-id="0999d-115">Retrieves the time of the next advise request.</span></span>                                       |
| [<span data-ttu-id="0999d-116">**AddAdvisePacket**</span><span class="sxs-lookup"><span data-stu-id="0999d-116">**AddAdvisePacket**</span></span>](camschedule-addadvisepacket.md)     | <span data-ttu-id="0999d-117">Aggiunge una richiesta di notifica all'elenco di richieste in sospeso.</span><span class="sxs-lookup"><span data-stu-id="0999d-117">Adds an advise request to the list of pending requests.</span></span>                              |
| [<span data-ttu-id="0999d-118">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="0999d-118">**Unadvise**</span></span>](camschedule-unadvise.md)                   | <span data-ttu-id="0999d-119">Rimuove una richiesta di notifica.</span><span class="sxs-lookup"><span data-stu-id="0999d-119">Removes an advise request.</span></span>                                                           |
| [<span data-ttu-id="0999d-120">**Consigliare**</span><span class="sxs-lookup"><span data-stu-id="0999d-120">**Advise**</span></span>](camschedule-advise.md)                       | <span data-ttu-id="0999d-121">Invia tutte le richieste pianificate per un periodo di tempo specificato o una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="0999d-121">Dispatches all requests that are scheduled for a specified time or earlier.</span></span>          |
| [<span data-ttu-id="0999d-122">**GetEvent**</span><span class="sxs-lookup"><span data-stu-id="0999d-122">**GetEvent**</span></span>](camschedule-getevent.md)                   | <span data-ttu-id="0999d-123">Recupera un handle di evento, che viene usato per segnalare una modifica nel tempo di notifica successivo.</span><span class="sxs-lookup"><span data-stu-id="0999d-123">Retrieves an event handle, which is used to signal a change in the next advise time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0999d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0999d-124">Remarks</span></span>

<span data-ttu-id="0999d-125">Questo oggetto helper gestisce un elenco di richieste di notifica per un orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0999d-125">This helper object maintains a list of advise requests for a reference clock.</span></span> <span data-ttu-id="0999d-126">La classe [**CBaseReferenceClock**](cbasereferenceclock.md) la utilizza per pianificare le richieste di notifica.</span><span class="sxs-lookup"><span data-stu-id="0999d-126">The [**CBaseReferenceClock**](cbasereferenceclock.md) class uses it to help schedule advise requests.</span></span> <span data-ttu-id="0999d-127">Gli orologi usano questo oggetto nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="0999d-127">Clocks use this object in the following manner:</span></span>

1.  <span data-ttu-id="0999d-128">Il clock crea un thread di lavoro per gestire la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0999d-128">The clock creates a worker thread to handle scheduling.</span></span>
2.  <span data-ttu-id="0999d-129">Il thread di lavoro chiama il metodo [**CAMSchedule:: GetEvent**](camschedule-getevent.md) per recuperare un handle di evento dall'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0999d-129">The worker thread calls the [**CAMSchedule::GetEvent**](camschedule-getevent.md) method to retrieve an event handle from the scheduler.</span></span> <span data-ttu-id="0999d-130">Attende questo evento, inizialmente con un timeout infinito.</span><span class="sxs-lookup"><span data-stu-id="0999d-130">It waits on this event, initially with an infinite time-out.</span></span>
3.  <span data-ttu-id="0999d-131">Per pianificare una nuova richiesta di notifica, il clock chiama il metodo [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="0999d-131">To schedule a new advise request, the clock calls the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span> <span data-ttu-id="0999d-132">Una richiesta di notifica può essere monofase o periodica.</span><span class="sxs-lookup"><span data-stu-id="0999d-132">An advise request can be one-shot or periodic.</span></span> <span data-ttu-id="0999d-133">L'utilità di pianificazione mantiene l'elenco di richieste in ordine temporale.</span><span class="sxs-lookup"><span data-stu-id="0999d-133">The scheduler keeps the list of requests in time order.</span></span>
4.  <span data-ttu-id="0999d-134">Se una richiesta viene aggiunta all'inizio dell'elenco, l'utilità di pianificazione segnala l'evento.</span><span class="sxs-lookup"><span data-stu-id="0999d-134">If a request is added to the front of the list, the scheduler signals the event.</span></span> <span data-ttu-id="0999d-135">(L'elenco è inizialmente vuoto, quindi la prima richiesta viene garantita per segnalare l'evento).</span><span class="sxs-lookup"><span data-stu-id="0999d-135">(The list is empty at first, so the first request is guaranteed to signal the event.)</span></span>
5.  <span data-ttu-id="0999d-136">Quando l'evento viene segnalato, il thread di lavoro chiama il metodo [**CAMSchedule:: Advise**](camschedule-advise.md) , specificando l'ora di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="0999d-136">When the event is signaled, the worker thread calls the [**CAMSchedule::Advise**](camschedule-advise.md) method, specifying the current reference time.</span></span> <span data-ttu-id="0999d-137">Se sono scadute richieste in sospeso, l'utilità di pianificazione li invia.</span><span class="sxs-lookup"><span data-stu-id="0999d-137">If any pending requests have expired, the scheduler dispatches them.</span></span>
6.  <span data-ttu-id="0999d-138">Il metodo Advise restituisce l'ora della richiesta successiva.</span><span class="sxs-lookup"><span data-stu-id="0999d-138">The Advise method returns the time of the next request.</span></span> <span data-ttu-id="0999d-139">Il thread di lavoro utilizza questo valore per calcolare un nuovo valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="0999d-139">The worker thread uses this value to calculate a new time-out value.</span></span>
7.  <span data-ttu-id="0999d-140">I passaggi 2 6 si ripetono per un periodo illimitato.</span><span class="sxs-lookup"><span data-stu-id="0999d-140">Steps 2 6 repeat indefinitely.</span></span>
8.  <span data-ttu-id="0999d-141">Per terminare il thread di lavoro, il clock imposta un flag interno e segnala l'evento.</span><span class="sxs-lookup"><span data-stu-id="0999d-141">To terminate the worker thread, the clock sets an internal flag and signals the event.</span></span>

<span data-ttu-id="0999d-142">Nel passaggio 2, l'evento viene segnalato o il timeout dell'attesa. Se l'evento viene segnalato, significa che è stata aggiunta una nuova richiesta all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0999d-142">In step 2, either the event is signaled, or the wait times out. If the event is signaled, it means that a new request was added to the front of the list.</span></span> <span data-ttu-id="0999d-143">Il thread di lavoro deve calcolare un nuovo valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="0999d-143">The worker thread must calculate a new time-out value.</span></span> <span data-ttu-id="0999d-144">D'altra parte, se si verifica il timeout dell'attesa, significa che una richiesta di notifica è dovuta e deve essere inviata.</span><span class="sxs-lookup"><span data-stu-id="0999d-144">On the other hand, if the wait times out, it means that an advise request has come due and must be dispatched.</span></span> <span data-ttu-id="0999d-145">La chiamata a advise nel passaggio 5 gestisce entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="0999d-145">The call to Advise in step 5 handles both cases.</span></span>

## <a name="requirements"></a><span data-ttu-id="0999d-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0999d-146">Requirements</span></span>



| <span data-ttu-id="0999d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0999d-147">Requirement</span></span> | <span data-ttu-id="0999d-148">Valore</span><span class="sxs-lookup"><span data-stu-id="0999d-148">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0999d-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0999d-149">Header</span></span><br/>  | <dl> <span data-ttu-id="0999d-150"><dt>Dsschedule. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0999d-150"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="0999d-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="0999d-151">Library</span></span><br/> | <dl> <span data-ttu-id="0999d-152"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0999d-152"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




