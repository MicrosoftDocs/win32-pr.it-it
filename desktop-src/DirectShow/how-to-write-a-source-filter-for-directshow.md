---
description: Questo argomento descrive come scrivere un filtro di origine personalizzato per DirectShow.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Come scrivere un filtro di origine per DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ea6821dc7d56f2628ce68e7320e5e76b2c1643978e68287d434b7a111cbbd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043241"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Come scrivere un filtro di origine per DirectShow

Questo argomento descrive come scrivere un filtro di origine personalizzato per DirectShow.

> [!Note]  
> In questo argomento vengono descritte solo le origini push. non descrive le origini pull, ad esempio il filtro lettore asincrono o i filtri della barra di divisione che si connettono alle origini pull. Per la distinzione tra *origini push* *e pull,* vedere [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>Modello DirectShow streaming

Quando si scrive un filtro di origine, è importante comprendere che un'origine push non corrisponde a un'origine live. Un'origine live ottiene i dati da un'origine esterna, ad esempio una fotocamera o un flusso di rete. In genere, un'origine in tempo reale non può controllare la velocità in ingresso dei dati. Se i filtri downstream non utilizzano i dati abbastanza velocemente, l'origine dovrà eliminare i campioni.

Tuttavia, un'origine push non deve essere un'origine live. Ad esempio, un'origine push può leggere i dati da un file locale. In tal caso, i filtri del renderer downstream determinano la velocità di utilizzo dei dati dall'origine, in base all'orologio di riferimento e ai timestamp di esempio. Il filtro di origine fornisce gli esempi il più rapidamente possibile, ma il flusso di dati effettivo è limitato dai renderer. I meccanismi per la gestione del flusso di dati sono descritti in [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

Ogni pin di output nel filtro di origine crea un thread denominato *thread di streaming.* Il pin recapita esempi sul thread di streaming. In genere, tutte le operazioni di decodifica, elaborazione e rendering si verificano in questo thread, anche se alcuni filtri downstream potrebbero creare thread aggiuntivi per accodare i campioni di output.

Il thread di streaming esegue un ciclo con la struttura seguente:

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Se non sono disponibili esempi, il passaggio 1 si blocca finché non diventa disponibile un campione. Il passaggio 4 può anche bloccare. Ad esempio, può bloccarsi mentre il grafo è in pausa.

Il ciclo viene eseguito il più rapidamente possibile, ma è limitato dalla velocità con cui il filtro del renderer esegue il rendering di ogni campione. Supponendo che il grafico dei filtri abbia un clock di riferimento, la frequenza è determinata dagli orari di presentazione degli esempi. Se non è presente alcun clock di riferimento, il renderer utilizza gli esempi il più rapidamente possibile.

## <a name="using-csource-and-csourcestream"></a>Uso di CSource e CSourceStream

Le DirectShow di base includono due classi che supportano le origini push: [**CSource**](csource.md) e [**CSourceStream**](csourcestream.md).

-   [**CSource**](csource.md) è la classe di base per il filtro e implementa [**l'interfaccia IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)
-   [**CSourceStream è**](csourcestream.md) la classe di base per i pin di output e implementa [**l'interfaccia IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

### <a name="output-pins"></a>Pin di output

Un filtro di origine può avere più di un pin di output. Nel metodo del costruttore del filtro creare uno o più pin derivati da [**CSourceStream**](csourcestream.md) (un pin per flusso di output). Non è necessario archiviare puntatori ai pin. i segnaposto si aggiungono automaticamente al filtro quando vengono creati.

### <a name="output-formats"></a>Formati di output

Il pin di output gestisce la negoziazione del formato con i metodi [**CSourceStream**](csourcestream.md) seguenti:



| Metodo                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetMediaType**](csourcestream-getmediatype.md)     | Ottiene un tipo di supporto dal pin di output. <br/> Il pin deve proporre almeno un tipo di supporto, perché il filtro downstream potrebbe non proporre alcun tipo. Nella maggior parte dei casi, il filtro downstream sarà un decodificatore o un renderer, a seconda che il filtro di origine consegnerà dati compressi o non compressi. Un filtro renderer richiede in genere un tipo di supporto completo, contenente tutte le informazioni sul formato necessarie per eseguire il rendering del flusso. Per un decodificatore, la quantità di informazioni necessarie nel tipo di supporto dipende molto dal formato di codifica.<br/> |
| [**CheckMediaType**](csourcestream-checkmediatype.md) | Verifica se il pin di output accetta un tipo di supporto specificato. L'override di questo metodo è facoltativo, a seconda della modalità di implementazione [**di GetMediaType.**](csourcestream-getmediatype.md)                                                                                                                                                                                                                                                                                                                                                                                                         |



 

Il [**metodo GetMediaType**](csourcestream-getmediatype.md) è sottoposto a overload:

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) accetta un singolo parametro, un puntatore a un [**oggetto CMediaType.**](cmediatype.md)
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) accetta una variabile di indice e un puntatore a un [**oggetto CMediaType.**](cmediatype.md)

Se il pin di output del filtro di origine supporta esattamente un formato multimediale, è necessario eseguire l'override di (1) per inizializzare l'oggetto [**CMediaType**](cmediatype.md) con tale formato. Lasciare l'implementazione predefinita di (2) e lasciare anche l'implementazione predefinita [**di CheckMediaType**](csourcestream-checkmediatype.md).

Se il pin supporta più di un formato, eseguire l'override (2). Inizializzare [**l'oggetto CMediaType**](cmediatype.md) in base al valore della variabile di indice. Il segnaposto deve restituire i formati come elenco ordinato. In questo caso, è anche necessario eseguire l'override di [**CheckMediaType**](csourcestream-checkmediatype.md) per controllare il tipo di supporto rispetto all'elenco di formati.

Per i formati video non compressi, tenere presente che il filtro downstream può proporre formati con vari valori stride. Il filtro deve accettare qualsiasi valore stride valido. Per altre informazioni, vedere [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

È anche necessario eseguire l'override del metodo [**CBaseOutputPin::D ecideBufferSize puramente**](cbaseoutputpin-decidebuffersize.md) virtuale. Usare questo metodo per impostare le dimensioni dei buffer di esempio.

### <a name="streaming"></a>Streaming

La [**classe CSourceStream**](csourcestream.md) crea il thread di streaming per il pin. La routine del thread viene implementata nel metodo [**CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) Questo metodo chiama il metodo [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) puro virtuale di cui la classe derivata deve eseguire l'override. Questo metodo è il punto in cui il segnaposto riempie il buffer con dati. Ad esempio, se il filtro recapita video non compresso, è qui che si disegnano i fotogrammi video.

La classe di base avvia e arresta automaticamente il ciclo di thread al momento giusto, quando il filtro viene sospeso o arrestato. In questo caso, la [**classe CSourceStream**](csourcestream.md) chiama alcuni metodi per notificare la classe derivata:

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

È possibile eseguire l'override di questi metodi se è necessario aggiungere una gestione speciale. In caso contrario, le implementazioni predefinite restituiscono **semplicemente S \_ OK.**

## <a name="seeking"></a>riercare

Se si dispone di un filtro di origine con un pin di output, è possibile usare la [**classe CSourceSeeking**](csourceseeking.md) come punto di partenza per l'implementazione della ricerca. Ereditare la classe pin [**da CSourceStream**](csourcestream.md) e **CSourceSeeking**.

> [!Note]  
> [**CSourceSeeking**](csourceseeking.md) non è consigliato per un filtro con più di un pin di output. Il problema principale è che un solo pin deve rispondere alle richieste di ricerca. Questa operazione richiede in genere la comunicazione tra i pin e il filtro.

 

La [**classe CSourceSeeking**](csourceseeking.md) gestisce la velocità di riproduzione, l'ora di inizio, l'ora di arresto e la durata. La classe derivata deve impostare il tempo di arresto iniziale e la durata. Ogni volta che uno di questi valori viene modificato, viene chiamato il metodo [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md), [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)o [**CSourceSeeking::ChangeStop,**](csourceseeking-changestop.md) in base alle esigenze. I metodi sono tutti metodi virtuali puri. La classe pin derivata esegue l'override di questi metodi per eseguire le operazioni seguenti:

1.  Chiamare [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin downstream. In questo modo i filtri downstream rilasciano gli esempi in cui sono in possesso e rifiutano nuovi esempi.
2.  Chiamare [**CSourceStream::Stop per**](csourcestream-stop.md) arrestare il thread di streaming. Il filtro di origine sospende la produzione di nuovi dati.
3.  Chiamare [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin downstream. Ciò segnala ai filtri downstream di accettare nuovi dati.
4.  Chiamare [**IPin::NewSegment con**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) i nuovi orari di inizio e arresto e frequenza.
5.  Impostare la proprietà discontinuity nell'esempio successivo.

Per altre informazioni, vedere [Supporto della ricerca in un filtro di origine.](supporting-seeking-in-a-source-filter.md)

Se il filtro supporta la ricerca, la posizione del flusso è ora indipendente dall'ora di presentazione. Dopo una ricerca, i timestamp vengono reimpostati su zero. La formula generale per i timestamp è:

-   sample start time = time elapsed/playback rate
-   sample end time = sample start time + (time per frame/playback rate)

dove *tempo trascorso è il* tempo trascorso dall'avvio dell'esecuzione del filtro o dall'ultimo comando seek.

### <a name="time-formats-for-seeking"></a>Formati di ora per la ricerca

Per impostazione predefinita, i comandi seek sono in unità di 100 nanosecondi. Il filtro di origine può supportare formati di ora aggiuntivi, ad esempio la ricerca in base al numero di fotogramma. Ogni formato ora è identificato da un GUID. vedere [**GUID di formato ora**](time-format-guids.md).

Per supportare formati di ora aggiuntivi, è necessario implementare i metodi seguenti sul pin di output:

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Se l'applicazione imposta un nuovo formato ora, tutti i parametri di posizione nei metodi [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) vengono interpretati in termini di nuovo formato ora. Ad esempio, se il formato dell'ora è frames, il [**metodo IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) deve restituire la durata in fotogrammi.

In pratica, pochi filtri DirectShow supportano formati di ora aggiuntivi e, di conseguenza, poche applicazioni DirectShow usano questa funzionalità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri di origine](writing-source-filters.md)
</dt> </dl>

 

 




