---
description: Media Foundation fornisce l'origine multimediale ASF che un'applicazione può usare per rappresentare un file ASF nel livello pipeline dell'architettura.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: Origine multimediale ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3222f32649aa5cb3f4d1d4688a9f7fb7402167e7831377fd8b04d6c879e23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881152"
---
# <a name="asf-media-source"></a>Origine multimediale ASF

Media Foundation fornisce l'origine multimediale ASF che un'applicazione può usare per rappresentare un file ASF nel livello pipeline dell'architettura.

Per riprodurre un file ASF, un'applicazione può usare l'origine multimediale ASF per alimentare i dati in una pipeline di riproduzione. In uno scenario di codifica, l'applicazione può usare l'origine multimediale ASF come origine per eseguire la conversione in un altro formato o per convertire un file a velocità in bit più elevata in un file a velocità in bit inferiore senza modificare i formati. L'origine multimediale ASF deve essere usata nel livello della pipeline, cio' un'applicazione deve usare la sessione multimediale per controllare l'operazione. Questo livello di accesso consente alle applicazioni di ottenere eventi mentre è in corso la sessione multimediale. Per ottenere l'accesso di livello inferiore al contenuto ASF, un'applicazione deve usare i componenti ASF del livello WMContainer.

L'origine multimediale ASF implementa [**l'interfaccia IMFMediaSource,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che è l'interfaccia generica per le origini multimediali in Media Foundation. Come qualsiasi altra origine multimediale, l'origine multimediale ASF fornisce un descrittore di presentazione che descrive principalmente l'oggetto intestazione ASF. Inoltre, l'origine multimediale ASF fornisce descrittori di flusso che rappresentano ogni flusso nel contenuto multimediale. Per altre informazioni, vedere [Struttura di file ASF.](asf-file-structure.md)

-   [Creazione dell'origine multimediale ASF](#creating-the-asf-media-source)
-   [Configurazione Impostazioni per l'origine multimediale ASF](#configuration-settings-for-the-asf-media-source)
-   [Modello a oggetti dell'origine multimediale ASF](#asf-media-source-object-model)
-   [Servizi di origine multimediale ASF](#asf-media-source-services)
    -   [Traduzione del codice temporale](#timecode-translation)
-   [Argomenti correlati](#related-topics)

## <a name="creating-the-asf-media-source"></a>Creazione dell'origine multimediale ASF

Per creare l'origine multimediale ASF, l'applicazione deve usare [il sistema di risoluzione dell'origine](source-resolver.md). Per creare l'origine multimediale ASF, l'applicazione deve fornire l'origine per cui il sistema di risoluzione di origine crea l'origine multimediale ASF. Le informazioni di origine devono essere fornite specificando l'URL del file di origine o il flusso di byte che contiene il supporto. Se l'applicazione sceglie di creare l'origine multimediale ASF specificando l'URL, deve chiamare [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) per l'operazione sincrona o **IMFSourceResolver::Begin... EndCreateObjectFromURL per l'operazione** asincrona. Il processo per la creazione dell'origine multimediale da un flusso di byte è simile. L'applicazione deve chiamare [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) per l'operazione sincrona o **IMFSourceResolver::Begin... EndCreateObjectFromBytestream per l'operazione** asincrona. Queste chiamate devono specificare MF \_ RESOLUTION \_ MEDIASOURCE nel *parametro dwFlags.* Per altre informazioni sull'uso di questo flag, vedere Uso del sistema di risoluzione dell'origine.

Se l'applicazione specifica un URL, per un file locale, la stringa URL può contenere il percorso del file multimediale o può essere preceduta dal prefisso "file: "scheme. L'estensione del nome file deve essere ".asf", ".wm", L".wma" o ".wmv". Per un file ASF in rete, il sistema di risoluzione di origine crea [l'origine di](network-source-features.md)rete , che usa l'origine multimediale ASF.

Durante il processo di creazione dell'oggetto, il sistema di risoluzione di origine cerca l'elenco dei gestori di schemi e dei gestori dei flussi di byte nel Registro di sistema e carica il gestore corrispondente più vicino in grado di analizzare il contenuto multimediale e creare anche l'oggetto di origine multimediale sottostante. Indipendentemente dal metodo usato per creare l'origine multimediale (URL e flusso di byte), il resolver di origine crea un flusso di byte e legge il contenuto del supporto di origine nel flusso di byte. Per altre informazioni, vedere [Gestori di schema e Byte-Stream di schema](scheme-handlers-and-byte-stream-handlers.md).

Per un esempio di codice su come creare un'origine multimediale, vedere [Using the Source Resolver](using-the-source-resolver.md).

## <a name="configuration-settings-for-the-asf-media-source"></a>Configurazione Impostazioni per l'origine multimediale ASF

Il resolver di origine esegue una query sulle funzionalità del flusso di byte sottostante e determina che le operazioni sono consentite nell'origine multimediale appena creata. Una di queste funzionalità è la ricerca. Se è consentita un'operazione di ricerca, l'applicazione può specificare la modalità di ricerca utilizzata dall'origine multimediale durante la ricerca in un punto specifico della presentazione.

Un'applicazione può impostare la modalità di ricerca, per l'origine multimediale da usare, durante la creazione dell'oggetto. Dopo aver creato l'origine multimediale ASF con la modalità di ricerca specificata, non può essere modificata nell'origine multimediale o modificata dinamicamente durante una presentazione. Le preferenze di ricerca vengono specificate come proprietà nella chiamata dell'applicazione ai metodi del resolver di origine pertinenti usati per creare l'origine multimediale. Questi set di proprietà vengono impostati in un archivio delle proprietà e passati al *parametro pProps.* Se queste proprietà non vengono passate, l'origine multimediale funziona con le impostazioni predefinite. Per altre informazioni sull'impostazione di queste proprietà, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

Se la ricerca è consentita, l'origine multimediale ASF supporta le modalità di ricerca seguenti:

-   Ricerca esatta: in questa modalità, l'origine multimediale ASF si basa sull'oggetto indice ASF del file ASF. Se il file non ha l'oggetto Index, la ricerca esatta è disabilitata e viene usata una delle altre modalità a seconda delle proprietà specificate dall'applicazione impostate nell'origine multimediale.
-   Ricerca approssimativa: questa modalità viene richiesta dall'applicazione passando [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) nell'archivio delle proprietà ai metodi del resolver di origine pertinenti. Tuttavia, la ricerca approssimativa viene usata solo se il flusso di byte non supporta la ricerca basata sul tempo. In questa modalità, l'origine multimediale determina un'ora di inizio relativamente più vicina all'ora di ricerca. Se il file ASF contiene un oggetto indice ASF, viene usato per calcolare l'ora di inizio. La ricerca approssimativa è meno accurata, ma più veloce della ricerca esatta, perché il tempo impiegato per eseguire il rendering del primo campione all'ora di inizio predeterminata è più veloce.
-   Ricerca iterativa: per impostare questa modalità, l'applicazione deve impostare la proprietà [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex.](mfpkey-asfmediasource-iterativeseekifnoindex.md) La ricerca iterativa è un algoritmo per trovare una posizione in un file ASF che non contiene alcun oggetto indice ASF. In questa modalità, l'origine multimediale determina una stima approssimativa del punto di ricerca leggendo l'offset del flusso di byte. Usa una serie di approssimazioni, in base alla velocità in bit media, per avvicinarsi progressivamente al tempo di ricerca di destinazione. L'algoritmo è simile a una ricerca binaria. La ricerca iterativa può richiedere più tempo rispetto alla ricerca tramite l'oggetto indice, pertanto è disabilitata per impostazione predefinita. Se si imposta questa proprietà, usare le proprietà seguenti per impostare i parametri di ricerca: [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance In \_ \_ MilliSecond](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Queste proprietà impostano rispettivamente il numero massimo di iterazioni e la tolleranza. L'algoritmo si arresta quando raggiunge il numero massimo di iterazioni o quando trova un pacchetto la cui distanza dal tempo di ricerca rientra nella tolleranza specificata.

In breve, l'applicazione può scegliere la ricerca approssimativa o iterativa quando il file ASF non contiene un oggetto indice ASF.

## <a name="asf-media-source-object-model"></a>Modello a oggetti dell'origine multimediale ASF

L'origine multimediale ASF implementa [**l'interfaccia IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) ed espone le interfacce seguenti. Un'applicazione può ottenere un riferimento a queste interfacce chiamando **IMFMediaSource::QueryInterface** nell'origine multimediale ASF.



| Interfaccia                                                | Descrizione                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Obbligatorio per tutte le origini multimediali.                                                                                                                    |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Obbligatorio per tutte le origini multimediali. Consente alle applicazioni di ottenere eventi dall'origine multimediale tramite la sessione multimediale.                                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Esegue una query sull'origine multimediale per l'interfaccia del servizio specificata.                                                                                      |
| [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Imposta e ottiene le proprietà nell'origine multimediale. Ogni proprietà contiene un nome descrittivo e un valore.                                               |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Descrive i metadati per il file ASF.                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Recupera una raccolta di metadati, per un'intera presentazione o per un flusso nella presentazione.                                      |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Esegue una query sull'intervallo di velocità di riproduzione supportate, inclusa la riproduzione inversa.                                                                |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Ottiene o imposta la velocità di riproduzione.                                                                                                                    |
| [**IMFTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Ottiene l'ITA per ogni flusso ASF contenuto nell'origine.                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Consente a un'origine multimediale di ricevere un puntatore [**all'interfaccia IMFPMPHost,**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) usata per creare oggetti nel processo PMP. |
| [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Esegue la conversione tra codici di tempo SMPTE (Society of Motion Picture and Television Engineers) e unità di tempo di 100 nanosecondi.                              |



 

## <a name="asf-media-source-services"></a>Servizi di origine multimediale ASF

L'origine multimediale ASF fornisce vari servizi con ambito per il file ASF. Per ottenere un puntatore a un particolare servizio, l'applicazione deve usare uno degli identificatori di servizio seguenti nella chiamata a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice). Per informazioni, vedere [Interfacce di servizio](service-interfaces.md).



| Identificatore del servizio               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SERVIZIO DI \_ CONTROLLO DELLA \_ FREQUENZA \_ MF       | Usando questo identificatore, un'applicazione può ottenere un puntatore alle [**interfacce IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) o [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) Usando l'oggetto di supporto della frequenza implementato dall'origine multimediale, l'applicazione può verificare se una determinata frequenza è supportata dal file multimediale ASF sottostante anche ottenere la velocità più veloce e la velocità più lenta. Usando l'oggetto di controllo della frequenza, l'applicazione può ottenere e impostare la velocità di riproduzione. Se l'applicazione specifica una frequenza specifica per la riproduzione, l'origine multimediale ASF verifica innanzitutto se la frequenza richiesta rientra nei limiti di velocità (determinati da velocità veloci e lente) e quindi imposta la frequenza. In questo modo non viene verificata la presenza di condizioni variabili perché la velocità in bit potrebbe cambiare in qualsiasi momento a seconda della larghezza di banda di rete. Per altre informazioni, vedere [Controllo della frequenza.](rate-control.md) |
| SERVIZIO PROVIDER DI METADATI MF \_ \_ \_  | Usando questo identificatore, l'applicazione può ottenere un puntatore [**all'interfaccia IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) dell'origine multimediale ASF. Questa interfaccia fornisce l'accesso alle informazioni sul file ASF in particolare gli oggetti intestazione ASF e i flussi contenuti nel contenuto multimediale. Le informazioni sull'intestazione vengono espore tramite gli attributi del descrittore di presentazione e le informazioni sul flusso vengono fornite tramite gli attributi del descrittore di flusso. Per altre informazioni su questi attributi, vedere Attributi [Media Foundation per gli oggetti intestazione ASF](media-foundation-attributes-for-asf-header-objects.md). Oltre alle informazioni esposte tramite attributi, esistono anche metadati descrittivi, impostati come proprietà.                                                                                                 |
| SERVIZIO DEL GESTORE DELLE PROPRIETÀ MF \_ \_ \_   | Usando questo identificatore, l'applicazione può ottenere un puntatore [**all'interfaccia IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) dell'origine multimediale ASF. L'archivio delle proprietà contiene tutti i metadati correlati al file ASF. Questo identificatore è nuovo in Windows 7 e sostituisce MF \_ METADATA PROVIDER SERVICE per ottenere le proprietà dei \_ \_ metadati.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SERVIZIO STATISTICHE \_ MFNETSOURCE \_ | Per altre informazioni, vedere Recupero di statistiche di rete nella [registrazione client](client-logging.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SERVIZIO \_ TIMECODE MF \_            | Usando questo identificatore, l'applicazione può ottenere un puntatore [**all'interfaccia IMFTimecodeTranslate dell'origine**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) multimediale. Questa implementazione può essere usata per eseguire time code traslazioni, ad esempio la conversione di SMPTE time code a 100 nano secondi e indietro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Traduzione del codice temporale

L'origine multimediale ASF fornisce un servizio di traduzione time code che consente all'applicazione di convertire SMPTE time code nel tempo di presentazione più vicino (in unità da 100 nanosecondi). Al contrario, l'applicazione può anche ottenere il time code per un'ora di presentazione richiesta. Il servizio è disponibile tramite [**l'interfaccia IMFTimecodeTranslate,**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) implementata dall'origine multimediale ASF. Le chiamate al metodo su questo puntatore a interfaccia sono asincrone che possono essere eseguite dal thread dell'applicazione principale senza bloccare l'interfaccia utente dell'applicazione.

I passaggi seguenti riepilogano la procedura per la time code traduzione:

1.  Ottenere il puntatore [**all'interfaccia IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) dell'origine multimediale ASF chiamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e specificando l'identificatore **MF \_ TIMECODE \_ SERVICE.**
2.  Chiamare [**IMFTimecodeTranslate::BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) o [**IMFTimecodeTranslate::BeginConvertHNSToTimecode e**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) specificare l'ora da convertire. Per **BeginConvertTimecodeToHNS,** time code deve essere specificata come variabile [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) con tipo di dati **VT \_ I8.** Il **metodo BeginConvertHNSToTimecode** richiede il tempo in unità da 100 nanosecondi come [**tipo MFTIME.**](mftime.md)
3.  Completare l'operazione asincrona chiamando [**IMFTimecodeTranslate::EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) o **IMFTimecodeTranslate::EndConvertTimecodeToHNS** in modo appropriato.

Durante la creazione dell'origine multimediale, il sistema di risoluzione di origine crea un flusso di byte per il file da cui l'origine multimediale legge il contenuto asf. Per consentire il corretto completamento delle conversioni temporizzato, il flusso di byte associato al file ASF deve avere funzionalità di ricerca. In caso contrario, l'applicazione ottiene l'errore MF \_ E \_ BYTESTREAM \_ NOT \_ SEEKABLE dalla chiamata **Begin....** Un altro requisito per le conversioni di tempo è che il file ASF, rappresentato dall'origine multimediale ASF, deve avere oggetti indice ASF. Gli orari di presentazione e i codici di ora vengono estratti dagli oggetti indice ASF che mantengono tutti gli indici e i corrispondenti punti di ricerca per il file ASF. Per la traduzione time-to-time code presentazione, il file ASF deve contenere un oggetto indice semplice. per time code conversione dell'ora da presentazione a presentazione, il file ASF deve avere un oggetto indice. Le operazioni di conversione si basano *sull'indicizzatore* sottostante (componente WMContainer) per analizzare e leggere l'oggetto indice associato al file ASF. Se il file non contiene un oggetto indice, l'applicazione riceve in modo asincrono il codice di errore MF \_ E \_ NO \_ INDEX.

Per convertire il tempo richiesto dall'applicazione, l'origine multimediale enumera i flussi all'interno del file e trova il flusso che contiene l'oggetto indice ASF appropriato. Se viene trovato un flusso di questo tipo, l'origine multimediale analizza i pacchetti ASF del flusso finché non viene raggiunto il time code corretto. Dopo aver trovato l'esempio corretto, recupera l'ora di presentazione o time code dall'esempio e la restituisce al chiamante.

### <a name="script-command-support"></a>Supporto dei comandi script

Quando si compila una topologia ASF che contiene un flusso di script, alla topologia viene aggiunto un nodo Flusso di script. Questo nodo invierà IMFSamples all'ora appropriata. L'oggetto IMFSample fornito dal nodo di origine dello script archivia i dati nell'oggetto IMFMediaBuffer associato all'esempio. È possibile chiamare CopyToBuffer sull'esempio per ottenere un oggetto IMFMediaBuffer e quindi chiamare Lock sul buffer per ottenere i dati. 

I payload del flusso di script vengono imballati nel buffer come stringa di tipo, seguiti da NULL, seguiti dalla stringa di comando, seguita da NULL. Le stringhe sono Unicode nel formato ASF.

Ad esempio, un payload potrebbe essere simile al seguente (dove \0 indica un carattere NULL):

*URL\0http://contoso.com\0*

*Text\0This è una didascalia\0*



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF del livello pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
