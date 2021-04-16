---
description: Questo argomento descrive come scrivere un filtro di origine personalizzato per DirectShow.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Come scrivere un filtro di origine per DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87af99595a43c86be0e2f4ecaa51768a211e9674
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522521"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Come scrivere un filtro di origine per DirectShow

Questo argomento descrive come scrivere un filtro di origine personalizzato per DirectShow.

> [!Note]  
> Questo argomento descrive solo le origini push; non descrive le origini pull, ad esempio il filtro di lettura asincrono, o i filtri splitter che si connettono alle origini di pull. Per la distinzione tra le origini *push* e *pull* , vedere [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>Modello di streaming DirectShow

Quando si scrive un filtro di origine, è importante comprendere che un'origine push non è la stessa cosa di un'origine live. Un'origine live recupera i dati da un'origine esterna, ad esempio una fotocamera o un flusso di rete. In genere, un'origine live non è in grado di controllare la frequenza di dati in ingresso. Se i filtri downstream non utilizzano i dati in modo sufficientemente veloce, è necessario che l'origine elimini gli esempi.

Tuttavia, non è necessario che un'origine push sia un'origine live. Ad esempio, un'origine push può leggere i dati da un file locale. In tal caso, i filtri del renderer downstream determinano la velocità con cui i dati vengono utilizzati dall'origine, in base all'orologio di riferimento e ai timestamp di esempio. Il filtro di origine recapita i campioni il più rapidamente possibile, ma il flusso di dati effettivo viene limitato dai renderer. I meccanismi per il controllo del flusso di dati sono descritti in [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).

Ogni pin di output nel filtro di origine crea un thread denominato *thread di streaming*. Il pin fornisce esempi sul thread di streaming. In genere, tutte le operazioni di decodifica, elaborazione e rendering avvengono in questo thread, sebbene alcuni filtri downstream possano creare thread aggiuntivi per accodare gli esempi di output.

Il thread di streaming esegue un ciclo con la struttura seguente:

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Se non è disponibile alcun campione, il passaggio 1 si blocca fino a quando non viene reso disponibile un campione. Il passaggio 4 può anche bloccare; ad esempio, può bloccarsi quando il grafico è sospeso.

Il ciclo viene eseguito il più rapidamente possibile, ma è limitato dalla velocità con cui il filtro renderer esegue il rendering di ogni campione. Supponendo che il grafico di filtro disponga di un orologio di riferimento, la velocità è determinata dai tempi di presentazione degli esempi. Se non è presente alcun clock di riferimento, il renderer utilizza gli esempi il più rapidamente possibile.

## <a name="using-csource-and-csourcestream"></a>Uso di CSource e CSourceStream

Le classi base di DirectShow includono due classi che supportano le origini push: [**CSource**](csource.md) e [**CSourceStream**](csourcestream.md).

-   [**CSource**](csource.md) è la classe di base per il filtro e implementa l'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .
-   [**CSourceStream**](csourcestream.md) è la classe base per i pin di output e implementa l'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

### <a name="output-pins"></a>Pin di output

Un filtro di origine può avere più di un pin di output. Nel metodo del costruttore del filtro creare uno o più pin derivati da [**CSourceStream**](csourcestream.md) (un PIN per ogni flusso di output). Non è necessario archiviare i puntatori ai pin; i pin si aggiungono automaticamente al filtro quando vengono creati.

### <a name="output-formats"></a>Formati di output

Il pin di output gestisce la negoziazione del formato con i seguenti metodi di [**CSourceStream**](csourcestream.md) :



| Metodo                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetMediaType**](csourcestream-getmediatype.md)     | Ottiene un tipo di supporto dal pin di output. <br/> Il PIN deve proporre almeno un tipo di supporto, perché il filtro downstream potrebbe non proporre tipi. Nella maggior parte dei casi, il filtro downstream sarà un decodificatore o un renderer, a seconda che il filtro di origine fornisca dati compressi o non compressi. Un filtro renderer richiede in genere un tipo di supporto completo, contenente tutte le informazioni sul formato necessarie per eseguire il rendering del flusso. Per un decodificatore, la quantità di informazioni richiesta nel tipo di supporto dipende molto dal formato di codifica.<br/> |
| [**CheckMediaType**](csourcestream-checkmediatype.md) | Controlla se il pin di output accetta un determinato tipo di supporto. L'override di questo metodo è facoltativo, a seconda della modalità di implementazione di [**GetMediaType**](csourcestream-getmediatype.md).                                                                                                                                                                                                                                                                                                                                                                                                         |



 

Il metodo [**GetMediaType**](csourcestream-getmediatype.md) è sovraccarico:

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) accetta un solo parametro, un puntatore a un oggetto [**CMediaType**](cmediatype.md) .
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) accetta una variabile di indice e un puntatore a un oggetto [**CMediaType**](cmediatype.md) .

Se il pin di output del filtro di origine supporta esattamente un formato multimediale, è necessario eseguire l'override di (1) per inizializzare l'oggetto [**CMediaType**](cmediatype.md) con tale formato. Lasciare l'implementazione predefinita di (2) e lasciare anche l'implementazione predefinita di [**CheckMediaType**](csourcestream-checkmediatype.md).

Se il pin supporta più di un formato, eseguire l'override di (2). Inizializzare l'oggetto [**CMediaType**](cmediatype.md) in base al valore della variabile index. Il PIN deve restituire i formati come un elenco ordinato. In questo caso, è necessario anche eseguire l'override di [**CheckMediaType**](csourcestream-checkmediatype.md) per verificare il tipo di supporto in base all'elenco di formati.

Per i formati video non compressi, tenere presente che il filtro downstream può proporre formati con diversi valori stride. Il filtro deve accettare qualsiasi valore stride valido. Per ulteriori informazioni, vedere [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

È anche necessario eseguire l'override del metodo [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) virtuale puro. Utilizzare questo metodo per impostare le dimensioni dei buffer di esempio.

### <a name="streaming"></a>Streaming

La classe [**CSourceStream**](csourcestream.md) crea il thread di streaming per il PIN. La routine thread è implementata nel metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . Questo metodo chiama il metodo [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , virtual pure, che la classe derivata deve eseguire l'override. Questo metodo è il punto in cui il pin riempie il buffer con i dati. Se, ad esempio, il filtro recapita video non compressi, è possibile creare i fotogrammi video.

La classe base viene avviata automaticamente e arresta il ciclo dei thread al momento giusto, quando il filtro viene sospeso o interrotto. Quando si verifica questo problema, la classe [**CSourceStream**](csourcestream.md) chiama alcuni metodi per notificare la classe derivata:

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

È possibile eseguire l'override di questi metodi se è necessario aggiungere una gestione speciale. In caso contrario, le implementazioni predefinite restituiscono semplicemente **S \_ OK**.

## <a name="seeking"></a>La ricerca

Se si dispone di un filtro di origine con un pin di output, è possibile usare la classe [**CSourceSeeking**](csourceseeking.md) come punto di partenza per l'implementazione della ricerca. Ereditare la classe pin sia da [**CSourceStream**](csourcestream.md) che da **CSourceSeeking**.

> [!Note]  
> [**CSourceSeeking**](csourceseeking.md) non è consigliato per un filtro con più di un pin di output. Il problema principale è che solo un PIN deve rispondere alle richieste di ricerca. Questa operazione richiede in genere la comunicazione tra i pin e il filtro.

 

La classe [**CSourceSeeking**](csourceseeking.md) gestisce la velocità di riproduzione, l'ora di inizio, l'ora di arresto e la durata. La classe derivata deve impostare la durata e l'ora di arresto iniziali. Ogni volta che viene modificato uno di questi valori, viene chiamato il metodo [**CSourceSeeking:: changere**](csourceseeking-changerate.md), [**CSourceSeeking:: iniziale**](csourceseeking-changestart.md)o [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md) , a seconda dei casi. I metodi sono tutti metodi virtuali puri. La classe pin derivata esegue l'override di questi metodi per eseguire le operazioni seguenti:

1.  Chiamare [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin downstream. In questo modo, i filtri downstream rilasciano campioni che contengono e rifiutano i nuovi esempi.
2.  Chiamare [**CSourceStream:: Stop**](csourcestream-stop.md) per arrestare il thread di streaming. Il filtro di origine sospende la produzione di nuovi dati.
3.  Chiamare [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin downstream. Ciò segnala ai filtri downstream di accettare nuovi dati.
4.  Chiamare [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) con la nuova frequenza e gli orari di inizio e di fine.
5.  Impostare la proprietà discontinuità nell'esempio successivo.

Per ulteriori informazioni, vedere [supporto della ricerca in un filtro di origine](supporting-seeking-in-a-source-filter.md).

Se il filtro supporta la ricerca, la posizione del flusso è ora indipendente dall'ora di presentazione. Dopo una ricerca, i timestamp vengono reimpostati su zero. La formula generale per gli indicatori temporali è:

-   ora di inizio di esempio = frequenza tempo trascorso/riproduzione
-   ora di fine campione = ora di inizio di esempio + (tempo per fotogramma/frequenza di riproduzione)

dove *tempo trascorso* è il tempo trascorso dall'avvio dell'esecuzione del filtro o dall'ultimo comando seek.

### <a name="time-formats-for-seeking"></a>Formati di ora per la ricerca

Per impostazione predefinita, i comandi Seek si trovano in unità di 100-nanosecondi. Il filtro di origine può supportare formati di ora aggiuntivi, ad esempio la ricerca in base al numero di frame. Ogni formato di ora è identificato da un GUID. vedere [**GUID del formato ora**](time-format-guids.md).

Per supportare formati di ora aggiuntivi, è necessario implementare i metodi seguenti sul pin di output:

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Se l'applicazione imposta un nuovo formato ora, tutti i parametri position nei metodi [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) vengono interpretati in base al nuovo formato di ora. Se, ad esempio, il formato dell'ora è frames, il metodo [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) deve restituire la durata nei frame.

In pratica, pochi filtri DirectShow supportano formati di ora aggiuntivi e, di conseguenza, alcune applicazioni DirectShow utilizzano questa funzionalità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri di origine](writing-source-filters.md)
</dt> </dl>

 

 




