---
description: Questo argomento descrive come implementare un'origine multimediale personalizzata in Microsoft Media Foundation.
ms.assetid: 82db6f32-ad94-4563-b8bd-8a5072c5b221
title: Scrittura di un'origine multimediale personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8769fa16d4dcbfd3438b66f9a9e78c34274735a5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320699"
---
# <a name="writing-a-custom-media-source"></a>Scrittura di un'origine multimediale personalizzata

Questo argomento descrive come implementare un'origine multimediale personalizzata in Microsoft Media Foundation. Contiene le sezioni seguenti:

-   [Creazione del descrittore della presentazione](#creating-the-presentation-descriptor)
-   [Avvio dell'origine supporto](#starting-the-media-source)
    -   [La ricerca](#seeking)
-   [Sospensione dell'origine multimediale](#pausing-the-media-source)
-   [Generazione dei dati di origine](#generating-source-data)
    -   [Richieste di esempio](#sample-requests)
    -   [Esempi di allocazione](#allocating-samples)
    -   [Gap nel flusso](#gaps-in-the-stream)
-   [Arresto dell'origine supporto](#shutting-down-the-media-source)
-   [Origini attive](#live-sources)
-   [Argomenti correlati](#related-topics)

## <a name="creating-the-presentation-descriptor"></a>Creazione del descrittore della presentazione

Il metodo [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) restituisce una copia del descrittore di presentazione dell'origine. Per creare il descrittore di presentazione, è necessario conoscerne il numero di flussi nel contenuto di origine e i formati possibili di ogni flusso. Per ogni flusso, creare un descrittore di flusso come segue:

1.  Creare una matrice di tipi di supporto. Ogni tipo di supporto nella matrice rappresenta un possibile formato per il flusso. Per ulteriori informazioni sulla creazione di tipi di supporto, vedere [tipi di supporti](media-types.md).
2.  Chiamare [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) per creare il descrittore del flusso. Passare la matrice dei tipi di supporto. La funzione restituisce un puntatore [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .
3.  Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) per ottenere il gestore del tipo di supporto del descrittore del flusso.
4.  Chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) per impostare il formato del flusso predefinito. Usare uno dei tipi di supporti creati nel passaggio 1. In genere, è consigliabile usare il formato con la qualità più elevata.
5.  Facoltativamente, impostare gli attributi sul descrittore del flusso. Per un elenco degli attributi che si applicano ai descrittori di flusso, vedere [attributi del descrittore di flusso](stream-descriptor-attributes.md).

A questo punto, creare il descrittore della presentazione:

1.  Chiamare [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) e passare la matrice dei descrittori di flusso. La funzione restituisce un puntatore [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .
2.  Scegliere la selezione del flusso predefinita chiamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) per selezionare uno o più flussi. È necessario selezionare almeno un flusso nella configurazione predefinita.
3.  Facoltativamente, impostare gli attributi per il descrittore della presentazione. Per un elenco di attributi validi per i descrittori di flusso, vedere la pagina relativa agli [attributi del descrittore di presentazione](presentation-descriptor-attributes.md).

È necessario creare il descrittore della presentazione una volta all'avvio o dopo che l'origine ha analizzato un numero sufficiente di dati di origine per determinare il contenuto. Il metodo [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) deve restituire una copia del descrittore della presentazione. Per creare la copia, chiamare [**IMFPresentationDescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). La restituzione di una copia impedisce al client di modificare lo stato del descrittore di presentazione originale, ad esempio gli attributi o la selezione del flusso. Tuttavia, tenere presente che **Clone** crea una copia superficiale, in modo che il client possa potenzialmente modificare i descrittori di flusso sottostanti.

## <a name="starting-the-media-source"></a>Avvio dell'origine supporto

Il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) avvia l'origine del supporto o cerca una nuova posizione. Una chiamata a **Start** causa una *ricerca* quando lo stato precedente è stato sospeso o in esecuzione e viene specificata una nuova ora di inizio. In caso contrario, il metodo **Start** genera un'operazione di *avvio*. Al termine dell'operazione di **avvio** , inviare gli eventi seguenti.

1.  Inviare un evento [MENewStream](menewstream.md) per ogni nuovo flusso, ovvero ogni flusso precedentemente deselezionato ed è ora selezionato. I dati dell'evento sono un puntatore al flusso.
2.  Invia un evento [MEUpdatedStream](meupdatedstream.md) per ogni flusso selezionato in precedenza ed è ancora selezionato. I dati dell'evento sono un puntatore al flusso. Non inviare un evento per i flussi deselezionati.
3.  Se l'origine sta cercando, inviare un evento [MESourceSeeked](mesourceseeked.md) . In caso contrario, inviare un evento [MESourceStarted](mesourcestarted.md) . I dati dell'evento corrispondono all'ora di inizio specificata nel metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) . Per l'evento MESourceStarted, se l'ora di avvio è un VT \_ vuoto, impostare l'attributo di [**\_ \_ \_ \_ avvio effettivo dell'origine evento MF**](mf-event-source-actual-start-attribute.md) sull'evento. Il valore dell'attributo è l'ora di inizio effettiva.
4.  Per ogni flusso, se l'origine sta cercando, inviare un evento [MEStreamSeeked](mestreamseeked.md) . In caso contrario, inviare un evento [MEStreamStarted](mestreamstarted.md) . I dati dell'evento sono l'ora di inizio. (L'origine multimediale può accodare un evento sul flusso chiamando il metodo [**IMFMediaEventGenerator:: QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent) del flusso).

Quando un flusso viene deselezionato, arrestare il flusso. Il flusso non deve accodare altri eventi in quel momento.

Il formato dell'ora per il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) viene specificato nel parametro *pguidTimeFormat* . Il formato dell'ora solare, indicato da **GUID \_ null**, è 100 unità di nanosecondi. Un'origine multimediale deve supportare questo formato di ora.

### <a name="seeking"></a>La ricerca

Quando si cerca, la posizione iniziale richiesta potrebbe non rientrare in un limite di campione esatto. Inoltre, per il contenuto compresso, la posizione iniziale potrebbe essere compresa tra fotogrammi chiave. Un flusso deve fornire campioni dal primo punto necessario per produrre un campione non compresso nella posizione iniziale richiesta. Per video, significa partire dal fotogramma chiave precedente. La pipeline è responsabile dell'eliminazione dei frame aggiuntivi dal decodificatore, in modo che la riproduzione venga avviata all'ora richiesta.

L'ora di inizio specificata negli eventi di origine ([MESourceStarted](mesourcestarted.md), [MESourceSeeked](mesourceseeked.md), [MEStreamStarted](mestreamstarted.md)e [MEStreamSeeked](mestreamseeked.md)) è l'ora di inizio richiesta (il valore specificato nel metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) ), indipendentemente dall'effettiva posizione iniziale.

Si supponga, ad esempio, che i primi frame di un flusso video abbiano le seguenti caratteristiche:



| Esempio     | 1       | 2       | 3        | 4        |
|------------|---------|---------|----------|----------|
| Tempo       | 33 msec | 66 msec | 100 msec | 133 msec |
| Fotogramma chiave? | Sì     | No      | No       | Sì      |



 

Se il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) viene chiamato con un valore di 100 millisecondi, l'origine deve eseguire l'output del video a partire dal frame 1, il primo fotogramma chiave prima del momento. L'evento di avvio indicherà comunque 100 millisecondi nei dati dell'evento.

## <a name="pausing-the-media-source"></a>Sospensione dell'origine multimediale

Il metodo [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) mette in pausa l'origine del supporto.

Mentre l'origine viene sospesa, un flusso può creare nuovi esempi e archiviarli in una coda, ma il flusso non recapita gli esempi. Di seguito sono riportate alcune eccezioni a questa regola:

-   Le origini attive dovrebbero eliminare i dati mentre sono sospesi.
-   Se l'origine recupera i dati da una rete, potrebbe sospendere il server.

Se il client chiama [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) mentre l'origine è sospesa, la richiesta viene accodata anche fino a quando l'origine non viene riavviata. Le richieste non devono essere eliminate.

La sospensione è consentita solo dallo stato started. In caso contrario, la [**sospensione**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) dovrebbe restituire una **\_ transizione di stato MF E \_ non valida \_ \_**.

## <a name="generating-source-data"></a>Generazione dei dati di origine

Media Foundation usa un *modello pull*, ovvero i flussi generano e recapitano gli esempi in risposta alle richieste dalla pipeline. Un flusso può fornire esempi quando l'origine multimediale è in esecuzione e il flusso è selezionato. Un flusso recapita i dati solo quando il client richiede un nuovo esempio.

### <a name="sample-requests"></a>Richieste di esempio

Il client richiede un nuovo esempio chiamando [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Di seguito è illustrata la sequenza di operazioni:

1.  Il client chiama [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). L'argomento è un puntatore a un oggetto *token* facoltativo utilizzato dal client per tenere traccia della richiesta. Il client implementa il token. I token devono esporre l'interfaccia **IUnknown** . Il client può anche passare un puntatore NULL anziché un token.
2.  Se il client ha fornito un token, il flusso multimediale chiama **AddRef** sul token e inserisce il token in una coda First in, First-out. Il metodo restituisce e i passaggi rimanenti si verificano in modo asincrono.

3.  Quando sono disponibili più dati, il flusso multimediale crea un nuovo esempio. Questo passaggio viene descritto più dettagliatamente nella sezione successiva.
4.  Il flusso multimediale estrae il primo token dalla coda.
5.  Se il token non è **null**, il flusso multimediale imposta l'attributo del [**\_ token MFSampleExtension**](mfsampleextension-token-attribute.md) nell'esempio di supporto. Il valore dell'attributo è un puntatore al token.
6.  Il flusso multimediale Invia un evento [MEMediaSample](memediasample.md) . I dati dell'evento sono un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dell'esempio.
7.  Se il client ha fornito un token, il flusso multimediale chiama **Release** sull'oggetto token.

Se il flusso multimediale non è in grado di soddisfare la richiesta [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) del client, estrae il token dalla coda e chiama **Release** sul token, ma non invia un evento [MEMediaSample](memediasample.md) .

Il client può usare il token per tenere traccia dello stato della richiesta. Quando il client riceve l'evento [MEMediaSample](memediasample.md) , può ottenere il token dall'esempio e confrontarlo con la richiesta originale. Il client può anche usare il token per rilevare se l'origine multimediale ha eliminato la richiesta. Se il conteggio dei riferimenti del token scende a zero e il flusso multimediale non invia un evento MEMediaSample, significa che la richiesta è stata eliminata.

I passaggi elencati di seguito presuppongono che il metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) venga implementato come operazione asincrona. Se il metodo è sincrono, non è necessario inserire il token della richiesta in una coda. Tuttavia, se la generazione di dati richiede una quantità significativa di tempo, è consigliabile un approccio asincrono, ad esempio se l'origine legge i dati da un flusso di byte.

Il flusso è responsabile del buffering di tutti i dati che si accumulano tra le chiamate a [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).

Quando il flusso multimediale raggiunge la fine del flusso, invia un evento [MEEndOfStream](meendofstream.md) dopo l'ultimo campione. Al termine di ogni flusso, l'origine multimediale Invia un evento [MEEndOfPresentation](meendofpresentation.md) . Quando un flusso multimediale invia l'evento MEEndOfStream, il metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) restituisce **MF \_ E \_ End \_ of \_ Stream** fino a quando l'origine non viene riavviata.

### <a name="allocating-samples"></a>Esempi di allocazione

Quando il flusso è pronto a compilare una richiesta di esempio in sospeso, viene creato un nuovo esempio e vengono aggiunti uno o più buffer multimediali all'esempio. Per ulteriori informazioni sulla creazione di buffer multimediali, vedere [buffer multimediali](media-buffers.md).

Il flusso deve impostare il timestamp e la durata, se noto. Il timestamp è relativo all'origine. Nella maggior parte dei casi, l'inizio del contenuto corrisponde a un timestamp di zero. Se, ad esempio, l'origine legge da un file multimediale, l'inizio del file avrà un timestamp pari a zero.

Il timestamp dell'esempio non è necessariamente uguale all'ora di presentazione. La sessione multimediale si traduce dall'ora di origine all'ora di presentazione. Per i dati compressi, il flusso deve generare dati a partire dal fotogramma chiave più vicino prima dell'ora di inizio. In questo modo, il decodificatore è in grado di recapitare il frame visualizzato all'ora di inizio richiesta. In caso contrario, il decodificatore deve attendere fino al fotogramma chiave seguente.

Se la velocità di riproduzione è più veloce o più lenta di 1,0, la pipeline regola la frequenza del clock di presentazione. L'origine non modifica i timestamp degli esempi.

L'origine può impostare informazioni aggiuntive sull'esempio impostando gli attributi. Per un elenco di attributi di esempio, vedere [esempi di attributi](sample-attributes.md).

### <a name="gaps-in-the-stream"></a>Gap nel flusso

Se un flusso contiene un gap di lunghezza significativa, è consigliabile che il flusso invii un evento [MEStreamTick](mestreamtick.md) . Questo evento informa il client che manca un campione. I dati dell'evento corrispondono al timestamp dell'esempio mancante, in unità di 100 nanosecondi (**VT \_ i8**). Questo evento consente di salvare i componenti downstream in attesa di esempi che non verranno ricevuti. Il flusso può inviare tutti gli eventi MEStreamTick necessari per estendere il gap nel flusso.

## <a name="shutting-down-the-media-source"></a>Arresto dell'origine supporto

Quando il client viene eseguito tramite l'origine del supporto, chiama [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). All'interno di questo metodo, l'origine multimediale dovrebbe interrompere i conteggi circolari dei riferimenti. In genere, vi saranno riferimenti circolari tra l'origine multimediale e i flussi multimediali.

Se si utilizza la coda degli eventi per implementare [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator), chiamare [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) nella coda degli eventi. Questo metodo arresta la coda degli eventi e segnala a qualsiasi chiamante che è attualmente in attesa di un evento.

Dopo l'arresto, tutti i metodi nell'origine restituiscono l' **\_ \_ arresto MF e**, ad eccezione dei metodi **IUnknown** .

## <a name="live-sources"></a>Origini attive

A partire da Windows 7, Media Foundation supporta automaticamente dispositivi di acquisizione audio e video. Per il video, il dispositivo deve fornire un minidriver di streaming kernel (KS) nella categoria acquisizione video. Media Foundation usa il percorso PnP per enumerare il dispositivo. Per l'audio, Media Foundation usa l'API del dispositivo multimediale Windows (MMDevice) per enumerare i dispositivi dell'endpoint audio. Se il dispositivo soddisfa questi criteri, non è necessario implementare un'origine multimediale personalizzata.

Tuttavia, potrebbe essere necessario implementare un'origine multimediale personalizzata per un altro tipo di dispositivo o un'altra origine dati dinamica. Esistono solo alcune differenze tra un'origine live e altre origini multimediali:

-   Nel metodo [**IMFMediaSource:: getcaratteristiche**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics) , restituire **MFMEDIASOURCE è il \_ flag \_ Live** .
-   Il primo campione deve avere un timestamp pari a zero.
-   Gli eventi e gli Stati di streaming vengono gestiti come le origini multimediali, ad eccezione dello stato di sospensione.
-   In pausa, non accodare gli esempi. Eliminare tutti i dati generati mentre sono sospesi.
-   Le origini attive in genere non supportano la ricerca, la riproduzione inversa o il controllo della frequenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini supporti](media-sources.md)
</dt> <dt>

[Esercitazione: scrittura di un'origine multimediale personalizzata](tutorial--writing-a-custom-media-source.md)
</dt> </dl>

 

 



