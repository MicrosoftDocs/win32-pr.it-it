---
description: La classe CPosPassThru gestisce i comandi Seek per i filtri di trasformazione, passandoli upstream al filtro successivo.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Classe CPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328495"
---
# <a name="cpospassthru-class"></a><span data-ttu-id="bf1e1-103">Classe CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="bf1e1-103">CPosPassThru class</span></span>

![gerarchia della classe base cpospassthru](images/cutil14.png)

<span data-ttu-id="bf1e1-105">La `CPosPassThru` classe gestisce i comandi Seek per i filtri di trasformazione, passandogli upstream al filtro successivo.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-105">The `CPosPassThru` class handles seek commands for transform filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="bf1e1-106">Quando un'applicazione cerca il grafico dei filtri, il gestore del grafico dei filtri fornisce al comando seek i filtri del renderer.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-106">When an application seeks the filter graph, the Filter Graph Manager gives the seek command to the renderer filters.</span></span> <span data-ttu-id="bf1e1-107">Il comando viene passato a Monte, tramite il pin di output di ogni filtro, fino a quando non raggiunge un filtro in grado di eseguire il comando (se presente).</span><span class="sxs-lookup"><span data-stu-id="bf1e1-107">The command is passed upstream, through each filter's output pin, until it reaches a filter that can execute the command (if any).</span></span> <span data-ttu-id="bf1e1-108">Per informazioni dettagliate, vedere la pagina relativa [alla ricerca](seeking.md).</span><span class="sxs-lookup"><span data-stu-id="bf1e1-108">For details, see [Seeking](seeking.md).</span></span> <span data-ttu-id="bf1e1-109">La `CPosPassThru` classe passa tutti i comandi Seek al pin di output sul filtro upstream, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-109">The `CPosPassThru` class passes all seek commands to the output pin on the upstream filter, as shown in the following diagram.</span></span>

![la classe cpospassthru invia i comandi Seek upstream.](images/cpospassthru.png)

<span data-ttu-id="bf1e1-111">Sebbene questa classe venga fornita nella libreria di classi base, DirectShow fornisce anche la stessa classe in Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-111">Although this class is provided in the base class library, DirectShow also provides the same class in Quartz.dll.</span></span> <span data-ttu-id="bf1e1-112">L'uso della versione Quartz.dll può ridurre in qualche modo le dimensioni del codice nel filtro, perché la classe viene caricata in fase di esecuzione dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-112">Using the Quartz.dll version can reduce the code size in your filter somewhat, because the class is loaded at run-time from the DLL.</span></span> <span data-ttu-id="bf1e1-113">Per utilizzare tale versione, chiamare la funzione [**CreatePosPassThru**](createpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="bf1e1-113">To use that version, call the [**CreatePosPassThru**](createpospassthru.md) function.</span></span>

<span data-ttu-id="bf1e1-114">Nel metodo **NonDelegatingQueryInterface** del PIN di output, delegare all'oggetto **CPosPassThru** ogni volta che l'interfaccia richiesta è [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) o [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="bf1e1-114">In your output pin's **NonDelegatingQueryInterface** method, delegate to the **CPosPassThru** object whenever the requested interface is [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) or [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), as shown in the following code:</span></span>


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



<span data-ttu-id="bf1e1-115">Eccetto laddove specificato, tutti i metodi [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) in questa classe chiamano il metodo corrispondente sul pin connesso e restituiscono il risultato.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-115">Except where noted, all [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods in this class call the corresponding method on the connected pin and return the result.</span></span>



| <span data-ttu-id="bf1e1-116">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="bf1e1-116">Public Methods</span></span>                                                    | <span data-ttu-id="bf1e1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf1e1-117">Description</span></span>                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf1e1-118">**CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-118">**CPosPassThru**</span></span>](cpospassthru-cpospassthru.md)                 | <span data-ttu-id="bf1e1-119">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-119">Constructor method.</span></span>                                                                                 |
| [<span data-ttu-id="bf1e1-120">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-120">**ForceRefresh**</span></span>](cpospassthru-forcerefresh.md)                 | <span data-ttu-id="bf1e1-121">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-121">Obsolete.</span></span>                                                                                           |
| [<span data-ttu-id="bf1e1-122">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-122">**GetMediaTime**</span></span>](cpospassthru-getmediatime.md)                 | <span data-ttu-id="bf1e1-123">Recupera i timestamp sull'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-123">Retrieves the time stamps on the current sample.</span></span> <span data-ttu-id="bf1e1-124">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-124">Virtual.</span></span>                                           |
| <span data-ttu-id="bf1e1-125">Metodi IMediaPosition</span><span class="sxs-lookup"><span data-stu-id="bf1e1-125">IMediaPosition Methods</span></span>                                            | <span data-ttu-id="bf1e1-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf1e1-126">Description</span></span>                                                                                         |
| [<span data-ttu-id="bf1e1-127">**ottenere la \_ durata**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-127">**get\_Duration**</span></span>](cpospassthru-get-duration.md)                | <span data-ttu-id="bf1e1-128">Recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-128">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="bf1e1-129">**Inserisci \_ currentPosition**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-129">**put\_CurrentPosition**</span></span>](cpospassthru-put-currentposition.md)  | <span data-ttu-id="bf1e1-130">Imposta la posizione corrente rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-130">Sets the current position, relative to the total duration of the stream.</span></span>                            |
| [<span data-ttu-id="bf1e1-131">**ottenere \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-131">**get\_StopTime**</span></span>](cpospassthru-get-stoptime.md)                | <span data-ttu-id="bf1e1-132">Recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-132">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="bf1e1-133">**Inserisci \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-133">**put\_StopTime**</span></span>](cpospassthru-put-stoptime.md)                | <span data-ttu-id="bf1e1-134">Imposta l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-134">Sets the time at which the playback will stop, relative to the duration of the stream.</span></span>              |
| [<span data-ttu-id="bf1e1-135">**ottenere \_ PrerollTime**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-135">**get\_PrerollTime**</span></span>](cpospassthru-get-prerolltime.md)          | <span data-ttu-id="bf1e1-136">Recupera la quantità di dati che verranno accodati prima della posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-136">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="bf1e1-137">**Inserisci \_ PrerollTime**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-137">**put\_PrerollTime**</span></span>](cpospassthru-put-prerolltime.md)          | <span data-ttu-id="bf1e1-138">Imposta la quantità di dati che verranno accodati prima della posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-138">Sets the amount of data that will be queued before the start position.</span></span>                              |
| [<span data-ttu-id="bf1e1-139">**velocità di ottenimento \_**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-139">**get\_Rate**</span></span>](cpospassthru-get-rate.md)                        | <span data-ttu-id="bf1e1-140">Recupera la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-140">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="bf1e1-141">**percentuale di inserimento \_**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-141">**put\_Rate**</span></span>](cpospassthru-put-rate.md)                        | <span data-ttu-id="bf1e1-142">Imposta la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-142">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="bf1e1-143">**ottenere \_ currentPosition**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-143">**get\_CurrentPosition**</span></span>](cpospassthru-get-currentposition.md)  | <span data-ttu-id="bf1e1-144">Recupera la posizione corrente rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-144">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="bf1e1-145">**CanSeekForward**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-145">**CanSeekForward**</span></span>](cpospassthru-canseekforward.md)             | <span data-ttu-id="bf1e1-146">Determina se è possibile cercare il flusso all'indietro.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-146">Determines whether the stream can be seeked backward.</span></span>                                               |
| [<span data-ttu-id="bf1e1-147">**CanSeekBackward**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-147">**CanSeekBackward**</span></span>](cpospassthru-canseekbackward.md)           | <span data-ttu-id="bf1e1-148">Determina se il flusso può essere cercato in futuro.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-148">Determines whether the stream can be seeked forward.</span></span>                                                |
| <span data-ttu-id="bf1e1-149">Metodi IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="bf1e1-149">IMediaSeeking Methods</span></span>                                             | <span data-ttu-id="bf1e1-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf1e1-150">Description</span></span>                                                                                         |
| [<span data-ttu-id="bf1e1-151">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-151">**CheckCapabilities**</span></span>](cpospassthru-checkcapabilities.md)       | <span data-ttu-id="bf1e1-152">Esegue una query per determinare se un flusso ha specificato funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-152">Queries whether a stream has specified seeking capabilities.</span></span>                                        |
| [<span data-ttu-id="bf1e1-153">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-153">**ConvertTimeFormat**</span></span>](cpospassthru-converttimeformat.md)       | <span data-ttu-id="bf1e1-154">Esegue la conversione da un formato di ora a un altro.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-154">Converts from one time format to another.</span></span>                                                           |
| [<span data-ttu-id="bf1e1-155">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-155">**GetAvailable**</span></span>](cpospassthru-getavailable.md)                 | <span data-ttu-id="bf1e1-156">Recupera l'intervallo di tempo in cui la ricerca è efficiente.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-156">Retrieves the range of times in which seeking is efficient.</span></span>                                         |
| [<span data-ttu-id="bf1e1-157">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-157">**GetCapabilities**</span></span>](cpospassthru-getcapabilities.md)           | <span data-ttu-id="bf1e1-158">Recupera tutte le funzionalità di ricerca del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-158">Retrieves all the seeking capabilities of the stream.</span></span>                                               |
| [<span data-ttu-id="bf1e1-159">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-159">**GetCurrentPosition**</span></span>](cpospassthru-getcurrentposition.md)     | <span data-ttu-id="bf1e1-160">Recupera la posizione corrente rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-160">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="bf1e1-161">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-161">**GetDuration**</span></span>](cpospassthru-getduration.md)                   | <span data-ttu-id="bf1e1-162">Recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-162">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="bf1e1-163">**GetPositions**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-163">**GetPositions**</span></span>](cpospassthru-getpositions.md)                 | <span data-ttu-id="bf1e1-164">Recupera la posizione corrente e la posizione di arresto rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-164">Retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> |
| [<span data-ttu-id="bf1e1-165">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-165">**GetPreroll**</span></span>](cpospassthru-getpreroll.md)                     | <span data-ttu-id="bf1e1-166">Recupera la quantità di dati che verranno accodati prima della posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-166">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="bf1e1-167">**Getrate**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-167">**GetRate**</span></span>](cpospassthru-getrate.md)                           | <span data-ttu-id="bf1e1-168">Recupera la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-168">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="bf1e1-169">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-169">**GetStopPosition**</span></span>](cpospassthru-getstopposition.md)           | <span data-ttu-id="bf1e1-170">Recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-170">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="bf1e1-171">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-171">**GetTimeFormat**</span></span>](cpospassthru-gettimeformat.md)               | <span data-ttu-id="bf1e1-172">Recupera il formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-172">Retrieves the current time format.</span></span>                                                                  |
| [<span data-ttu-id="bf1e1-173">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-173">**IsFormatSupported**</span></span>](cpospassthru-isformatsupported.md)       | <span data-ttu-id="bf1e1-174">Determina se è supportato un formato di ora specificato.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-174">Determines whether a specified time format is supported.</span></span>                                            |
| [<span data-ttu-id="bf1e1-175">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-175">**IsUsingTimeFormat**</span></span>](cpospassthru-isusingtimeformat.md)       | <span data-ttu-id="bf1e1-176">Determina se un formato di ora specificato è il formato attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-176">Determines whether a specified time format is the format currently in use.</span></span>                          |
| [<span data-ttu-id="bf1e1-177">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-177">**QueryPreferredFormat**</span></span>](cpospassthru-querypreferredformat.md) | <span data-ttu-id="bf1e1-178">Recupera il formato di ora preferito per il flusso.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-178">Retrieves the preferred time format for the stream.</span></span>                                                 |
| [<span data-ttu-id="bf1e1-179">**Posizioni**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-179">**SetPositions**</span></span>](cpospassthru-setpositions.md)                 | <span data-ttu-id="bf1e1-180">Imposta la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-180">Sets the current position and the stop position.</span></span>                                                    |
| [<span data-ttu-id="bf1e1-181">**Frequenza**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-181">**SetRate**</span></span>](cpospassthru-setrate.md)                           | <span data-ttu-id="bf1e1-182">Imposta la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-182">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="bf1e1-183">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-183">**SetTimeFormat**</span></span>](cpospassthru-settimeformat.md)               | <span data-ttu-id="bf1e1-184">Imposta il formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-184">Sets the time format.</span></span>                                                                               |
| <span data-ttu-id="bf1e1-185">Funzioni di supporto</span><span class="sxs-lookup"><span data-stu-id="bf1e1-185">Helper Functions</span></span>                                                  | <span data-ttu-id="bf1e1-186">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf1e1-186">Description</span></span>                                                                                         |
| [<span data-ttu-id="bf1e1-187">**CreatePosPassThru**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-187">**CreatePosPassThru**</span></span>](createpospassthru.md)                    | <span data-ttu-id="bf1e1-188">Crea un `CPosPassThru` oggetto o [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="bf1e1-188">Creates a `CPosPassThru` or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="bf1e1-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf1e1-189">Requirements</span></span>



| <span data-ttu-id="bf1e1-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf1e1-190">Requirement</span></span> | <span data-ttu-id="bf1e1-191">Valore</span><span class="sxs-lookup"><span data-stu-id="bf1e1-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1e1-192">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf1e1-192">Header</span></span><br/>  | <dl> <span data-ttu-id="bf1e1-193"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-193"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf1e1-194">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf1e1-194">Library</span></span><br/> | <dl> <span data-ttu-id="bf1e1-195"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




