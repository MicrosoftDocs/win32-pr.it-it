---
description: I sink di supporto sono gli oggetti pipeline che ricevono dati multimediali.
ms.assetid: a0fbce1b-0a16-4449-9eca-906fd9056a1c
title: Sink di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9394cbfd49a631d59b9296202a2b6ca7a868869
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351246"
---
# <a name="media-sinks"></a>Sink di supporti

I *sink di supporto* sono gli oggetti pipeline che ricevono dati multimediali. Un sink multimediale è la destinazione di uno o più flussi multimediali. I sink di supporto rientrano in due categorie generali:

-   Un *renderer* è un sink multimediale che presenta i dati per la riproduzione. Il renderer video avanzato (EVR) consente di visualizzare i fotogrammi video e il renderer audio riproduce i flussi audio attraverso la scheda audio o altro dispositivo audio.

-   Un *sink di archivio* è un sink multimediale che scrive i dati in un file o in un'altra risorsa di archiviazione.

La differenza principale tra di essi è che un sink di archivio non utilizza i dati a una frequenza di riproduzione fissa. Scrive invece i dati ricevuti nel minor tempo possibile.

I sink di supporto espongono l'interfaccia [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) . Ogni sink multimediale contiene uno o più *sink di flusso*. Ogni sink di flusso riceve i dati da un flusso. I sink di flusso espongono l'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . In genere, un'applicazione non crea direttamente i sink di supporto. Al contrario, l'applicazione crea uno o più oggetti attivazione, che la sessione multimediale USA per creare il sink. Tutte le altre operazioni sul sink vengono gestite dalla sessione multimediale e l'applicazione non chiama alcun metodo sul sink multimediale o su uno dei sink di flusso. Per ulteriori informazioni sugli oggetti attivazione, vedere [oggetti Activation](activation-objects.md).

È necessario leggere la parte restante di questo argomento se si sta scrivendo un sink multimediale personalizzato o se si vuole usare direttamente un sink multimediale senza la sessione multimediale.

-   [Sink di flusso](#stream-sinks)
-   [Orologio di presentazione](#presentation-clock)
-   [Formati di flusso](#stream-formats)
-   [Flusso di dati](#data-flow)
-   [Indicatori](#markers)
-   [Modifiche di stato](#state-changes)
-   [Finalizzazione](#finalizing)
-   [Chiusura in corso](#shutting-down)
-   [Interfacce del sink multimediale](#media-sink-interfaces)
-   [Interfacce di sink di flusso](#stream-sink-interfaces)
-   [Eventi sink di flusso](#stream-sink-events)
-   [Argomenti correlati](#related-topics)

## <a name="stream-sinks"></a>Sink di flusso

Un sink multimediale può avere un numero fisso di sink di flusso oppure può supportare l'aggiunta e la rimozione di sink di flusso. Se dispone di un numero fisso di sink di flusso, il metodo [**IMFMediaSink:: getcaratteristiche**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) restituisce il \_ flag dei \_ flussi fissi MEDIASINK. In caso contrario, è possibile aggiungere e rimuovere i sink di flusso. Per aggiungere un nuovo sink di flusso, chiamare [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Per rimuovere un sink di flusso, chiamare [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). Il \_ flag dei \_ flussi fissi MEDIASINK indica che il sink multimediale non supporta questi due metodi. (Potrebbe supportare un altro modo per configurare il numero di flussi, ad esempio impostando i parametri di inizializzazione quando viene creato il sink). L'elenco dei sink di flusso viene ordinato. Per enumerarli in base al valore di indice, chiamare il metodo [**IMFMediaSink:: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) .

I sink di flusso hanno anche identificatori. Gli identificatori di flusso sono univoci all'interno del sink multimediale, ma non devono essere consecutivi. A seconda del sink multimediale, gli identificatori di flusso possono avere un significato correlato al contenuto. Ad esempio, un sink di archivio potrebbe scrivere gli identificatori di flusso nell'intestazione del file. In caso contrario, sono arbitrari. Per ottenere un sink del flusso in base al relativo identificatore, chiamare [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid).

## <a name="presentation-clock"></a>Orologio di presentazione

La velocità con cui un sink multimediale utilizza gli esempi è controllata dal [clock di presentazione](presentation-clock.md). La sessione multimediale seleziona il clock di presentazione e lo imposta sul sink multimediale chiamando il metodo [**IMFMediaSink:: SetPresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock) del sink multimediale. Per poter iniziare lo streaming, è necessario impostare il clock di presentazione sul sink multimediale. Ogni sink multimediale richiede l'esecuzione di un clock di presentazione. Il sink multimediale usa il clock di presentazione per due scopi:

-   Per ricevere notifiche quando lo streaming viene avviato o interrotto. Il sink multimediale riceve queste notifiche tramite l'interfaccia [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) , che deve essere implementata da tutti i sink di supporto.

-   Per determinare quando eseguire il rendering degli esempi. Quando il sink multimediale riceve un nuovo esempio, ottiene il timestamp dall'esempio e tenta di eseguire il rendering dell'esempio in corrispondenza di tale ora di presentazione.

Il clock di presentazione deriva i tempi di clock da un altro oggetto chiamato *origine dell'ora di presentazione*. Le origini dell'ora di presentazione espongono l'interfaccia [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . Alcuni sink di supporto hanno accesso a un clock accurato, quindi espongono questa interfaccia. Ciò significa che un sink multimediale può pianificare campioni rispetto a un'ora fornita dal proprio clock. Tuttavia, il sink multimediale non può presupporre che questo sia il caso. Deve sempre usare l'ora dal clock di presentazione, indipendentemente dal fatto che il clock di presentazione sia determinato dal sink multimediale stesso o da un altro Clock.

Se un sink multimediale non è in grado di trovare corrispondenze con un clock diverso da se stesso, [**il metodo**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) GetProperties restituisce MEDIASINK \_ non può \_ corrispondere al \_ flag Clock. Se questo flag è presente e il clock di presentazione usa un'origine dell'ora di presentazione diversa, è probabile che il sink multimediale non venga eseguito correttamente. È possibile, ad esempio, che si sia verificato un problema durante la riproduzione.

Un sink *senza frequenza* è un sink multimediale che ignora i timestamp degli esempi e utilizza i dati non appena arrivano ogni campione. Un sink di supporto senza frequenza restituisce il \_ flag MEDIASINK senza frequenza dal metodo [**getcaratteristiche**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . In genere questo flag si applica ai sink di archivio. Se ogni sink multimediale nella pipeline è senza frequenza, la sessione multimediale usa un clock speciale di presentazione senza frequenza. Questo clock viene eseguito con la stessa velocità con cui i sink utilizzano esempi.

## <a name="stream-formats"></a>Formati di flusso

Prima che il sink multimediale possa ricevere esempi, il client deve impostare il tipo di supporto nei sink di flusso. Per impostare il tipo di supporto, chiamare il metodo [**IMFStreamSink:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler) del sink di flusso. Questo metodo restituisce un puntatore all'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) . Usare questa interfaccia per ottenere l'elenco dei tipi di supporto preferiti, ottenere il tipo di supporto corrente e impostare il tipo di supporto.

Per ottenere l'elenco dei tipi di supporto preferiti, chiamare [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex). I tipi preferiti devono essere presi come hint per il client. L'elenco potrebbe essere incompleto o includere tipi di supporti parziali. Un tipo di supporto parziale è uno che non include tutti gli attributi necessari per descrivere un formato valido. Ad esempio, un tipo di video parziale potrebbe specificare lo spazio di colore e la profondità del bit, ma non la larghezza o l'altezza dell'immagine. Un tipo audio parziale può specificare il formato di compressione e la frequenza di campionamento, ma non il numero di canali audio.

Per ottenere il tipo di supporto corrente del sink di flusso, chiamare [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Quando viene creato per la prima volta un sink del flusso, è possibile che sia già impostato un tipo di supporto predefinito oppure che non siano presenti tipi di supporti fino a quando il client non ne imposta uno.

Per impostare il tipo di supporto, chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Alcuni sink di flusso potrebbero non supportare la modifica del tipo dopo che è stato impostato. Pertanto, è utile testare i tipi di supporto prima di impostarli. Per verificare se il sink multimediale accetterà un tipo di supporto, ovvero senza impostare il tipo, chiamare [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).

## <a name="data-flow"></a>Flusso di dati

I sink di supporto usano un *modello pull*, il che significa che il flusso sink richiede i dati necessari. Il client deve rispondere in modo tempestivo per evitare eventuali problemi.

Alcuni sink multimediali supportano la *preregistrazione*. La preregistrazione è il processo di assegnazione dei dati al sink multimediale prima dell'avvio del clock di presentazione. Se un sink multimediale supporta la preregistrazione, il sink del supporto espone l'interfaccia [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) e il metodo [**getcaratteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) restituisce il \_ flag di \_ preroll MEDIASINK può. La preregistrazione garantisce che il sink multimediale sia pronto a presentare il primo campione all'avvio del clock di presentazione. Si consiglia di preregistrare sempre il client se il sink multimediale lo supporta, perché può impedire problemi o interruzioni durante la riproduzione.

Il flusso di dati in un sink multimediale funziona nel modo seguente:

1.  Il client imposta i tipi di supporto e il clock di presentazione. Il sink multimediale si registra con il clock di presentazione per ricevere notifiche sulle modifiche dello stato dell'orologio.
2.  Facoltativamente, il client esegue una query per [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll). Se il sink multimediale espone questa interfaccia, il client chiama [**IMFMediaSinkPreroll:: NotifyPreroll**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasinkpreroll-notifypreroll). In caso contrario, il client passerà al passaggio 5.
3.  Ogni sink di flusso invia uno o più eventi [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) . In risposta a ognuno di questi eventi, il client ottiene il campione di dati successivo per tale flusso e chiama [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample).
4.  Quando ogni sink di flusso riceve un numero sufficiente di dati di preroll, invia un evento [MEStreamSinkPrerolled](mestreamsinkprerolled.md) .
5.  Il client chiama [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) per avviare il clock di presentazione.
6.  Il clock di presentazione notifica al sink multimediale che l'orologio viene avviato, chiamando [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).
7.  Per ottenere più dati, ogni sink di flusso invia eventi [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) . In risposta a ognuno di questi eventi, il client ottiene l'esempio successivo e chiama [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample). Questo passaggio viene ripetuto fino alla fine della presentazione.

La maggior parte dei sink di supporto elabora gli esempi in modo asincrono, quindi i sink di flusso possono inviare più di una richiesta di esempio alla volta.

Durante lo streaming, il client può chiamare [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) e [**IMFStreamSink:: Flush**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-flush) in qualsiasi momento. I marcatori sono descritti nella sezione successiva. Lo svuotamento causa il sink del flusso per eliminare tutti gli esempi in coda ma non ancora sottoposti a rendering.

## <a name="markers"></a>Indicatori

I marcatori consentono al client di indicare punti specifici nel flusso. Un marcatore è costituito dalle seguenti informazioni:

-   Tipo di marcatore, definito come membro dell'enumerazione [**del \_ \_ tipo di marcatore MFSTREAMSINK**](/windows/desktop/api/mfidl/ne-mfidl-mfstreamsink_marker_type) .
-   Dati associati al marcatore. Il significato dei dati dipende dal tipo di marcatore. Alcuni tipi di marcatore non contengono dati.
-   Dati facoltativi per l'uso da parte del client.

Per inserire un marcatore, il client chiama [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker). Il sink di flusso completa l'elaborazione di tutti gli esempi ricevuti prima della chiamata del **segnaposto** e quindi Invia un evento [MEStreamSinkMarker](mestreamsinkmarker.md) .

La maggior parte dei sink multimediali mantiene una coda di esempi in sospeso, elaborati in modo asincrono. Gli eventi del marcatore devono essere serializzati con l'elaborazione di esempio, in modo che il sink multimediale debba inserire i marcatori nella stessa coda. Si supponga, ad esempio, che il client effettua le chiamate al metodo seguenti:

1.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (esempio \# 1)
2.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (esempio \# 2)
3.  [**Segnaposto**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marcatore \# 1)
4.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (esempio \# 3)
5.  [**Segnaposto**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marcatore \# 2)

In questo esempio, il sink di flusso deve inviare l'evento [MEStreamSinkMarker](mestreamsinkmarker.md) per il marcatore \# 1 dopo l'elaborazione del campione \# 2 e l'evento per il marcatore \# 2 dopo l'elaborazione del campione \# 3.

Se il client Scarica un sink di flusso, il sink di flusso elabora immediatamente tutti i marcatori presenti nella coda. Imposta il codice di stato su E \_ Interrompi per questi eventi.

Alcuni marcatori contengono informazioni rilevanti per il sink multimediale:

-   **MFSTREAMSINK \_ INDICATORE \_** di selezione: indica la presenza di un gap nel flusso. L'esempio successivo sarà una discontinuità.
-   **MFSTREAMSINK \_ MARKER \_ ENDOFSEGMENT**: indica la fine di un segmento o la fine di un flusso. L'esempio successivo (se presente) potrebbe essere una discontinuità.
-   **MFSTREAMSINK \_ \_Evento marcatore**: contiene un evento. A seconda del tipo di evento e dell'implementazione del sink multimediale, il sink multimediale può gestire l'evento o ignorarlo.

## <a name="state-changes"></a>Modifiche di stato

Un sink multimediale riceve una notifica delle modifiche di stato nel clock di presentazione tramite l'interfaccia [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) del sink multimediale. Quando il client imposta il clock di presentazione, il sink multimediale chiama [**IMFPresentationClock:: AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) per registrarsi per le notifiche dall'orologio. Nella tabella seguente viene riepilogato il comportamento di un sink multimediale in risposta alle modifiche dello stato del clock.



| Modifica stato orologio                                         | Elaborazione di esempio                                                                                                                                                                                                                                             | Elaborazione indicatore                                                                                                                                                                                   |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | Elabora esempi il cui timestamp è uguale o successivo all'ora di inizio dell'orologio.                                                                                                                                                                              | Invia l'evento [MEStreamSinkMarker](mestreamsinkmarker.md) quando tutti gli esempi ricevuti prima del marcatore sono stati elaborati.                                                                 |
| [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause)     | Il sink multimediale può non riuscire [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) mentre è sospeso.<br/> Se il sink multimediale accetta esempi durante la pausa, deve accodarli fino al riavvio del clock. Non elaborare alcun campione in coda mentre è in pausa.<br/> | Se sono presenti esempi in coda, inserire i marcatori nella stessa coda. Invia l'evento marcatore quando il clock viene riavviato.<br/> In caso contrario, inviare immediatamente l'evento marcatore.<br/>                    |
| [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | Elaborare tutti gli esempi in coda durante la pausa, quindi considerare lo stesso [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).                                                                                                                         | Inviare gli eventi [MEStreamSinkMarker](mestreamsinkmarker.md) per i marcatori in coda (serializzati con elaborazione di esempio), quindi considerare lo stesso [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart). |
| [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | Elimina tutti gli esempi in coda. Altre chiamate a [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) possono avere esito negativo.                                                                                                                                                      | Invia gli eventi del marcatore in coda. Nelle chiamate successive a [**segnaposto**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker), inviare immediatamente l'evento marcatore.                                                              |



 

Inoltre, i sink di flusso devono inviare gli eventi seguenti quando hanno completato le transizioni di stato:

-   [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart), [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart): evento [MEStreamSinkStarted](mestreamsinkstarted.md)
-   [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause): evento [MEStreamSinkPaused](mestreamsinkpaused.md)
-   [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop): evento [MEStreamSinkStopped](mestreamsinkstopped.md)

## <a name="finalizing"></a>Finalizzazione

Alcuni sink di supporto richiedono un passaggio di elaborazione aggiuntivo dopo che l'ultimo campione è stato recapitato. In genere questo requisito si applica ai sink di archivio, che devono scrivere intestazioni o indici nel file. Se un sink multimediale richiede un'elaborazione finale, espone l'interfaccia [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) .

Quando il client recapita l'ultimo esempio, il client esegue una query per questa interfaccia. Se il sink multimediale supporta l'interfaccia, il client chiama [**IMFFinalizableMediaSink:: BeginFinalize**](/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize) per eseguire l'elaborazione finale in modo asincrono. Questo metodo segue il modello di Media Foundation asincrono standard, descritto in [metodi di callback asincroni](asynchronous-callback-methods.md). Il sink multimediale può presupporre che il client chiamerà **BeginFinalize**. La mancata chiamata di **BeginFinalize** può causare un file creato in modo non corretto.

## <a name="shutting-down"></a>Chiusura in corso

Quando il client viene eseguito tramite il sink multimediale, il client chiama [**IMFMediaSink:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown). All'interno di questo metodo, il sink multimediale dovrebbe interrompere i conteggi circolari dei riferimenti. In genere, vi saranno riferimenti circolari tra il sink multimediale e i sink del flusso.

Se si utilizza l'oggetto helper della coda di eventi per implementare [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator), chiamare [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) nella coda degli eventi. Questo metodo arresta la coda degli eventi e segnala a qualsiasi chiamante che è attualmente in attesa di un evento.

Dopo l'arresto, tutti i metodi sul sink multimediale restituiscono MF \_ E \_ Shutdown, ad eccezione dei metodi **IUnknown** .

## <a name="media-sink-interfaces"></a>Interfacce del sink multimediale

La tabella seguente elenca le interfacce standard che i sink di supporto possono esporre tramite **QueryInterface**. I sink di supporto possono anche esporre interfacce personalizzate.



| Interfaccia                                                      | Descrizione                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                           | Interfaccia principale per i sink di supporto. Obbligatorio.                                            |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                 | Utilizzato per notificare al sink multimediale quando lo stato dell'orologio di presentazione cambia. Obbligatorio.              |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)     | Implementare se il sink multimediale deve eseguire un passaggio di elaborazione finale. Facoltativo.                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                         | Implementare se il sink multimediale espone le interfacce del servizio. Facoltativo.                       |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)       | Implementare se il sink multimediale invia eventi. Facoltativo.                                     |
| [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)             | Implementare se il sink multimediale supporta la preroll. Facoltativo.                                     |
| [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) | Implementare se il sink multimediale può fornire un'origine dell'ora per il clock di presentazione. Facoltativo. |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                   | Implementare se il sink multimediale può regolare la qualità della riproduzione. Facoltativo.                          |



 

Facoltativamente, un sink multimediale può implementare l'interfaccia seguente come servizio.



| Interfaccia del servizio                        | Descrizione                                    |
|------------------------------------------|------------------------------------------------|
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) | Segnala l'intervallo di frequenze di riproduzione supportate. |



 

Per ulteriori informazioni sulle interfacce del servizio e [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), vedere [interfacce di servizio](service-interfaces.md).

## <a name="stream-sink-interfaces"></a>Interfacce di sink di flusso

I sink di flusso devono esporre le interfacce seguenti tramite **QueryInterface**.



| Interfaccia                                                | Descrizione                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)                   | Interfaccia principale per i sink di flusso. Obbligatorio.                                                      |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Accoda gli eventi. L'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) eredita questa interfaccia. Obbligatorio. |



 

Attualmente non sono definite interfacce del servizio per i sink di flusso.

## <a name="stream-sink-events"></a>Eventi sink di flusso

La tabella seguente elenca gli eventi definiti per i sink di flusso generici. I sink di flusso possono anche inviare eventi personalizzati non elencati qui.



| Event                                                                  | Descrizione                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)             | Il tipo di supporto del sink di flusso non è più valido. Facoltativo. |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                           | Un marcatore è stato elaborato. Obbligatorio.                          |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                           | Il sink del flusso è stato sospeso. Obbligatorio.                      |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                     | Il preroll è stato completato. Facoltativo.                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                 | La velocità di riproduzione del sink del flusso è cambiata. Facoltativo.       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)             | Viene richiesto un nuovo esempio. Obbligatorio.                       |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) | Una richiesta di scrub è stata completata. Facoltativo.                   |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                         | Sink di flusso avviato. Obbligatorio.                     |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                         | Il sink del flusso è stato arrestato. Obbligatorio.                     |



 

Attualmente non sono definiti eventi generici per i sink di supporto. Alcuni sink di supporto potrebbero inviare eventi personalizzati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




