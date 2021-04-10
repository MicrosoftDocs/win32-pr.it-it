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
# <a name="supporting-seeking-in-a-source-filter"></a>Supporto della ricerca in un filtro di origine

Questo argomento descrive come implementare la ricerca in un filtro origine Microsoft DirectShow. Usa l'esempio di [filtro palla](ball-filter-sample.md) come punto di partenza e descrive il codice aggiuntivo necessario per supportare la ricerca in questo filtro.

L'esempio di [filtro palla](ball-filter-sample.md) è un filtro di origine che consente di creare una palla da rimbalzo animata. Questo articolo descrive come aggiungere la funzionalità di ricerca a questo filtro. Una volta aggiunta questa funzionalità, è possibile eseguire il rendering del filtro in GraphEdit e controllare la palla trascinando il dispositivo di scorrimento GraphEdit.

In questo argomento sono incluse le sezioni seguenti:

-   [Panoramica della ricerca in DirectShow](#overview-of-seeking-in-directshow)
-   [Panoramica rapida del filtro palla](#quick-overview-of-the-ball-filter)
-   [Modifica del filtro palla per la ricerca](#modifying-the-ball-filter-for-seeking)
-   [Limitazioni della classe CSourceSeeking](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a>Panoramica della ricerca in DirectShow

Un'applicazione cerca il grafico di filtro chiamando un metodo [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) su Filter Graph Manager. Il gestore del grafico dei filtri distribuisce quindi la chiamata a ogni renderer nel grafico. Ogni renderer Invia la chiamata upstream, tramite il pin di output del filtro upstream successivo. La chiamata passa a upstream fino a quando non raggiunge un filtro in grado di eseguire il comando seek, in genere un filtro di origine o un filtro del parser. In generale, il filtro che origina i timestamp gestisce anche la ricerca.

Un filtro risponde a un comando seek come segue:

1.  Il filtro Scarica il grafo. In questo modo si cancellano tutti i dati non aggiornati da Graph, migliorando la velocità di risposta. In caso contrario, gli esempi memorizzati nel buffer prima del comando seek potrebbero essere recapitati.
2.  Il filtro chiama [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) per informare i filtri downstream della nuova ora di arresto, dell'ora di inizio e della velocità di riproduzione.
3.  Il filtro imposta quindi il flag di discontinuità sul primo campione dopo il comando seek.

I timestamp iniziano da zero dopo qualsiasi comando seek, incluse le modifiche di frequenza.

## <a name="quick-overview-of-the-ball-filter"></a>Panoramica rapida del filtro palla

Il filtro palla è un'origine push, il che significa che usa un thread di lavoro per recapitare campioni a valle, anziché un'origine pull, che attende passivamente un filtro downstream per richiedere esempi. Il filtro palla viene creato dalla classe [**CSource**](csource.md) e il relativo pin di output viene creato dalla classe [**CSourceStream**](csourcestream.md) . La classe **CSourceStream** crea il thread di lavoro che guida il flusso di dati. Questo thread immette un ciclo che ottiene campioni dall'allocatore, li compila con i dati e li recapita a valle.

La maggior parte dell'azione in [**CSourceStream**](csourcestream.md) si verifica nel metodo [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , che viene implementato dalla classe derivata. L'argomento di questo metodo è un puntatore all'esempio da recapitare. L'implementazione di **FillBuffer** del filtro palla recupera l'indirizzo del buffer di esempio e viene disegnato direttamente nel buffer impostando singoli valori pixel. Il disegno viene eseguito da una classe helper, CBall, in modo che sia possibile ignorare i dettagli relativi a profondità di bit, tavolozze e così via.

## <a name="modifying-the-ball-filter-for-seeking"></a>Modifica del filtro palla per la ricerca

Per fare in modo che il filtro palla sia ricercabile, usare la classe [**CSourceSeeking**](csourceseeking.md) , progettata per implementare la ricerca nei filtri con un pin di output. Aggiungere la classe **CSourceSeeking** all'elenco di ereditarietà per la classe CBallStream:


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



Sarà inoltre necessario aggiungere un inizializzatore per [**CSourceSeeking**](csourceseeking.md) al costruttore CBallStream:


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



Questa istruzione chiama il costruttore di base per [**CSourceSeeking**](csourceseeking.md). I parametri sono un nome, un puntatore al pin proprietario, un valore **HRESULT** e l'indirizzo di un oggetto sezione critica. Il nome viene usato solo per il debug e la macro del [**nome**](name.md) viene compilata in una stringa vuota nelle compilazioni al dettaglio. Il pin eredita direttamente **CSourceSeeking**, quindi il secondo parametro è un puntatore a se stesso, eseguito il cast a un puntatore [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) . Il valore **HRESULT** viene ignorato nella versione corrente delle classi di base. rimane per la compatibilità con le versioni precedenti. La sezione critica protegge i dati condivisi, ad esempio l'ora di inizio, l'ora di arresto e la velocità di riproduzione correnti.

Aggiungere l'istruzione seguente all'interno del costruttore [**CSourceSeeking**](csourceseeking.md) :


```C++
m_rtStop = 60 * UNITS;
```



La variabile *m \_ rtStop* specifica l'ora di arresto. Per impostazione predefinita, il valore è \_ I64 \_ Max/2, che corrisponde a circa 14.600 anni. L'istruzione precedente lo imposta su un valore di 60 secondi più conservativo.

È necessario aggiungere altre due variabili membro a CBallStream:


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



Dopo ogni comando seek, il filtro deve impostare il flag di discontinuità nell'esempio seguente chiamando [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity). La variabile *m \_ bDiscontinuity* terrà traccia di questo. La *variabile \_ rtBallPosition m* consente di specificare la posizione della palla all'interno del frame del video. Il filtro palla originale calcola la posizione dall'ora del flusso, ma il tempo di flusso viene reimpostato su zero dopo ogni comando seek. In un flusso ricercabile, la posizione assoluta è indipendente dall'ora del flusso.

### <a name="queryinterface"></a>QueryInterface

La classe [**CSourceSeeking**](csourceseeking.md) implementa l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Per esporre questa interfaccia ai client, eseguire l'override del metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) :


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



Il metodo è denominato "non Delegating" a causa del modo in cui le classi base DirectShow supportano l'aggregazione Component Object Model (COM). Per ulteriori informazioni, vedere l'argomento "come implementare IUnknown" in DirectShow SDK.

### <a name="seeking-methods"></a>Metodi di ricerca

La classe [**CSourceSeeking**](csourceseeking.md) gestisce diverse variabili membro relative alla ricerca.



| Variabile          | Descrizione   | Valore predefinito  |
|-------------------|---------------|----------------|
| *\_rtStart m*      | Ora di inizio    | Zero           |
| *\_rtStop m*       | Ora di arresto     | \_I64 \_ Max/2 |
| *\_dRateSeeking m* | Velocità di riproduzione | 1.0            |



 

L'implementazione [**CSourceSeeking**](csourceseeking.md) di [**IMediaSeeking:: sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) aggiorna le ore di inizio e di fine e quindi chiama due metodi virtuali puri sulla classe derivata, [**CSourceSeeking:: iniziale**](csourceseeking-changestart.md) e [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md). L'implementazione di [**IMediaSeeking:: serate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) è simile: aggiorna la velocità di riproduzione e quindi chiama il metodo virtuale puro [**CSourceSeeking:: changere**](csourceseeking-changerate.md). In ognuno di questi metodi virtuali il PIN deve eseguire le operazioni seguenti:

1.  Chiamare [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) per avviare lo scaricamento dei dati.
2.  Arrestare il thread di streaming.
3.  Chiamare [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
4.  Riavviare il thread di streaming.
5.  Chiamare [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).
6.  Impostare il flag di discontinuità nell'esempio successivo.

L'ordine di questi passaggi è fondamentale, perché il thread di streaming può bloccarsi durante l'attesa del recapito di un campione o ottenere un nuovo esempio. Il metodo [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garantisce che il thread di streaming non sia bloccato e pertanto non verrà generato un deadlock nel passaggio 2. La chiamata a [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informa i filtri downstream per prevedere nuovi esempi, in modo che non li rifiuti quando il thread viene riavviato nel passaggio 4.

Il metodo privato seguente esegue i passaggi da 1 a 4:


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



Quando il thread di streaming viene riavviato, chiama il metodo [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) . Eseguire l'override di questo metodo per eseguire i passaggi 5 e 6:


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



Nel metodo [**iniziale**](csourceseeking-changestart.md) impostare la durata del flusso su zero e la posizione della palla sulla nuova ora di inizio. Quindi, chiamare CBallStream:: UpdateFromSeek:


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



Nel metodo [**ChangeStop**](csourceseeking-changestop.md) chiamare CBallStream:: UpdateFromSeek se la nuova ora di arresto è inferiore alla posizione corrente. In caso contrario, l'ora di arresto è ancora in futuro, quindi non è necessario scaricare il grafo.


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



Per le modifiche alla frequenza, il metodo [**CSourceSeeking::**](csourceseeking-setrate.md) SetValue imposta *m \_ dRateSeeking* sulla nuova frequenza (eliminando il valore precedente) prima di chiamare [**changere**](csourceseeking-changerate.md). Sfortunatamente, se il chiamante ha assegnato una frequenza non valida, ad esempio minore di zero, è troppo tardi per chiamare il **juke** -time. Una soluzione consiste nell'eseguire l'override di **bitrate** e verificare la validità delle tariffe:


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



### <a name="drawing-in-the-buffer"></a>Disegno nel buffer

Di seguito è illustrata la versione modificata di [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md), la routine che disegna la palla in ogni frame:


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



Le differenze principali tra questa versione e quella originale sono le seguenti:

-   Come indicato in precedenza, la variabile *m \_ rtBallPosition* viene utilizzata per impostare la posizione della palla anziché l'ora del flusso.
-   Dopo aver tenuto la sezione critica, il metodo controlla se la posizione corrente supera l'ora di arresto. In caso affermativo, **restituisce \_ false**, che segnala alla classe di base di arrestare l'invio di dati e recapitare una notifica di fine del flusso.
-   I timestamp sono divisi per la frequenza corrente.
-   Se *m \_ BDiscontinuity* è **true**, il metodo imposta il flag di discontinuità nell'esempio.

C'è un'altra differenza minore. Poiché la versione originale si basa su un solo buffer, riempie l'intero buffer con zeri una volta, all'inizio del flusso. Dopodiché, cancella solo la palla dalla posizione precedente. Tuttavia, questa ottimizzazione rivela un lieve bug nel filtro palla. Quando il metodo [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) chiama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), imposta il flag di sola lettura su **false**. Di conseguenza, il filtro downstream è libero di scrivere nel buffer. Una soluzione consiste nell'eseguire l'override di **DecideAllocator** in modo da impostare il flag di sola lettura su **true**. Per semplicità, tuttavia, la nuova versione consente semplicemente di rimuovere completamente l'ottimizzazione. Questa versione riempie invece il buffer con zeri ogni volta.

### <a name="miscellaneous-changes"></a>Modifiche varie

Nella nuova versione queste due righe vengono rimosse dal Costruttore CBall:


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



Il filtro palla originale usa questi valori per aggiungere la casualità alla posizione iniziale della palla. Per questo scopo, è necessario che la palla sia deterministica. Inoltre, alcune variabili sono state modificate dagli oggetti [**CRefTime**](creftime.md) alle [**variabili \_ temporali di riferimento**](reference-time.md) . La classe **CRefTime** è un wrapper sottile per un valore **di \_ ora di riferimento** . Infine, l'implementazione di [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) è stata modificata leggermente; per informazioni dettagliate, è possibile fare riferimento al codice sorgente.

## <a name="limitations-of-the-csourceseeking-class"></a>Limitazioni della classe CSourceSeeking

La classe [**CSourceSeeking**](csourceseeking.md) non è destinata ai filtri con più pin di output, a causa di problemi di comunicazione tra pin. Si supponga, ad esempio, un filtro del parser che riceve un flusso audio-video Interleaved, suddivide il flusso nei componenti audio e video e recapita il video da un pin di output e audio da un altro. Entrambi i pin di output riceveranno ogni comando seek, ma il filtro deve cercare solo una volta per ogni comando seek. La soluzione consiste nel designare uno dei pin per controllare la ricerca e ignorare i comandi Seek ricevuti dall'altro pin.

Dopo il comando seek, tuttavia, entrambi i pin devono svuotare i dati. Per complicare ulteriormente il problema, il comando seek si verifica nel thread dell'applicazione, non nel thread di streaming. Pertanto, è necessario assicurarsi che nessuno dei due pin sia bloccato e in attesa della restituzione di una chiamata [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) oppure che sia possibile che si verifichi un deadlock. Per ulteriori informazioni sullo svuotamento thread-safe nei pin, vedere [thread e sezioni critiche](threads-and-critical-sections.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri di origine](writing-source-filters.md)
</dt> </dl>

 

 



