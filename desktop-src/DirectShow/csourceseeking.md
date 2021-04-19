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
# <a name="csourceseeking-class"></a>Classe CSourceSeeking

![gerarchia di classi csourceseeking](images/cutil15.png)

La classe **CSourceSeeking** è una classe astratta per l'implementazione della ricerca nei filtri di origine con un pin di output.

Questa classe supporta l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Fornisce le implementazioni predefinite per tutti i metodi **IMediaSeeking** . Le variabili membro protette memorizzano l'ora di inizio, l'ora di arresto e la frequenza corrente. Per impostazione predefinita, l'unico formato di ora supportato dalla classe **è \_ \_ Time Format Media \_ time** (unità di 100-nanosecondi). Per ulteriori informazioni, vedere la sezione Osservazioni.



| Variabili membro protette                                          | Descrizione                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_rtDuration m**](csourceseeking-m-rtduration.md)                | Durata del flusso.                                                                     |
| [**\_rtStart m**](csourceseeking-m-rtstart.md)                      | Ora di inizio.                                                                                 |
| [**\_rtStop m**](csourceseeking-m-rtstop.md)                        | Ora di arresto.                                                                                  |
| [**\_dRateSeeking m**](csourceseeking-m-drateseeking.md)            | Velocità di riproduzione.                                                                              |
| [**\_dwSeekingCaps m**](csourceseeking-m-dwseekingcaps.md)          | Funzionalità di ricerca.                                                                       |
| [**\_pLock m**](csourceseeking-m-plock.md)                          | Puntatore a un oggetto sezione critica per il blocco.                                           |
| Metodi protetti                                                   | Descrizione                                                                                 |
| [**CSourceSeeking**](csourceseeking-csourceseeking.md)             | Metodo del costruttore.                                                                         |
| Metodi virtuali puri                                                | Descrizione                                                                                 |
| [**Modificatore**](csourceseeking-changerate.md)                     | Chiamato quando cambia la velocità di riproduzione.                                                      |
| [**Iniziale**](csourceseeking-changestart.md)                   | Chiamato quando cambia la posizione iniziale.                                                     |
| [**ChangeStop**](csourceseeking-changestop.md)                     | Chiamato quando cambia la posizione di arresto.                                                      |
| Metodi IMediaSeeking                                               | Descrizione                                                                                 |
| [**IsFormatSupported**](csourceseeking-isformatsupported.md)       | Determina se è supportato un formato di ora specificato.                                    |
| [**QueryPreferredFormat**](csourceseeking-querypreferredformat.md) | Recupera il formato di ora preferito dell'oggetto.                                               |
| [**SetTimeFormat**](csourceseeking-settimeformat.md)               | Imposta il formato dell'ora.                                                                       |
| [**IsUsingTimeFormat**](csourceseeking-isusingtimeformat.md)       | Determina se un formato di ora specificato è il formato attualmente in uso.                  |
| [**GetTimeFormat**](csourceseeking-gettimeformat.md)               | Recupera il formato dell'ora corrente.                                                          |
| [**GetDuration**](csourceseeking-getduration.md)                   | Recupera la durata del flusso.                                                       |
| [**GetStopPosition**](csourceseeking-getstopposition.md)           | Recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso. |
| [**GetCurrentPosition**](csourceseeking-getcurrentposition.md)     | Recupera la posizione corrente rispetto alla durata totale del flusso.               |
| [**GetCapabilities**](csourceseeking-getcapabilities.md)           | Recupera tutte le funzionalità di ricerca del flusso.                                       |
| [**CheckCapabilities**](csourceseeking-checkcapabilities.md)       | Esegue una query se il flusso ha specificato funzionalità di ricerca.                              |
| [**ConvertTimeFormat**](csourceseeking-converttimeformat.md)       | Esegue la conversione da un formato di ora a un altro.                                                   |
| [**Posizioni**](csourceseeking-setpositions.md)                 | Imposta la posizione corrente e la posizione di arresto.                                            |
| [**GetPositions**](csourceseeking-getpositions.md)                 | Recupera la posizione corrente e la posizione di arresto.                                       |
| [**GetAvailable**](csourceseeking-getavailable.md)                 | Recupera l'intervallo di tempo in cui la ricerca è efficiente.                                 |
| [**Frequenza**](csourceseeking-setrate.md)                           | Imposta la velocità di riproduzione.                                                                     |
| [**Getrate**](csourceseeking-getrate.md)                           | Recupera la velocità di riproduzione.                                                                |
| [**GetPreroll**](csourceseeking-getpreroll.md)                     | Recupera l'ora di preregistrazione.                                                                 |



 

## <a name="remarks"></a>Commenti

Ogni volta che viene modificata la posizione iniziale, la posizione di arresto o la frequenza di riproduzione, l'oggetto **CSourceSeeking** chiama un metodo virtuale puro corrispondente:

-   Posizione iniziale: [ **CSourceSeeking:: iniziale**](csourceseeking-changestart.md)
-   Posizione stop: [ **CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md)
-   Velocità di riproduzione: [ **CSourceSeeking:: Changer**](csourceseeking-changerate.md)

La classe derivata deve implementare questi metodi. Dopo qualsiasi operazione di ricerca, un filtro deve eseguire le operazioni seguenti:

1.  Chiamare il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input downstream.
2.  Arrestare il thread di lavoro che fornisce i dati.
3.  Chiamare il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.
4.  Riavviare il thread di lavoro.
5.  Chiamare il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sul pin di input.
6.  Impostare la proprietà discontinuità nel primo esempio. Chiamare il metodo [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

La chiamata a [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) libera il thread di lavoro, se il thread è bloccato in attesa di recapitare un campione.

Nel passaggio 2, verificare che il thread abbia interrotto l'invio dei dati. A seconda dell'implementazione, potrebbe essere necessario attendere che il thread venga chiuso o che il thread segnali una risposta di qualche tipo. Se il filtro usa la classe [**CSourceStream**](csourcestream.md) , il metodo [**CSourceStream:: Stop**](csourcestream-stop.md) si blocca fino a quando il thread di lavoro non risponde.

Idealmente, il nuovo segmento (passaggio 5) deve essere recapitato dal thread di lavoro. Può anche essere eseguita dall'oggetto **CSourceSeeking** , purché il filtro lo serializza con gli esempi.

Nell'esempio seguente viene illustrata una possibile implementazione di. Si presuppone che il pin di output del filtro di origine sia derivato da **CSourceSeeking** e [**CSourceStream**](csourcestream.md). Questo esempio definisce un metodo helper, UpdateFromSeek, che esegue i passaggi 1 4. Viene eseguito l'override del metodo [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) per inviare il nuovo segmento e impostare un flag che indica la discontinuità. Il thread di lavoro preleva questo flag e chiama il metodo [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :


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



### <a name="supporting-additional-time-formats"></a>Supporto di formati di ora aggiuntivi

Per impostazione predefinita, questa classe supporta la ricerca solo in unità di tempo di riferimento (tempo di supporto per il formato dell'ora \_ \_ \_ ). Per supportare formati di ora aggiuntivi, eseguire l'override dei metodi [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) che gestiscono i formati di ora:

-   [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Inoltre, eseguire l'override dei metodi [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) rimanenti per eseguire le conversioni necessarie tra i formati di ora. Dopo la chiamata del metodo [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) , tutti i metodi **IMediaSeeking** devono considerare i parametri temporali in entrata e in uscita come nel nuovo formato di ora. Se, ad esempio, la variabile *m \_ rtDuration* rappresenta la durata in unità di tempo di riferimento, ma il formato dell'ora corrente è frames, il metodo [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) deve restituire il valore *m \_ rtDuration* convertito in frame. Ad esempio:


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



Assicurarsi inoltre di verificare la presenza del \_ \_ flag ReturnTime seeking nel metodo [**IMediaSeeking:: sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) . Se questo flag è presente, convertire i valori di posizione in tempi di riferimento quando vengono restituiti al chiamante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto della ricerca in un filtro di origine](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




