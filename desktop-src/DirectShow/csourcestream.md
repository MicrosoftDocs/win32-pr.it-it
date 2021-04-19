---
description: La classe CSourceStream fornisce un pin di output per la classe filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Classe CSourceStream (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330288"
---
# <a name="csourcestream-class"></a><span data-ttu-id="4aced-103">Classe CSourceStream</span><span class="sxs-lookup"><span data-stu-id="4aced-103">CSourceStream class</span></span>

![gerarchia di classi csourcestream](images/source02.png)

<span data-ttu-id="4aced-105">La classe **CSourceStream** fornisce un pin di output per la classe filtro [**CSource**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="4aced-105">The **CSourceStream** class provides an output pin for the [**CSource**](csource.md) filter class.</span></span>

<span data-ttu-id="4aced-106">Per informazioni sull'utilizzo di questa classe, vedere [**CSource**](csource.md).</span><span class="sxs-lookup"><span data-stu-id="4aced-106">For information on using this class, see [**CSource**](csource.md).</span></span> <span data-ttu-id="4aced-107">Questa classe eredita la classe [**CAMThread**](camthread.md) , che fornisce un thread di lavoro per lo streaming dei dati dal pin.</span><span class="sxs-lookup"><span data-stu-id="4aced-107">This class inherits the [**CAMThread**](camthread.md) class, which provides a worker thread for streaming data from the pin.</span></span> <span data-ttu-id="4aced-108">La classe **CSourceStream** implementa i seguenti metodi helper per inviare richieste al thread:</span><span class="sxs-lookup"><span data-stu-id="4aced-108">The **CSourceStream** class implements the following helper methods to send requests to the thread:</span></span>

-   [<span data-ttu-id="4aced-109">**CSourceStream:: Exit**</span><span class="sxs-lookup"><span data-stu-id="4aced-109">**CSourceStream::Exit**</span></span>](csourcestream-exit.md)
-   [<span data-ttu-id="4aced-110">**CSourceStream:: init**</span><span class="sxs-lookup"><span data-stu-id="4aced-110">**CSourceStream::Init**</span></span>](csourcestream-init.md)
-   [<span data-ttu-id="4aced-111">**CSourceStream::P ause**</span><span class="sxs-lookup"><span data-stu-id="4aced-111">**CSourceStream::Pause**</span></span>](csourcestream-pause.md)
-   [<span data-ttu-id="4aced-112">**CSourceStream:: Run**</span><span class="sxs-lookup"><span data-stu-id="4aced-112">**CSourceStream::Run**</span></span>](csourcestream-run.md)
-   [<span data-ttu-id="4aced-113">**CSourceStream:: Stop**</span><span class="sxs-lookup"><span data-stu-id="4aced-113">**CSourceStream::Stop**</span></span>](csourcestream-stop.md)

<span data-ttu-id="4aced-114">La prima richiesta al thread deve essere [**init**](csourcestream-init.md).</span><span class="sxs-lookup"><span data-stu-id="4aced-114">The first request to the thread must be [**Init**](csourcestream-init.md).</span></span> <span data-ttu-id="4aced-115">La richiesta di [**uscita**](csourcestream-exit.md) termina il thread.</span><span class="sxs-lookup"><span data-stu-id="4aced-115">The [**Exit**](csourcestream-exit.md) request terminates the thread.</span></span> <span data-ttu-id="4aced-116">In pratica, non è necessario chiamare direttamente uno di questi metodi, perché i metodi [**CSourceStream:: Active**](csourcestream-active.md) e [**CSourceStream:: inactive**](csourcestream-inactive.md) del pin li chiamano in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="4aced-116">In practice, it is not necessary to call any of these methods directly, because the pin's [**CSourceStream::Active**](csourcestream-active.md) and [**CSourceStream::Inactive**](csourcestream-inactive.md) methods call them as needed.</span></span>

<span data-ttu-id="4aced-117">La classe fornisce anche diversi metodi "handler":</span><span class="sxs-lookup"><span data-stu-id="4aced-117">The class also provides several "handler" methods:</span></span>

-   [<span data-ttu-id="4aced-118">**CSourceStream::OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="4aced-118">**CSourceStream::OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)
-   [<span data-ttu-id="4aced-119">**CSourceStream::OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="4aced-119">**CSourceStream::OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)
-   [<span data-ttu-id="4aced-120">**CSourceStream::OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="4aced-120">**CSourceStream::OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)

<span data-ttu-id="4aced-121">Non eseguono alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="4aced-121">These do nothing in the base class, but the derived class can override them.</span></span>



| <span data-ttu-id="4aced-122">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="4aced-122">Protected Member Variables</span></span>                                             | <span data-ttu-id="4aced-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aced-123">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4aced-124">**\_pFilter m**</span><span class="sxs-lookup"><span data-stu-id="4aced-124">**m\_pFilter**</span></span>](csourcestream-m-pfilter.md)                          | <span data-ttu-id="4aced-125">Puntatore al filtro che contiene questo pin.</span><span class="sxs-lookup"><span data-stu-id="4aced-125">Pointer to the filter that contains this pin.</span></span>                                                                                     |
| <span data-ttu-id="4aced-126">Metodi protetti</span><span class="sxs-lookup"><span data-stu-id="4aced-126">Protected Methods</span></span>                                                      | <span data-ttu-id="4aced-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aced-127">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="4aced-128">**OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="4aced-128">**OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)                 | <span data-ttu-id="4aced-129">Chiamato quando viene inizializzato il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="4aced-129">Called when the streaming thread is initialized.</span></span> <span data-ttu-id="4aced-130">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aced-130">Virtual.</span></span>                                                                         |
| [<span data-ttu-id="4aced-131">**OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="4aced-131">**OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)               | <span data-ttu-id="4aced-132">Chiamato quando il thread di streaming sta per uscire.</span><span class="sxs-lookup"><span data-stu-id="4aced-132">Called when the streaming thread is about to exit.</span></span> <span data-ttu-id="4aced-133">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aced-133">Virtual.</span></span>                                                                       |
| [<span data-ttu-id="4aced-134">**OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="4aced-134">**OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)           | <span data-ttu-id="4aced-135">Chiamato all'inizio del metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="4aced-135">Called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="4aced-136">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aced-136">Virtual.</span></span> |
| [<span data-ttu-id="4aced-137">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="4aced-137">**Active**</span></span>](csourcestream-active.md)                                 | <span data-ttu-id="4aced-138">Notifica al pin che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="4aced-138">Notifies the pin that the filter is now active.</span></span>                                                                                   |
| [<span data-ttu-id="4aced-139">**Inattivo**</span><span class="sxs-lookup"><span data-stu-id="4aced-139">**Inactive**</span></span>](csourcestream-inactive.md)                             | <span data-ttu-id="4aced-140">Notifica al pin che il filtro non è più attivo.</span><span class="sxs-lookup"><span data-stu-id="4aced-140">Notifies the pin that the filter is no longer active.</span></span>                                                                             |
| [<span data-ttu-id="4aced-141">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="4aced-141">**GetRequest**</span></span>](csourcestream-getrequest.md)                         | <span data-ttu-id="4aced-142">Attende la richiesta successiva del thread.</span><span class="sxs-lookup"><span data-stu-id="4aced-142">Waits for the next thread request.</span></span>                                                                                                |
| [<span data-ttu-id="4aced-143">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="4aced-143">**CheckRequest**</span></span>](csourcestream-checkrequest.md)                     | <span data-ttu-id="4aced-144">Verifica se è presente una richiesta di thread senza blocco.</span><span class="sxs-lookup"><span data-stu-id="4aced-144">Checks if there is a thread request, without blocking.</span></span>                                                                            |
| [<span data-ttu-id="4aced-145">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="4aced-145">**ThreadProc**</span></span>](csourcestream-threadproc.md)                         | <span data-ttu-id="4aced-146">Routine thread.</span><span class="sxs-lookup"><span data-stu-id="4aced-146">Thread procedure.</span></span> <span data-ttu-id="4aced-147">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aced-147">Virtual.</span></span>                                                                                                        |
| [<span data-ttu-id="4aced-148">**DoBufferProcessingLoop**</span><span class="sxs-lookup"><span data-stu-id="4aced-148">**DoBufferProcessingLoop**</span></span>](csourcestream-dobufferprocessingloop.md) | <span data-ttu-id="4aced-149">Genera i dati multimediali e li recapita al pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="4aced-149">Generates media data and delivers it to the downstream input pin.</span></span> <span data-ttu-id="4aced-150">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aced-150">Virtual.</span></span>                                                        |
| [<span data-ttu-id="4aced-151">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="4aced-151">**CheckMediaType**</span></span>](csourcestream-checkmediatype.md)                 | <span data-ttu-id="4aced-152">Determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="4aced-152">Determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="4aced-153">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aced-153">Virtual.</span></span>                                                                     |
| [<span data-ttu-id="4aced-154">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="4aced-154">**GetMediaType**</span></span>](csourcestream-getmediatype.md)                     | <span data-ttu-id="4aced-155">Recupera un tipo di supporto preferito.</span><span class="sxs-lookup"><span data-stu-id="4aced-155">Retrieves a preferred media type.</span></span> <span data-ttu-id="4aced-156">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aced-156">Virtual.</span></span>                                                                                        |
| <span data-ttu-id="4aced-157">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="4aced-157">Public Methods</span></span>                                                         | <span data-ttu-id="4aced-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aced-158">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="4aced-159">**CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="4aced-159">**CSourceStream**</span></span>](csourcestream-csourcestream.md)                   | <span data-ttu-id="4aced-160">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="4aced-160">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="4aced-161">**~ CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="4aced-161">**~ CSourceStream**</span></span>](csourcestream--csourcestream.md)                | <span data-ttu-id="4aced-162">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="4aced-162">Destructor method.</span></span> <span data-ttu-id="4aced-163">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aced-163">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="4aced-164">**Init**</span><span class="sxs-lookup"><span data-stu-id="4aced-164">**Init**</span></span>](csourcestream-init.md)                                     | <span data-ttu-id="4aced-165">Inizializza il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="4aced-165">Initializes the streaming thread.</span></span>                                                                                                 |
| [<span data-ttu-id="4aced-166">**Esci**</span><span class="sxs-lookup"><span data-stu-id="4aced-166">**Exit**</span></span>](csourcestream-exit.md)                                     | <span data-ttu-id="4aced-167">Segnala al thread di streaming di uscire.</span><span class="sxs-lookup"><span data-stu-id="4aced-167">Signals the streaming thread to exit.</span></span>                                                                                             |
| [<span data-ttu-id="4aced-168">**Correre**</span><span class="sxs-lookup"><span data-stu-id="4aced-168">**Run**</span></span>](csourcestream-run.md)                                       | <span data-ttu-id="4aced-169">Segnala l'esecuzione del thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="4aced-169">Signals the streaming thread to run.</span></span>                                                                                              |
| [<span data-ttu-id="4aced-170">**Sospendere**</span><span class="sxs-lookup"><span data-stu-id="4aced-170">**Pause**</span></span>](csourcestream-pause.md)                                   | <span data-ttu-id="4aced-171">Segnala al thread di streaming che diventa attivo.</span><span class="sxs-lookup"><span data-stu-id="4aced-171">Signals the streaming thread to become active.</span></span>                                                                                    |
| [<span data-ttu-id="4aced-172">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="4aced-172">**Stop**</span></span>](csourcestream-stop.md)                                     | <span data-ttu-id="4aced-173">Segnala al thread di streaming di arrestarsi.</span><span class="sxs-lookup"><span data-stu-id="4aced-173">Signals the streaming thread to stop.</span></span>                                                                                             |
| <span data-ttu-id="4aced-174">Metodi virtuali puri</span><span class="sxs-lookup"><span data-stu-id="4aced-174">Pure Virtual Methods</span></span>                                                   | <span data-ttu-id="4aced-175">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aced-175">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="4aced-176">**FillBuffer**</span><span class="sxs-lookup"><span data-stu-id="4aced-176">**FillBuffer**</span></span>](csourcestream-fillbuffer.md)                         | <span data-ttu-id="4aced-177">Compila un esempio multimediale con i dati.</span><span class="sxs-lookup"><span data-stu-id="4aced-177">Fills a media sample with data.</span></span>                                                                                                   |
| <span data-ttu-id="4aced-178">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="4aced-178">IPin Methods</span></span>                                                           | <span data-ttu-id="4aced-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aced-179">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="4aced-180">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="4aced-180">**QueryId**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | <span data-ttu-id="4aced-181">Recupera un identificatore per il PIN.</span><span class="sxs-lookup"><span data-stu-id="4aced-181">Retrieves an identifier for the pin.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="4aced-182">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4aced-182">Requirements</span></span>



| <span data-ttu-id="4aced-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aced-183">Requirement</span></span> | <span data-ttu-id="4aced-184">Valore</span><span class="sxs-lookup"><span data-stu-id="4aced-184">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aced-185">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4aced-185">Header</span></span><br/>  | <dl> <span data-ttu-id="4aced-186"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4aced-186"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4aced-187">Libreria</span><span class="sxs-lookup"><span data-stu-id="4aced-187">Library</span></span><br/> | <dl> <span data-ttu-id="4aced-188"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4aced-188"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aced-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4aced-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aced-190">Scrittura di filtri di origine</span><span class="sxs-lookup"><span data-stu-id="4aced-190">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




