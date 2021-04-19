---
description: La classe CSourceSeeking è una classe astratta per l'implementazione della ricerca nei filtri di origine con un pin di output.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: Classe CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329043"
---
# <a name="csourceseeking-class"></a><span data-ttu-id="6c484-103">Classe CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="6c484-103">CSourceSeeking class</span></span>

![gerarchia di classi csourceseeking](images/cutil15.png)

<span data-ttu-id="6c484-105">La classe **CSourceSeeking** è una classe astratta per l'implementazione della ricerca nei filtri di origine con un pin di output.</span><span class="sxs-lookup"><span data-stu-id="6c484-105">The **CSourceSeeking** class is an abstract class for implementing seeking in source filters with one output pin.</span></span>

<span data-ttu-id="6c484-106">Questa classe supporta l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="6c484-106">This class supports the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="6c484-107">Fornisce le implementazioni predefinite per tutti i metodi **IMediaSeeking** .</span><span class="sxs-lookup"><span data-stu-id="6c484-107">It provides default implementations for all of the **IMediaSeeking** methods.</span></span> <span data-ttu-id="6c484-108">Le variabili membro protette memorizzano l'ora di inizio, l'ora di arresto e la frequenza corrente.</span><span class="sxs-lookup"><span data-stu-id="6c484-108">Protected member variables store the start time, stop time, and current rate.</span></span> <span data-ttu-id="6c484-109">Per impostazione predefinita, l'unico formato di ora supportato dalla classe **è \_ \_ Time Format Media \_ time** (unità di 100-nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="6c484-109">By default, the only time format supported by the class is **TIME\_FORMAT\_MEDIA\_TIME** (100-nanosecond units).</span></span> <span data-ttu-id="6c484-110">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="6c484-110">See Remarks for more information.</span></span>



| <span data-ttu-id="6c484-111">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="6c484-111">Protected Member Variables</span></span>                                          | <span data-ttu-id="6c484-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c484-112">Description</span></span>                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c484-113">**\_rtDuration m**</span><span class="sxs-lookup"><span data-stu-id="6c484-113">**m\_rtDuration**</span></span>](csourceseeking-m-rtduration.md)                | <span data-ttu-id="6c484-114">Durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="6c484-114">Duration of the stream.</span></span>                                                                     |
| [<span data-ttu-id="6c484-115">**\_rtStart m**</span><span class="sxs-lookup"><span data-stu-id="6c484-115">**m\_rtStart**</span></span>](csourceseeking-m-rtstart.md)                      | <span data-ttu-id="6c484-116">Ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="6c484-116">Start time.</span></span>                                                                                 |
| [<span data-ttu-id="6c484-117">**\_rtStop m**</span><span class="sxs-lookup"><span data-stu-id="6c484-117">**m\_rtStop**</span></span>](csourceseeking-m-rtstop.md)                        | <span data-ttu-id="6c484-118">Ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="6c484-118">Stop time.</span></span>                                                                                  |
| [<span data-ttu-id="6c484-119">**\_dRateSeeking m**</span><span class="sxs-lookup"><span data-stu-id="6c484-119">**m\_dRateSeeking**</span></span>](csourceseeking-m-drateseeking.md)            | <span data-ttu-id="6c484-120">Velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6c484-120">Playback rate.</span></span>                                                                              |
| [<span data-ttu-id="6c484-121">**\_dwSeekingCaps m**</span><span class="sxs-lookup"><span data-stu-id="6c484-121">**m\_dwSeekingCaps**</span></span>](csourceseeking-m-dwseekingcaps.md)          | <span data-ttu-id="6c484-122">Funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="6c484-122">Seeking capabilities.</span></span>                                                                       |
| [<span data-ttu-id="6c484-123">**\_pLock m**</span><span class="sxs-lookup"><span data-stu-id="6c484-123">**m\_pLock**</span></span>](csourceseeking-m-plock.md)                          | <span data-ttu-id="6c484-124">Puntatore a un oggetto sezione critica per il blocco.</span><span class="sxs-lookup"><span data-stu-id="6c484-124">Pointer to a critical section object for locking.</span></span>                                           |
| <span data-ttu-id="6c484-125">Metodi protetti</span><span class="sxs-lookup"><span data-stu-id="6c484-125">Protected Methods</span></span>                                                   | <span data-ttu-id="6c484-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c484-126">Description</span></span>                                                                                 |
| [<span data-ttu-id="6c484-127">**CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="6c484-127">**CSourceSeeking**</span></span>](csourceseeking-csourceseeking.md)             | <span data-ttu-id="6c484-128">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="6c484-128">Constructor method.</span></span>                                                                         |
| <span data-ttu-id="6c484-129">Metodi virtuali puri</span><span class="sxs-lookup"><span data-stu-id="6c484-129">Pure Virtual Methods</span></span>                                                | <span data-ttu-id="6c484-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c484-130">Description</span></span>                                                                                 |
| [<span data-ttu-id="6c484-131">**Modificatore**</span><span class="sxs-lookup"><span data-stu-id="6c484-131">**ChangeRate**</span></span>](csourceseeking-changerate.md)                     | <span data-ttu-id="6c484-132">Chiamato quando cambia la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6c484-132">Called when the playback rate changes.</span></span>                                                      |
| [<span data-ttu-id="6c484-133">**Iniziale**</span><span class="sxs-lookup"><span data-stu-id="6c484-133">**ChangeStart**</span></span>](csourceseeking-changestart.md)                   | <span data-ttu-id="6c484-134">Chiamato quando cambia la posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="6c484-134">Called when the start position changes.</span></span>                                                     |
| [<span data-ttu-id="6c484-135">**ChangeStop**</span><span class="sxs-lookup"><span data-stu-id="6c484-135">**ChangeStop**</span></span>](csourceseeking-changestop.md)                     | <span data-ttu-id="6c484-136">Chiamato quando cambia la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="6c484-136">Called when the stop position changes.</span></span>                                                      |
| <span data-ttu-id="6c484-137">Metodi IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="6c484-137">IMediaSeeking Methods</span></span>                                               | <span data-ttu-id="6c484-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c484-138">Description</span></span>                                                                                 |
| [<span data-ttu-id="6c484-139">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="6c484-139">**IsFormatSupported**</span></span>](csourceseeking-isformatsupported.md)       | <span data-ttu-id="6c484-140">Determina se è supportato un formato di ora specificato.</span><span class="sxs-lookup"><span data-stu-id="6c484-140">Determines whether a specified time format is supported.</span></span>                                    |
| [<span data-ttu-id="6c484-141">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-141">**QueryPreferredFormat**</span></span>](csourceseeking-querypreferredformat.md) | <span data-ttu-id="6c484-142">Recupera il formato di ora preferito dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c484-142">Retrieves the object's preferred time format.</span></span>                                               |
| [<span data-ttu-id="6c484-143">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-143">**SetTimeFormat**</span></span>](csourceseeking-settimeformat.md)               | <span data-ttu-id="6c484-144">Imposta il formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="6c484-144">Sets the time format.</span></span>                                                                       |
| [<span data-ttu-id="6c484-145">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-145">**IsUsingTimeFormat**</span></span>](csourceseeking-isusingtimeformat.md)       | <span data-ttu-id="6c484-146">Determina se un formato di ora specificato è il formato attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="6c484-146">Determines whether a specified time format is the format currently in use.</span></span>                  |
| [<span data-ttu-id="6c484-147">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-147">**GetTimeFormat**</span></span>](csourceseeking-gettimeformat.md)               | <span data-ttu-id="6c484-148">Recupera il formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="6c484-148">Retrieves the current time format.</span></span>                                                          |
| [<span data-ttu-id="6c484-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="6c484-149">**GetDuration**</span></span>](csourceseeking-getduration.md)                   | <span data-ttu-id="6c484-150">Recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="6c484-150">Retrieves the duration of the stream.</span></span>                                                       |
| [<span data-ttu-id="6c484-151">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="6c484-151">**GetStopPosition**</span></span>](csourceseeking-getstopposition.md)           | <span data-ttu-id="6c484-152">Recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="6c484-152">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> |
| [<span data-ttu-id="6c484-153">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="6c484-153">**GetCurrentPosition**</span></span>](csourceseeking-getcurrentposition.md)     | <span data-ttu-id="6c484-154">Recupera la posizione corrente rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="6c484-154">Retrieves the current position, relative to the total duration of the stream.</span></span>               |
| [<span data-ttu-id="6c484-155">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6c484-155">**GetCapabilities**</span></span>](csourceseeking-getcapabilities.md)           | <span data-ttu-id="6c484-156">Recupera tutte le funzionalità di ricerca del flusso.</span><span class="sxs-lookup"><span data-stu-id="6c484-156">Retrieves all the seeking capabilities of the stream.</span></span>                                       |
| [<span data-ttu-id="6c484-157">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6c484-157">**CheckCapabilities**</span></span>](csourceseeking-checkcapabilities.md)       | <span data-ttu-id="6c484-158">Esegue una query se il flusso ha specificato funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="6c484-158">Queries whether the stream has specified seeking capabilities.</span></span>                              |
| [<span data-ttu-id="6c484-159">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-159">**ConvertTimeFormat**</span></span>](csourceseeking-converttimeformat.md)       | <span data-ttu-id="6c484-160">Esegue la conversione da un formato di ora a un altro.</span><span class="sxs-lookup"><span data-stu-id="6c484-160">Converts from one time format to another.</span></span>                                                   |
| [<span data-ttu-id="6c484-161">**Posizioni**</span><span class="sxs-lookup"><span data-stu-id="6c484-161">**SetPositions**</span></span>](csourceseeking-setpositions.md)                 | <span data-ttu-id="6c484-162">Imposta la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="6c484-162">Sets the current position and the stop position.</span></span>                                            |
| [<span data-ttu-id="6c484-163">**GetPositions**</span><span class="sxs-lookup"><span data-stu-id="6c484-163">**GetPositions**</span></span>](csourceseeking-getpositions.md)                 | <span data-ttu-id="6c484-164">Recupera la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="6c484-164">Retrieves the current position and the stop position.</span></span>                                       |
| [<span data-ttu-id="6c484-165">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="6c484-165">**GetAvailable**</span></span>](csourceseeking-getavailable.md)                 | <span data-ttu-id="6c484-166">Recupera l'intervallo di tempo in cui la ricerca è efficiente.</span><span class="sxs-lookup"><span data-stu-id="6c484-166">Retrieves the range of times in which seeking is efficient.</span></span>                                 |
| [<span data-ttu-id="6c484-167">**Frequenza**</span><span class="sxs-lookup"><span data-stu-id="6c484-167">**SetRate**</span></span>](csourceseeking-setrate.md)                           | <span data-ttu-id="6c484-168">Imposta la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6c484-168">Sets the playback rate.</span></span>                                                                     |
| [<span data-ttu-id="6c484-169">**Getrate**</span><span class="sxs-lookup"><span data-stu-id="6c484-169">**GetRate**</span></span>](csourceseeking-getrate.md)                           | <span data-ttu-id="6c484-170">Recupera la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6c484-170">Retrieves the playback rate.</span></span>                                                                |
| [<span data-ttu-id="6c484-171">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="6c484-171">**GetPreroll**</span></span>](csourceseeking-getpreroll.md)                     | <span data-ttu-id="6c484-172">Recupera l'ora di preregistrazione.</span><span class="sxs-lookup"><span data-stu-id="6c484-172">Retrieves the preroll time.</span></span>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="6c484-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c484-173">Remarks</span></span>

<span data-ttu-id="6c484-174">Ogni volta che viene modificata la posizione iniziale, la posizione di arresto o la frequenza di riproduzione, l'oggetto **CSourceSeeking** chiama un metodo virtuale puro corrispondente:</span><span class="sxs-lookup"><span data-stu-id="6c484-174">Whenever the start position, stop position, or playback rate changes, the **CSourceSeeking** object calls a corresponding pure virtual method:</span></span>

-   <span data-ttu-id="6c484-175">Posizione iniziale: [ **CSourceSeeking:: iniziale**](csourceseeking-changestart.md)</span><span class="sxs-lookup"><span data-stu-id="6c484-175">Start position: [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)</span></span>
-   <span data-ttu-id="6c484-176">Posizione stop: [ **CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md)</span><span class="sxs-lookup"><span data-stu-id="6c484-176">Stop position: [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)</span></span>
-   <span data-ttu-id="6c484-177">Velocità di riproduzione: [ **CSourceSeeking:: Changer**](csourceseeking-changerate.md)</span><span class="sxs-lookup"><span data-stu-id="6c484-177">Playback rate: [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)</span></span>

<span data-ttu-id="6c484-178">La classe derivata deve implementare questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6c484-178">The derived class must implement these methods.</span></span> <span data-ttu-id="6c484-179">Dopo qualsiasi operazione di ricerca, un filtro deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c484-179">After any seek operation, a filter must do the following:</span></span>

1.  <span data-ttu-id="6c484-180">Chiamare il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="6c484-180">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the downstream input pin.</span></span>
2.  <span data-ttu-id="6c484-181">Arrestare il thread di lavoro che fornisce i dati.</span><span class="sxs-lookup"><span data-stu-id="6c484-181">Halt the worker thread that is delivering data.</span></span>
3.  <span data-ttu-id="6c484-182">Chiamare il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="6c484-182">Call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>
4.  <span data-ttu-id="6c484-183">Riavviare il thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6c484-183">Restart the worker thread.</span></span>
5.  <span data-ttu-id="6c484-184">Chiamare il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="6c484-184">Call the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>
6.  <span data-ttu-id="6c484-185">Impostare la proprietà discontinuità nel primo esempio.</span><span class="sxs-lookup"><span data-stu-id="6c484-185">Set the discontinuity property on the first sample.</span></span> <span data-ttu-id="6c484-186">Chiamare il metodo [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="6c484-186">Call the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="6c484-187">La chiamata a [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) libera il thread di lavoro, se il thread è bloccato in attesa di recapitare un campione.</span><span class="sxs-lookup"><span data-stu-id="6c484-187">The call to [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) frees the worker thread, if the thread is blocked waiting to deliver a sample.</span></span>

<span data-ttu-id="6c484-188">Nel passaggio 2, verificare che il thread abbia interrotto l'invio dei dati.</span><span class="sxs-lookup"><span data-stu-id="6c484-188">In step 2, make sure that the thread has stopped sending data.</span></span> <span data-ttu-id="6c484-189">A seconda dell'implementazione, potrebbe essere necessario attendere che il thread venga chiuso o che il thread segnali una risposta di qualche tipo.</span><span class="sxs-lookup"><span data-stu-id="6c484-189">Depending on the implementation, you might need to wait for the thread to exit, or for the thread to signal a response of some kind.</span></span> <span data-ttu-id="6c484-190">Se il filtro usa la classe [**CSourceStream**](csourcestream.md) , il metodo [**CSourceStream:: Stop**](csourcestream-stop.md) si blocca fino a quando il thread di lavoro non risponde.</span><span class="sxs-lookup"><span data-stu-id="6c484-190">If your filter uses the [**CSourceStream**](csourcestream.md) class, the [**CSourceStream::Stop**](csourcestream-stop.md) method blocks until the worker thread replies.</span></span>

<span data-ttu-id="6c484-191">Idealmente, il nuovo segmento (passaggio 5) deve essere recapitato dal thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6c484-191">Ideally, the new segment (step 5) should be delivered from the worker thread.</span></span> <span data-ttu-id="6c484-192">Può anche essere eseguita dall'oggetto **CSourceSeeking** , purché il filtro lo serializza con gli esempi.</span><span class="sxs-lookup"><span data-stu-id="6c484-192">It can also be done by the **CSourceSeeking** object, as long as the filter serializes it with the samples.</span></span>

<span data-ttu-id="6c484-193">Nell'esempio seguente viene illustrata una possibile implementazione di.</span><span class="sxs-lookup"><span data-stu-id="6c484-193">The following example shows a possible implementation.</span></span> <span data-ttu-id="6c484-194">Si presuppone che il pin di output del filtro di origine sia derivato da **CSourceSeeking** e [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="6c484-194">It assumes that the source filter's output pin is derived from **CSourceSeeking** and [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="6c484-195">Questo esempio definisce un metodo helper, UpdateFromSeek, che esegue i passaggi 1 4.</span><span class="sxs-lookup"><span data-stu-id="6c484-195">This example defines a helper method, UpdateFromSeek, that performs steps 1 4.</span></span> <span data-ttu-id="6c484-196">Viene eseguito l'override del metodo [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) per inviare il nuovo segmento e impostare un flag che indica la discontinuità.</span><span class="sxs-lookup"><span data-stu-id="6c484-196">The [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method is overridden to send the new segment, and to set a flag indicating the discontinuity.</span></span> <span data-ttu-id="6c484-197">Il thread di lavoro preleva questo flag e chiama il metodo [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :</span><span class="sxs-lookup"><span data-stu-id="6c484-197">The worker thread picks up this flag and calls the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method:</span></span>


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a><span data-ttu-id="6c484-198">Supporto di formati di ora aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="6c484-198">Supporting Additional Time Formats</span></span>

<span data-ttu-id="6c484-199">Per impostazione predefinita, questa classe supporta la ricerca solo in unità di tempo di riferimento (tempo di supporto per il formato dell'ora \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="6c484-199">By default, this class supports seeking only in units of reference time (TIME\_FORMAT\_MEDIA\_TIME).</span></span> <span data-ttu-id="6c484-200">Per supportare formati di ora aggiuntivi, eseguire l'override dei metodi [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) che gestiscono i formati di ora:</span><span class="sxs-lookup"><span data-stu-id="6c484-200">To support additional time formats, override the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods that deal with time formats:</span></span>

-   [<span data-ttu-id="6c484-201">**IMediaSeeking:: GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-201">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="6c484-202">**IMediaSeeking:: GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-202">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="6c484-203">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-203">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="6c484-204">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-204">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="6c484-205">**IMediaSeeking::SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6c484-205">**IMediaSeeking::SetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

<span data-ttu-id="6c484-206">Inoltre, eseguire l'override dei metodi [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) rimanenti per eseguire le conversioni necessarie tra i formati di ora.</span><span class="sxs-lookup"><span data-stu-id="6c484-206">In addition, override the remaining [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods to perform the necessary conversions between time formats.</span></span> <span data-ttu-id="6c484-207">Dopo la chiamata del metodo [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) , tutti i metodi **IMediaSeeking** devono considerare i parametri temporali in entrata e in uscita come nel nuovo formato di ora.</span><span class="sxs-lookup"><span data-stu-id="6c484-207">After the [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method is called, all **IMediaSeeking** methods must treat incoming and outgoing time parameters as being in the new time format.</span></span> <span data-ttu-id="6c484-208">Se, ad esempio, la variabile *m \_ rtDuration* rappresenta la durata in unità di tempo di riferimento, ma il formato dell'ora corrente è frames, il metodo [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) deve restituire il valore *m \_ rtDuration* convertito in frame.</span><span class="sxs-lookup"><span data-stu-id="6c484-208">For example, if the *m\_rtDuration* variable represents the duration in units of reference time, but the current time format is frames, then the [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method must return the value *m\_rtDuration* converted to frames.</span></span> <span data-ttu-id="6c484-209">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6c484-209">For example:</span></span>


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



<span data-ttu-id="6c484-210">Assicurarsi inoltre di verificare la presenza del \_ \_ flag ReturnTime seeking nel metodo [**IMediaSeeking:: sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="6c484-210">Also, make sure to check for the AM\_SEEKING\_ReturnTime flag in the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span> <span data-ttu-id="6c484-211">Se questo flag è presente, convertire i valori di posizione in tempi di riferimento quando vengono restituiti al chiamante.</span><span class="sxs-lookup"><span data-stu-id="6c484-211">If this flag is present, convert the position values into reference times when you return them to the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c484-212">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c484-212">Requirements</span></span>



| <span data-ttu-id="6c484-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c484-213">Requirement</span></span> | <span data-ttu-id="6c484-214">Valore</span><span class="sxs-lookup"><span data-stu-id="6c484-214">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c484-215">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c484-215">Header</span></span><br/>  | <dl> <span data-ttu-id="6c484-216"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c484-216"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c484-217">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c484-217">Library</span></span><br/> | <dl> <span data-ttu-id="6c484-218"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6c484-218"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c484-219">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c484-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c484-220">Supporto della ricerca in un filtro di origine</span><span class="sxs-lookup"><span data-stu-id="6c484-220">Supporting Seeking in a Source Filter</span></span>](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




