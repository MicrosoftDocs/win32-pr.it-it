---
description: Questo argomento descrive come implementare la ricerca in un filtro di origine DirectShow Microsoft. Usa l'esempio di filtro palla come punto di partenza e descrive il codice aggiuntivo necessario per supportare la ricerca in questo filtro.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Supporto della ricerca in un filtro di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92c52ff4bde3ea75b156e5521af9825b0902df38f0d0c6bc23cc7be99c37a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072355"
---
# <a name="supporting-seeking-in-a-source-filter"></a>Supporto della ricerca in un filtro di origine

Questo argomento descrive come implementare la ricerca in un filtro di origine DirectShow Microsoft. Usa [l'esempio di filtro palla](ball-filter-sample.md) come punto di partenza e descrive il codice aggiuntivo necessario per supportare la ricerca in questo filtro.

[L'esempio di filtro](ball-filter-sample.md) palla è un filtro di origine che crea una palla da gioco animata. Questo articolo descrive come aggiungere funzionalità di ricerca a questo filtro. Dopo aver aggiunto questa funzionalità, è possibile eseguire il rendering del filtro in GraphEdit e controllare la palla trascinando il dispositivo di scorrimento GraphEdit.

In questo argomento sono incluse le sezioni seguenti:

-   [Panoramica della ricerca in DirectShow](#overview-of-seeking-in-directshow)
-   [Panoramica rapida del filtro palla](#quick-overview-of-the-ball-filter)
-   [Modifica del filtro palla per la ricerca](#modifying-the-ball-filter-for-seeking)
-   [Limitazioni della classe CSourceSeeking](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a>Panoramica della ricerca in DirectShow

Un'applicazione cerca il grafico dei filtri chiamando un [**metodo IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) in Filter Graph Manager. Filter Graph Manager distribuisce quindi la chiamata a ogni renderer nel grafico. Ogni renderer invia la chiamata upstream, tramite il pin di output del filtro upstream successivo. La chiamata si sposta a monte fino a raggiungere un filtro in grado di eseguire il comando seek, in genere un filtro di origine o un filtro parser. In generale, anche il filtro che ha origine i timestamp gestisce la ricerca.

Un filtro risponde a un comando seek come segue:

1.  Il filtro scarica il grafico. In questo modo vengono cancellati tutti i dati non obsoleti dal grafo, migliorando la velocità di risposta. In caso contrario, gli esempi memorizzati nel buffer prima del comando seek potrebbero essere recapitati.
2.  Il filtro chiama [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) per informare i filtri downstream della nuova ora di arresto, dell'ora di inizio e della velocità di riproduzione.
3.  Il filtro imposta quindi il flag di discontinuità nel primo esempio dopo il comando seek.

I timestamp iniziano da zero dopo qualsiasi comando seek (incluse le modifiche della frequenza).

## <a name="quick-overview-of-the-ball-filter"></a>Panoramica rapida del filtro palla

Il filtro Ball è un'origine push, il che significa che usa un thread di lavoro per distribuire i campioni a valle, anziché un'origine pull, che attende passivamente che un filtro downstream richiedi campioni. Il filtro Ball viene compilato dalla [**classe CSource**](csource.md) e il relativo pin di output viene compilato dalla [**classe CSourceStream.**](csourcestream.md) La **classe CSourceStream** crea il thread di lavoro che guida il flusso di dati. Questo thread entra in un ciclo che ottiene campioni dall'allocatore, li riempie di dati e li recapita a valle.

La maggior parte dell'azione in [**CSourceStream**](csourcestream.md) si verifica nel [**metodo CSourceStream::FillBuffer,**](csourcestream-fillbuffer.md) implementato dalla classe derivata. L'argomento di questo metodo è un puntatore all'esempio da recapitare. L'implementazione del filtro Ball di **FillBuffer** recupera l'indirizzo del buffer di esempio e disegna direttamente nel buffer impostando singoli valori in pixel. Il disegno viene eseguito da una classe helper, CBall, in modo che sia possibile ignorare i dettagli relativi alle profondità dei bit, alle tavolozze e così via.

## <a name="modifying-the-ball-filter-for-seeking"></a>Modifica del filtro palla per la ricerca

Per rendere il filtro Ball ricercabile, usare la [**classe CSourceSeeking,**](csourceseeking.md) progettata per l'implementazione della ricerca nei filtri con un pin di output. Aggiungere la **classe CSourceSeeking** all'elenco di ereditarietà per la classe CBallStream:


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



Sarà anche necessario aggiungere un inizializzatore per [**CSourceSeeking**](csourceseeking.md) al costruttore CBallStream:


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



Questa istruzione chiama il costruttore di base [**per CSourceSeeking.**](csourceseeking.md) I parametri sono un nome, un puntatore al pin proprietario, un **valore HRESULT** e l'indirizzo di un oggetto sezione critica. Il nome viene usato solo per il debug e la macro [**NAME**](name.md) viene compilata in una stringa vuota nelle build per la vendita al dettaglio. Il segnaposto eredita direttamente **CSourceSeeking,** quindi il secondo parametro è un puntatore a se stesso, di cui viene eseguito il cast a un [**puntatore IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin) Il **valore HRESULT** viene ignorato nella versione corrente delle classi di base. rimane per la compatibilità con le versioni precedenti. La sezione critica protegge i dati condivisi, ad esempio l'ora di inizio corrente, l'ora di arresto e la velocità di riproduzione.

Aggiungere l'istruzione seguente [**all'interno del costruttore CSourceSeeking:**](csourceseeking.md)


```C++
m_rtStop = 60 * UNITS;
```



La *variabile m \_ rtStop* specifica l'ora di arresto. Per impostazione predefinita, il valore è \_ I64 \_ MAX / 2, ovvero circa 14.600 anni. L'istruzione precedente lo imposta su un valore più conservativo di 60 secondi.

È necessario aggiungere altre due variabili membro a CBallStream:


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



Dopo ogni comando seek, il filtro deve impostare il flag di discontinuità nell'esempio successivo chiamando [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity). La *variabile \_ m bDiscontinuity* ne tiene traccia. La *variabile m \_ rtBallPosition* specifica la posizione della palla all'interno del fotogramma video. Il filtro Ball originale calcola la posizione dal tempo del flusso, ma l'ora del flusso viene reimpostata su zero dopo ogni comando di ricerca. In un flusso ricercabile, la posizione assoluta è indipendente dal tempo del flusso.

### <a name="queryinterface"></a>QueryInterface

La [**classe CSourceSeeking**](csourceseeking.md) implementa [**l'interfaccia IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) Per esporre questa interfaccia ai client, eseguire l'override [**del metodo NonDelegatingQueryInterface:**](cunknown-nondelegatingqueryinterface.md)


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



Il metodo è denominato "NonDelegating" a causa del modo in cui le classi di base DirectShow supportano l'aggregazione Component Object Model (COM). Per altre informazioni, vedere l'argomento "Come implementare IUnknown" in DirectShow SDK.

### <a name="seeking-methods"></a>Metodi di ricerca

La [**classe CSourceSeeking**](csourceseeking.md) gestisce diverse variabili membro relative alla ricerca.



| Variabile          | Descrizione   | Valore predefinito  |
|-------------------|---------------|----------------|
| *m \_ rtStart*      | Ora di inizio    | Zero           |
| *m \_ rtStop*       | Ora di arresto     | \_I64 \_ MAX / 2 |
| *m \_ dRateSeeking* | Velocità di riproduzione | 1.0            |



 

L'implementazione [**CSourceSeeking**](csourceseeking.md) di [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) aggiorna l'ora di inizio e di arresto e quindi chiama due metodi virtuali puri sulla classe derivata, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) e [**CSourceSeeking::ChangeStop.**](csourceseeking-changestop.md) L'implementazione di [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) è simile: aggiorna la velocità di riproduzione e quindi chiama il metodo virtuale [**puro CSourceSeeking::ChangeRate**](csourceseeking-changerate.md). In ognuno di questi metodi virtuali, il pin deve eseguire le operazioni seguenti:

1.  Chiamare [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) per avviare lo scaricamento dei dati.
2.  Arrestare il thread di streaming.
3.  Chiamare [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
4.  Riavviare il thread di streaming.
5.  Chiamare [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).
6.  Impostare il flag di discontinuità nell'esempio successivo.

L'ordine di questi passaggi è fondamentale, perché il thread di streaming può bloccarsi mentre è in attesa di distribuire un campione o ottenere un nuovo campione. Il [**metodo BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garantisce che il thread di streaming non sia bloccato e pertanto non si verifica un deadlock nel passaggio 2. La [**chiamata EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informa i filtri downstream di prevedere nuovi esempi, quindi non li rifiuta quando il thread viene avviato nuovamente nel passaggio 4.

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



Quando il thread di streaming viene avviato di nuovo, chiama il [**metodo CSourceStream::OnThreadStartPlay.**](csourcestream-onthreadstartplay.md) Eseguire l'override di questo metodo per eseguire i passaggi 5 e 6:


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



Nel metodo [**ChangeStart**](csourceseeking-changestart.md) impostare l'ora del flusso su zero e la posizione della palla sulla nuova ora di inizio. Chiamare quindi CBallStream::UpdateFromSeek:


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



Nel metodo [**ChangeStop**](csourceseeking-changestop.md) chiamare CBallStream::UpdateFromSeek se la nuova ora di arresto è inferiore alla posizione corrente. In caso contrario, l'ora di arresto è ancora in futuro, quindi non è necessario scaricare il grafico.


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



Per le modifiche della frequenza, il metodo [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) imposta *m \_ dRateSeeking* sulla nuova frequenza (rimuovendo il valore precedente) prima che [**chiami ChangeRate.**](csourceseeking-changerate.md) Sfortunatamente, se il chiamante ha dato una frequenza non valida, ad esempio minore di zero, è troppo tardi quando viene chiamato **ChangeRate.** Una soluzione consiste nell'eseguire l'override **di SetRate** e verificare le tariffe valide:


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

Ecco la versione modificata di [**CSourceStream::FillBuffer,**](csourcestream-fillbuffer.md)la routine che disegna la palla su ogni fotogramma:


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



Le principali differenze tra questa versione e quella originale sono le seguenti:

-   Come accennato in precedenza, la variabile *m \_ rtBallPosition* viene usata per impostare la posizione della palla, anziché il tempo del flusso.
-   Dopo aver posizionato la sezione critica, il metodo verifica se la posizione corrente supera il tempo di arresto. In tal caso, restituisce **S \_ FALSE,** che segnala alla classe di base di interrompere l'invio di dati e recapitare una notifica di fine flusso.
-   I timestamp sono divisi per la frequenza corrente.
-   Se *m \_ bDiscontinuity* **è TRUE,** il metodo imposta il flag di discontinuità nell'esempio.

Esiste un'altra differenza secondaria. Poiché la versione originale si basa esattamente su un buffer, riempie l'intero buffer con zeri una sola volta, all'avvio dello streaming. Successivamente, cancella semplicemente la palla dalla posizione precedente. Tuttavia, questa ottimizzazione rivela un leggero bug nel filtro Palla. Quando il [**metodo CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md) chiama [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), imposta il flag di sola lettura su **FALSE.** Di conseguenza, il filtro downstream è libero di scrivere nel buffer. Una soluzione consiste nell'eseguire l'override **di DecideAllocator** in modo da impostare il flag di sola lettura su **TRUE.** Per semplicità, tuttavia, la nuova versione rimuove completamente l'ottimizzazione. Questa versione riempie invece il buffer con zeri ogni volta.

### <a name="miscellaneous-changes"></a>Modifiche varie

Nella nuova versione queste due righe vengono rimosse dal costruttore CBall:


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



Il filtro Ball originale usa questi valori per aggiungere una certa casualità alla posizione iniziale della palla. Per i nostri scopi, si vuole che la palla sia deterministica. Inoltre, alcune variabili sono state modificate dagli [**oggetti CRefTime**](creftime.md) alle [**variabili REFERENCE \_ TIME.**](reference-time.md) La **classe CRefTime** è un thin wrapper per un **valore REFERENCE \_ TIME.** Infine, l'implementazione [**di IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) è stata modificata leggermente. È possibile fare riferimento al codice sorgente per informazioni dettagliate.

## <a name="limitations-of-the-csourceseeking-class"></a>Limitazioni della classe CSourceSeeking

La [**classe CSourceSeeking**](csourceseeking.md) non è destinata ai filtri con più pin di output, a causa di problemi di comunicazione tra pin. Si supponga ad esempio un filtro del parser che riceve un flusso audio-video interleaved, suddivide il flusso nei relativi componenti audio e video e recapita video da un pin di output e audio da un altro. Entrambi i pin di output riceveranno ogni comando seek, ma il filtro deve cercare una sola volta per ogni comando seek. La soluzione consiste nel designare uno dei pin per controllare la ricerca e ignorare i comandi di ricerca ricevuti dall'altro pin.

Dopo il comando seek, tuttavia, entrambi i pin devono scaricare i dati. Per complicare ulteriormente le cose, il comando seek viene eseguito nel thread dell'applicazione, non nel thread di streaming. Pertanto, è necessario assicurarsi che nessuno dei due pin sia bloccato e in attesa della restituzione di una chiamata [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) oppure potrebbe causare un deadlock. Per altre informazioni sullo scaricamento thread-safe nei pin, vedere [Thread e sezioni critiche](threads-and-critical-sections.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri di origine](writing-source-filters.md)
</dt> </dl>

 

 



