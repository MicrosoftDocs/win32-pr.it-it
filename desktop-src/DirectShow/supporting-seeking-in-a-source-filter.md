---
description: Questo argomento descrive come implementare la ricerca in un filtro origine Microsoft DirectShow. Usa l'esempio di filtro palla come punto di partenza e descrive il codice aggiuntivo necessario per supportare la ricerca in questo filtro.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Supporto della ricerca in un filtro di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885165"
---
# <a name="supporting-seeking-in-a-source-filter"></a><span data-ttu-id="48e62-104">Supporto della ricerca in un filtro di origine</span><span class="sxs-lookup"><span data-stu-id="48e62-104">Supporting Seeking in a Source Filter</span></span>

<span data-ttu-id="48e62-105">Questo argomento descrive come implementare la ricerca in un filtro origine Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="48e62-105">This topic describes how to implement seeking in a Microsoft DirectShow source filter.</span></span> <span data-ttu-id="48e62-106">Usa l'esempio di [filtro palla](ball-filter-sample.md) come punto di partenza e descrive il codice aggiuntivo necessario per supportare la ricerca in questo filtro.</span><span class="sxs-lookup"><span data-stu-id="48e62-106">It uses the [Ball Filter](ball-filter-sample.md) sample as the starting point and describes the additional code needed to support seeking in this filter.</span></span>

<span data-ttu-id="48e62-107">L'esempio di [filtro palla](ball-filter-sample.md) è un filtro di origine che consente di creare una palla da rimbalzo animata.</span><span class="sxs-lookup"><span data-stu-id="48e62-107">The [Ball Filter](ball-filter-sample.md) sample is a source filter that creates an animated bouncing ball.</span></span> <span data-ttu-id="48e62-108">Questo articolo descrive come aggiungere la funzionalità di ricerca a questo filtro.</span><span class="sxs-lookup"><span data-stu-id="48e62-108">This article describes how to add seeking functionality to this filter.</span></span> <span data-ttu-id="48e62-109">Una volta aggiunta questa funzionalità, è possibile eseguire il rendering del filtro in GraphEdit e controllare la palla trascinando il dispositivo di scorrimento GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="48e62-109">Once you have added this functionality, you can render the filter in GraphEdit and control the ball by dragging the GraphEdit slider.</span></span>

<span data-ttu-id="48e62-110">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="48e62-110">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="48e62-111">Panoramica della ricerca in DirectShow</span><span class="sxs-lookup"><span data-stu-id="48e62-111">Overview of Seeking in DirectShow</span></span>](#overview-of-seeking-in-directshow)
-   [<span data-ttu-id="48e62-112">Panoramica rapida del filtro palla</span><span class="sxs-lookup"><span data-stu-id="48e62-112">Quick Overview of the Ball Filter</span></span>](#quick-overview-of-the-ball-filter)
-   [<span data-ttu-id="48e62-113">Modifica del filtro palla per la ricerca</span><span class="sxs-lookup"><span data-stu-id="48e62-113">Modifying the Ball Filter for Seeking</span></span>](#modifying-the-ball-filter-for-seeking)
-   [<span data-ttu-id="48e62-114">Limitazioni della classe CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="48e62-114">Limitations of the CSourceSeeking Class</span></span>](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a><span data-ttu-id="48e62-115">Panoramica della ricerca in DirectShow</span><span class="sxs-lookup"><span data-stu-id="48e62-115">Overview of Seeking in DirectShow</span></span>

<span data-ttu-id="48e62-116">Un'applicazione cerca il grafico di filtro chiamando un metodo [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) su Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="48e62-116">An application seeks the filter graph by calling an [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) method on the Filter Graph Manager.</span></span> <span data-ttu-id="48e62-117">Il gestore del grafico dei filtri distribuisce quindi la chiamata a ogni renderer nel grafico.</span><span class="sxs-lookup"><span data-stu-id="48e62-117">The Filter Graph Manager then distributes the call to every renderer in the graph.</span></span> <span data-ttu-id="48e62-118">Ogni renderer Invia la chiamata upstream, tramite il pin di output del filtro upstream successivo.</span><span class="sxs-lookup"><span data-stu-id="48e62-118">Each renderer sends the call upstream, through the output pin of the next upstream filter.</span></span> <span data-ttu-id="48e62-119">La chiamata passa a upstream fino a quando non raggiunge un filtro in grado di eseguire il comando seek, in genere un filtro di origine o un filtro del parser.</span><span class="sxs-lookup"><span data-stu-id="48e62-119">The call travels upstream until it reaches a filter that can execute the seek command, typically a source filter or a parser filter.</span></span> <span data-ttu-id="48e62-120">In generale, il filtro che origina i timestamp gestisce anche la ricerca.</span><span class="sxs-lookup"><span data-stu-id="48e62-120">In general, the filter that originates the time stamps also handles seeking.</span></span>

<span data-ttu-id="48e62-121">Un filtro risponde a un comando seek come segue:</span><span class="sxs-lookup"><span data-stu-id="48e62-121">A filter responds to a seek command as follows:</span></span>

1.  <span data-ttu-id="48e62-122">Il filtro Scarica il grafo.</span><span class="sxs-lookup"><span data-stu-id="48e62-122">The filter flushes the graph.</span></span> <span data-ttu-id="48e62-123">In questo modo si cancellano tutti i dati non aggiornati da Graph, migliorando la velocità di risposta.</span><span class="sxs-lookup"><span data-stu-id="48e62-123">This clears any stale data from graph, which improves responsiveness.</span></span> <span data-ttu-id="48e62-124">In caso contrario, gli esempi memorizzati nel buffer prima del comando seek potrebbero essere recapitati.</span><span class="sxs-lookup"><span data-stu-id="48e62-124">Otherwise, samples that were buffered prior to the seek command might get delivered.</span></span>
2.  <span data-ttu-id="48e62-125">Il filtro chiama [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) per informare i filtri downstream della nuova ora di arresto, dell'ora di inizio e della velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="48e62-125">The filter calls [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) to inform downstream filters of the new stop time, start time, and playback rate.</span></span>
3.  <span data-ttu-id="48e62-126">Il filtro imposta quindi il flag di discontinuità sul primo campione dopo il comando seek.</span><span class="sxs-lookup"><span data-stu-id="48e62-126">The filter then sets the discontinuity flag on the first sample after the seek command.</span></span>

<span data-ttu-id="48e62-127">I timestamp iniziano da zero dopo qualsiasi comando seek, incluse le modifiche di frequenza.</span><span class="sxs-lookup"><span data-stu-id="48e62-127">Time stamps start from zero after any seek command (including rate changes).</span></span>

## <a name="quick-overview-of-the-ball-filter"></a><span data-ttu-id="48e62-128">Panoramica rapida del filtro palla</span><span class="sxs-lookup"><span data-stu-id="48e62-128">Quick Overview of the Ball Filter</span></span>

<span data-ttu-id="48e62-129">Il filtro palla è un'origine push, il che significa che usa un thread di lavoro per recapitare campioni a valle, anziché un'origine pull, che attende passivamente un filtro downstream per richiedere esempi.</span><span class="sxs-lookup"><span data-stu-id="48e62-129">The Ball filter is a push source, which means that it uses a worker thread to deliver samples downstream, as opposed to a pull source, which passively waits for a downstream filter to request samples.</span></span> <span data-ttu-id="48e62-130">Il filtro palla viene creato dalla classe [**CSource**](csource.md) e il relativo pin di output viene creato dalla classe [**CSourceStream**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="48e62-130">The Ball filter is built from the [**CSource**](csource.md) class, and its output pin is built from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="48e62-131">La classe **CSourceStream** crea il thread di lavoro che guida il flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="48e62-131">The **CSourceStream** class creates the worker thread that drives the flow of data.</span></span> <span data-ttu-id="48e62-132">Questo thread immette un ciclo che ottiene campioni dall'allocatore, li compila con i dati e li recapita a valle.</span><span class="sxs-lookup"><span data-stu-id="48e62-132">This thread enters a loop that gets samples from the allocator, fills them with data, and delivers them downstream.</span></span>

<span data-ttu-id="48e62-133">La maggior parte dell'azione in [**CSourceStream**](csourcestream.md) si verifica nel metodo [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , che viene implementato dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="48e62-133">Most of the action in [**CSourceStream**](csourcestream.md) happens in the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which the derived class implements.</span></span> <span data-ttu-id="48e62-134">L'argomento di questo metodo è un puntatore all'esempio da recapitare.</span><span class="sxs-lookup"><span data-stu-id="48e62-134">The argument to this method is a pointer to the sample to be delivered.</span></span> <span data-ttu-id="48e62-135">L'implementazione di **FillBuffer** del filtro palla recupera l'indirizzo del buffer di esempio e viene disegnato direttamente nel buffer impostando singoli valori pixel.</span><span class="sxs-lookup"><span data-stu-id="48e62-135">The Ball filter's implementation of **FillBuffer** retrieves the address of the sample buffer and draws directly to the buffer by setting individual pixel values.</span></span> <span data-ttu-id="48e62-136">Il disegno viene eseguito da una classe helper, CBall, in modo che sia possibile ignorare i dettagli relativi a profondità di bit, tavolozze e così via.</span><span class="sxs-lookup"><span data-stu-id="48e62-136">(The drawing is done by a helper class, CBall, so you can ignore the details regarding bit depths, palettes, and so forth.)</span></span>

## <a name="modifying-the-ball-filter-for-seeking"></a><span data-ttu-id="48e62-137">Modifica del filtro palla per la ricerca</span><span class="sxs-lookup"><span data-stu-id="48e62-137">Modifying the Ball Filter for Seeking</span></span>

<span data-ttu-id="48e62-138">Per fare in modo che il filtro palla sia ricercabile, usare la classe [**CSourceSeeking**](csourceseeking.md) , progettata per implementare la ricerca nei filtri con un pin di output.</span><span class="sxs-lookup"><span data-stu-id="48e62-138">To make the Ball filter seekable, use the [**CSourceSeeking**](csourceseeking.md) class, which is designed for implementing seeking in filters with one output pin.</span></span> <span data-ttu-id="48e62-139">Aggiungere la classe **CSourceSeeking** all'elenco di ereditarietà per la classe CBallStream:</span><span class="sxs-lookup"><span data-stu-id="48e62-139">Add the **CSourceSeeking** class to the inheritance list for the CBallStream class:</span></span>


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



<span data-ttu-id="48e62-140">Sarà inoltre necessario aggiungere un inizializzatore per [**CSourceSeeking**](csourceseeking.md) al costruttore CBallStream:</span><span class="sxs-lookup"><span data-stu-id="48e62-140">Also, you will need to add an initializer for [**CSourceSeeking**](csourceseeking.md) to the CBallStream constructor:</span></span>


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



<span data-ttu-id="48e62-141">Questa istruzione chiama il costruttore di base per [**CSourceSeeking**](csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="48e62-141">This statement calls the base constructor for [**CSourceSeeking**](csourceseeking.md).</span></span> <span data-ttu-id="48e62-142">I parametri sono un nome, un puntatore al pin proprietario, un valore **HRESULT** e l'indirizzo di un oggetto sezione critica.</span><span class="sxs-lookup"><span data-stu-id="48e62-142">The parameters are a name, a pointer to the owning pin, an **HRESULT** value, and the address of a critical section object.</span></span> <span data-ttu-id="48e62-143">Il nome viene usato solo per il debug e la macro del [**nome**](name.md) viene compilata in una stringa vuota nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="48e62-143">The name is used only for debugging, and the [**NAME**](name.md) macro compiles to an empty string in retail builds.</span></span> <span data-ttu-id="48e62-144">Il pin eredita direttamente **CSourceSeeking**, quindi il secondo parametro è un puntatore a se stesso, eseguito il cast a un puntatore [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="48e62-144">The pin directly inherits **CSourceSeeking**, so the second parameter is a pointer to itself, cast to an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointer.</span></span> <span data-ttu-id="48e62-145">Il valore **HRESULT** viene ignorato nella versione corrente delle classi di base. rimane per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="48e62-145">The **HRESULT** value is ignored in the current version of the base classes; it remains for compatibility with previous versions.</span></span> <span data-ttu-id="48e62-146">La sezione critica protegge i dati condivisi, ad esempio l'ora di inizio, l'ora di arresto e la velocità di riproduzione correnti.</span><span class="sxs-lookup"><span data-stu-id="48e62-146">The critical section protects shared data, such as the current start time, stop time, and playback rate.</span></span>

<span data-ttu-id="48e62-147">Aggiungere l'istruzione seguente all'interno del costruttore [**CSourceSeeking**](csourceseeking.md) :</span><span class="sxs-lookup"><span data-stu-id="48e62-147">Add the following statement inside the [**CSourceSeeking**](csourceseeking.md) constructor:</span></span>


```C++
m_rtStop = 60 * UNITS;
```



<span data-ttu-id="48e62-148">La variabile *m \_ rtStop* specifica l'ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="48e62-148">The *m\_rtStop* variable specifies the stop time.</span></span> <span data-ttu-id="48e62-149">Per impostazione predefinita, il valore è \_ I64 \_ Max/2, che corrisponde a circa 14.600 anni.</span><span class="sxs-lookup"><span data-stu-id="48e62-149">By default, the value is \_I64\_MAX / 2, which is approximately 14,600 years.</span></span> <span data-ttu-id="48e62-150">L'istruzione precedente lo imposta su un valore di 60 secondi più conservativo.</span><span class="sxs-lookup"><span data-stu-id="48e62-150">The previous statement sets it to a more conservative 60 seconds.</span></span>

<span data-ttu-id="48e62-151">È necessario aggiungere altre due variabili membro a CBallStream:</span><span class="sxs-lookup"><span data-stu-id="48e62-151">Two additional member variables must be added to CBallStream:</span></span>


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



<span data-ttu-id="48e62-152">Dopo ogni comando seek, il filtro deve impostare il flag di discontinuità nell'esempio seguente chiamando [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span><span class="sxs-lookup"><span data-stu-id="48e62-152">After every seek command, the filter must set the discontinuity flag on the next sample by calling [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span></span> <span data-ttu-id="48e62-153">La variabile *m \_ bDiscontinuity* terrà traccia di questo.</span><span class="sxs-lookup"><span data-stu-id="48e62-153">The *m\_bDiscontinuity* variable will keep track of this.</span></span> <span data-ttu-id="48e62-154">La *variabile \_ rtBallPosition m* consente di specificare la posizione della palla all'interno del frame del video.</span><span class="sxs-lookup"><span data-stu-id="48e62-154">The *m\_rtBallPosition* variable will specify the position of the ball within the video frame.</span></span> <span data-ttu-id="48e62-155">Il filtro palla originale calcola la posizione dall'ora del flusso, ma il tempo di flusso viene reimpostato su zero dopo ogni comando seek.</span><span class="sxs-lookup"><span data-stu-id="48e62-155">The original Ball filter calculates the position from the stream time, but the stream time resets to zero after each seek command.</span></span> <span data-ttu-id="48e62-156">In un flusso ricercabile, la posizione assoluta è indipendente dall'ora del flusso.</span><span class="sxs-lookup"><span data-stu-id="48e62-156">In a seekable stream, the absolute position is independent of the stream time.</span></span>

### <a name="queryinterface"></a><span data-ttu-id="48e62-157">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="48e62-157">QueryInterface</span></span>

<span data-ttu-id="48e62-158">La classe [**CSourceSeeking**](csourceseeking.md) implementa l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="48e62-158">The [**CSourceSeeking**](csourceseeking.md) class implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="48e62-159">Per esporre questa interfaccia ai client, eseguire l'override del metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) :</span><span class="sxs-lookup"><span data-stu-id="48e62-159">To expose this interface to clients, override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method:</span></span>


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="48e62-160">Il metodo è denominato "non Delegating" a causa del modo in cui le classi base DirectShow supportano l'aggregazione Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="48e62-160">The method is called "NonDelegating" because of the way the DirectShow base classes support Component Object Model (COM) aggregation.</span></span> <span data-ttu-id="48e62-161">Per ulteriori informazioni, vedere l'argomento "come implementare IUnknown" in DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="48e62-161">For more information, see the "How to Implement IUnknown" topic in the DirectShow SDK.</span></span>

### <a name="seeking-methods"></a><span data-ttu-id="48e62-162">Metodi di ricerca</span><span class="sxs-lookup"><span data-stu-id="48e62-162">Seeking Methods</span></span>

<span data-ttu-id="48e62-163">La classe [**CSourceSeeking**](csourceseeking.md) gestisce diverse variabili membro relative alla ricerca.</span><span class="sxs-lookup"><span data-stu-id="48e62-163">The [**CSourceSeeking**](csourceseeking.md) class maintains several member variables relating to seeking.</span></span>



| <span data-ttu-id="48e62-164">Variabile</span><span class="sxs-lookup"><span data-stu-id="48e62-164">Variable</span></span>          | <span data-ttu-id="48e62-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48e62-165">Description</span></span>   | <span data-ttu-id="48e62-166">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="48e62-166">Default Value</span></span>  |
|-------------------|---------------|----------------|
| <span data-ttu-id="48e62-167">*\_rtStart m*</span><span class="sxs-lookup"><span data-stu-id="48e62-167">*m\_rtStart*</span></span>      | <span data-ttu-id="48e62-168">Ora di inizio</span><span class="sxs-lookup"><span data-stu-id="48e62-168">Start time</span></span>    | <span data-ttu-id="48e62-169">Zero</span><span class="sxs-lookup"><span data-stu-id="48e62-169">Zero</span></span>           |
| <span data-ttu-id="48e62-170">*\_rtStop m*</span><span class="sxs-lookup"><span data-stu-id="48e62-170">*m\_rtStop*</span></span>       | <span data-ttu-id="48e62-171">Ora di arresto</span><span class="sxs-lookup"><span data-stu-id="48e62-171">Stop time</span></span>     | <span data-ttu-id="48e62-172">\_I64 \_ Max/2</span><span class="sxs-lookup"><span data-stu-id="48e62-172">\_I64\_MAX / 2</span></span> |
| <span data-ttu-id="48e62-173">*\_dRateSeeking m*</span><span class="sxs-lookup"><span data-stu-id="48e62-173">*m\_dRateSeeking*</span></span> | <span data-ttu-id="48e62-174">Velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="48e62-174">Playback rate</span></span> | <span data-ttu-id="48e62-175">1.0</span><span class="sxs-lookup"><span data-stu-id="48e62-175">1.0</span></span>            |



 

<span data-ttu-id="48e62-176">L'implementazione [**CSourceSeeking**](csourceseeking.md) di [**IMediaSeeking:: sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) aggiorna le ore di inizio e di fine e quindi chiama due metodi virtuali puri sulla classe derivata, [**CSourceSeeking:: iniziale**](csourceseeking-changestart.md) e [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="48e62-176">The [**CSourceSeeking**](csourceseeking.md) implementation of [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) updates the start and stop times, and then calls two pure virtual methods on the derived class, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span> <span data-ttu-id="48e62-177">L'implementazione di [**IMediaSeeking:: serate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) è simile: aggiorna la velocità di riproduzione e quindi chiama il metodo virtuale puro [**CSourceSeeking:: changere**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="48e62-177">The implementation of [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) is similar: It updates the playback rate and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="48e62-178">In ognuno di questi metodi virtuali il PIN deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="48e62-178">In each of these virtual methods, the pin must do the following:</span></span>

1.  <span data-ttu-id="48e62-179">Chiamare [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) per avviare lo scaricamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="48e62-179">Call [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) to start flushing data.</span></span>
2.  <span data-ttu-id="48e62-180">Arrestare il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="48e62-180">Halt the streaming thread.</span></span>
3.  <span data-ttu-id="48e62-181">Chiamare [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="48e62-181">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>
4.  <span data-ttu-id="48e62-182">Riavviare il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="48e62-182">Restart the streaming thread.</span></span>
5.  <span data-ttu-id="48e62-183">Chiamare [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span><span class="sxs-lookup"><span data-stu-id="48e62-183">Call [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span></span>
6.  <span data-ttu-id="48e62-184">Impostare il flag di discontinuità nell'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="48e62-184">Set the discontinuity flag on the next sample.</span></span>

<span data-ttu-id="48e62-185">L'ordine di questi passaggi è fondamentale, perché il thread di streaming può bloccarsi durante l'attesa del recapito di un campione o ottenere un nuovo esempio.</span><span class="sxs-lookup"><span data-stu-id="48e62-185">The order of these steps is crucial, because the streaming thread can block while it waits to deliver a sample or get a new sample.</span></span> <span data-ttu-id="48e62-186">Il metodo [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garantisce che il thread di streaming non sia bloccato e pertanto non verrà generato un deadlock nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="48e62-186">The [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method ensures that the streaming thread is not blocked and therefore will not deadlock in step 2.</span></span> <span data-ttu-id="48e62-187">La chiamata a [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informa i filtri downstream per prevedere nuovi esempi, in modo che non li rifiuti quando il thread viene riavviato nel passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="48e62-187">The [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) call informs the downstream filters to expect new samples, so they do not reject them when the thread starts again in step 4.</span></span>

<span data-ttu-id="48e62-188">Il metodo privato seguente esegue i passaggi da 1 a 4:</span><span class="sxs-lookup"><span data-stu-id="48e62-188">The following private method performs steps 1 through 4:</span></span>


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



<span data-ttu-id="48e62-189">Quando il thread di streaming viene riavviato, chiama il metodo [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) .</span><span class="sxs-lookup"><span data-stu-id="48e62-189">When the streaming thread starts again, it calls the [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method.</span></span> <span data-ttu-id="48e62-190">Eseguire l'override di questo metodo per eseguire i passaggi 5 e 6:</span><span class="sxs-lookup"><span data-stu-id="48e62-190">Override this method to perform steps 5 and 6:</span></span>


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



<span data-ttu-id="48e62-191">Nel metodo [**iniziale**](csourceseeking-changestart.md) impostare la durata del flusso su zero e la posizione della palla sulla nuova ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="48e62-191">In the [**ChangeStart**](csourceseeking-changestart.md) method, set the stream time to zero and the position of the ball to the new start time.</span></span> <span data-ttu-id="48e62-192">Quindi, chiamare CBallStream:: UpdateFromSeek:</span><span class="sxs-lookup"><span data-stu-id="48e62-192">Then call CBallStream::UpdateFromSeek:</span></span>


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="48e62-193">Nel metodo [**ChangeStop**](csourceseeking-changestop.md) chiamare CBallStream:: UpdateFromSeek se la nuova ora di arresto è inferiore alla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="48e62-193">In the [**ChangeStop**](csourceseeking-changestop.md) method, call CBallStream::UpdateFromSeek if the new stop time is less than the current position.</span></span> <span data-ttu-id="48e62-194">In caso contrario, l'ora di arresto è ancora in futuro, quindi non è necessario scaricare il grafo.</span><span class="sxs-lookup"><span data-stu-id="48e62-194">Otherwise, the stop time is still in the future, so there's no need to flush the graph.</span></span>


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="48e62-195">Per le modifiche alla frequenza, il metodo [**CSourceSeeking::**](csourceseeking-setrate.md) SetValue imposta *m \_ dRateSeeking* sulla nuova frequenza (eliminando il valore precedente) prima di chiamare [**changere**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="48e62-195">For rate changes, the [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method sets *m\_dRateSeeking* to the new rate (discarding the old value) before it calls [**ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="48e62-196">Sfortunatamente, se il chiamante ha assegnato una frequenza non valida, ad esempio minore di zero, è troppo tardi per chiamare il **juke** -time.</span><span class="sxs-lookup"><span data-stu-id="48e62-196">Unfortunately, if the caller gave an invalid rate—for example, less than zero—it's too late by the time **ChangeRate** is called.</span></span> <span data-ttu-id="48e62-197">Una soluzione consiste nell'eseguire l'override di **bitrate** e verificare la validità delle tariffe:</span><span class="sxs-lookup"><span data-stu-id="48e62-197">One solution is to override **SetRate** and check for valid rates:</span></span>


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a><span data-ttu-id="48e62-198">Disegno nel buffer</span><span class="sxs-lookup"><span data-stu-id="48e62-198">Drawing in the Buffer</span></span>

<span data-ttu-id="48e62-199">Di seguito è illustrata la versione modificata di [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md), la routine che disegna la palla in ogni frame:</span><span class="sxs-lookup"><span data-stu-id="48e62-199">Here is the modified version of [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), the routine that draws the ball on each frame:</span></span>


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



<span data-ttu-id="48e62-200">Le differenze principali tra questa versione e quella originale sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="48e62-200">The major differences between this version and the original are the following:</span></span>

-   <span data-ttu-id="48e62-201">Come indicato in precedenza, la variabile *m \_ rtBallPosition* viene utilizzata per impostare la posizione della palla anziché l'ora del flusso.</span><span class="sxs-lookup"><span data-stu-id="48e62-201">As mentioned earlier, the *m\_rtBallPosition* variable is used to set the position of the ball, rather than the stream time.</span></span>
-   <span data-ttu-id="48e62-202">Dopo aver tenuto la sezione critica, il metodo controlla se la posizione corrente supera l'ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="48e62-202">After holding the critical section, the method checks whether the current position exceeds the stop time.</span></span> <span data-ttu-id="48e62-203">In caso affermativo, **restituisce \_ false**, che segnala alla classe di base di arrestare l'invio di dati e recapitare una notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="48e62-203">If so, it returns **S\_FALSE**, which signals the base class to stop sending data and deliver an end-of-stream notification.</span></span>
-   <span data-ttu-id="48e62-204">I timestamp sono divisi per la frequenza corrente.</span><span class="sxs-lookup"><span data-stu-id="48e62-204">The time stamps are divided by the current rate.</span></span>
-   <span data-ttu-id="48e62-205">Se *m \_ BDiscontinuity* è **true**, il metodo imposta il flag di discontinuità nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="48e62-205">If *m\_bDiscontinuity* is **TRUE**, the method sets the discontinuity flag on the sample.</span></span>

<span data-ttu-id="48e62-206">C'è un'altra differenza minore.</span><span class="sxs-lookup"><span data-stu-id="48e62-206">There is another minor difference.</span></span> <span data-ttu-id="48e62-207">Poiché la versione originale si basa su un solo buffer, riempie l'intero buffer con zeri una volta, all'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="48e62-207">Because the original version relies on having exactly one buffer, it fills the entire buffer with zeroes once, when streaming begins.</span></span> <span data-ttu-id="48e62-208">Dopodiché, cancella solo la palla dalla posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="48e62-208">After that, it just erases the ball from its previous position.</span></span> <span data-ttu-id="48e62-209">Tuttavia, questa ottimizzazione rivela un lieve bug nel filtro palla.</span><span class="sxs-lookup"><span data-stu-id="48e62-209">However, this optimization reveals a slight bug in the Ball filter.</span></span> <span data-ttu-id="48e62-210">Quando il metodo [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) chiama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), imposta il flag di sola lettura su **false**.</span><span class="sxs-lookup"><span data-stu-id="48e62-210">When the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), it sets the read-only flag to **FALSE**.</span></span> <span data-ttu-id="48e62-211">Di conseguenza, il filtro downstream è libero di scrivere nel buffer.</span><span class="sxs-lookup"><span data-stu-id="48e62-211">As a result, the downstream filter is free to write on the buffer.</span></span> <span data-ttu-id="48e62-212">Una soluzione consiste nell'eseguire l'override di **DecideAllocator** in modo da impostare il flag di sola lettura su **true**.</span><span class="sxs-lookup"><span data-stu-id="48e62-212">One solution is to override **DecideAllocator** so that it sets the read-only flag to **TRUE**.</span></span> <span data-ttu-id="48e62-213">Per semplicità, tuttavia, la nuova versione consente semplicemente di rimuovere completamente l'ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="48e62-213">For simplicity, however, the new version simply removes the optimization altogether.</span></span> <span data-ttu-id="48e62-214">Questa versione riempie invece il buffer con zeri ogni volta.</span><span class="sxs-lookup"><span data-stu-id="48e62-214">Instead, this version fills the buffer with zeroes each time.</span></span>

### <a name="miscellaneous-changes"></a><span data-ttu-id="48e62-215">Modifiche varie</span><span class="sxs-lookup"><span data-stu-id="48e62-215">Miscellaneous Changes</span></span>

<span data-ttu-id="48e62-216">Nella nuova versione queste due righe vengono rimosse dal Costruttore CBall:</span><span class="sxs-lookup"><span data-stu-id="48e62-216">In the new version, these two lines are removed from the CBall constructor:</span></span>


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



<span data-ttu-id="48e62-217">Il filtro palla originale usa questi valori per aggiungere la casualità alla posizione iniziale della palla.</span><span class="sxs-lookup"><span data-stu-id="48e62-217">The original Ball filter uses these values to add some randomness to the initial ball position.</span></span> <span data-ttu-id="48e62-218">Per questo scopo, è necessario che la palla sia deterministica.</span><span class="sxs-lookup"><span data-stu-id="48e62-218">For our purposes, we want the ball to be deterministic.</span></span> <span data-ttu-id="48e62-219">Inoltre, alcune variabili sono state modificate dagli oggetti [**CRefTime**](creftime.md) alle [**variabili \_ temporali di riferimento**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="48e62-219">Also, some variables have been changed from [**CRefTime**](creftime.md) objects to [**REFERENCE\_TIME**](reference-time.md) variables.</span></span> <span data-ttu-id="48e62-220">La classe **CRefTime** è un wrapper sottile per un valore **di \_ ora di riferimento** . Infine, l'implementazione di [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) è stata modificata leggermente; per informazioni dettagliate, è possibile fare riferimento al codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="48e62-220">(The **CRefTime** class is a thin wrapper for a **REFERENCE\_TIME** value.) Lastly, the implementation of [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) has been modified slightly; you can refer to the source code for details.</span></span>

## <a name="limitations-of-the-csourceseeking-class"></a><span data-ttu-id="48e62-221">Limitazioni della classe CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="48e62-221">Limitations of the CSourceSeeking Class</span></span>

<span data-ttu-id="48e62-222">La classe [**CSourceSeeking**](csourceseeking.md) non è destinata ai filtri con più pin di output, a causa di problemi di comunicazione tra pin.</span><span class="sxs-lookup"><span data-stu-id="48e62-222">The [**CSourceSeeking**](csourceseeking.md) class is not meant for filters with multiple output pins, because of issues with cross-pin communication.</span></span> <span data-ttu-id="48e62-223">Si supponga, ad esempio, un filtro del parser che riceve un flusso audio-video Interleaved, suddivide il flusso nei componenti audio e video e recapita il video da un pin di output e audio da un altro.</span><span class="sxs-lookup"><span data-stu-id="48e62-223">For example, imagine a parser filter that receives an interleaved audio-video stream, splits the stream into its audio and video components, and delivers video from one output pin and audio from another.</span></span> <span data-ttu-id="48e62-224">Entrambi i pin di output riceveranno ogni comando seek, ma il filtro deve cercare solo una volta per ogni comando seek.</span><span class="sxs-lookup"><span data-stu-id="48e62-224">Both output pins will receive every seek command, but the filter should seek only once per seek command.</span></span> <span data-ttu-id="48e62-225">La soluzione consiste nel designare uno dei pin per controllare la ricerca e ignorare i comandi Seek ricevuti dall'altro pin.</span><span class="sxs-lookup"><span data-stu-id="48e62-225">The solution is to designate one of the pins to control seeking and to ignore seek commands received by the other pin.</span></span>

<span data-ttu-id="48e62-226">Dopo il comando seek, tuttavia, entrambi i pin devono svuotare i dati.</span><span class="sxs-lookup"><span data-stu-id="48e62-226">After the seek command, however, both pins should flush data.</span></span> <span data-ttu-id="48e62-227">Per complicare ulteriormente il problema, il comando seek si verifica nel thread dell'applicazione, non nel thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="48e62-227">To complicate matters further, the seek command happens on the application thread, not the streaming thread.</span></span> <span data-ttu-id="48e62-228">Pertanto, è necessario assicurarsi che nessuno dei due pin sia bloccato e in attesa della restituzione di una chiamata [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) oppure che sia possibile che si verifichi un deadlock.</span><span class="sxs-lookup"><span data-stu-id="48e62-228">Therefore, you must make certain that neither pin is blocked and waiting for a [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call to return, or it might cause a deadlock.</span></span> <span data-ttu-id="48e62-229">Per ulteriori informazioni sullo svuotamento thread-safe nei pin, vedere [thread e sezioni critiche](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="48e62-229">For more information about thread-safe flushing in pins, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48e62-230">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48e62-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48e62-231">Scrittura di filtri di origine</span><span class="sxs-lookup"><span data-stu-id="48e62-231">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 



