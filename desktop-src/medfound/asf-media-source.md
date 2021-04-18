---
description: Media Foundation fornisce l'origine dei supporti ASF che può essere utilizzata da un'applicazione per rappresentare un file ASF nel livello pipeline dell'architettura.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: Origine supporto ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75dc682d48339ce4ff707e7859a6962b9f5cfd92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320816"
---
# <a name="asf-media-source"></a>Origine supporto ASF

Media Foundation fornisce l'origine dei supporti ASF che può essere utilizzata da un'applicazione per rappresentare un file ASF nel livello pipeline dell'architettura.

Per riprodurre un file ASF, un'applicazione può usare l'origine dei supporti ASF per inserire i dati in una pipeline di riproduzione. In uno scenario di codifica, l'applicazione può usare l'origine dei supporti ASF come origine per la conversione in un altro formato o per la conversione di un file con velocità in bit superiore in un file con velocità in bit inferiore senza modificare i formati. L'origine dei supporti ASF deve essere usata nel livello della pipeline, ovvero un'applicazione deve usare la sessione multimediale per controllare l'operazione. Questo livello di accesso consente alle applicazioni di ottenere gli eventi mentre è in corso la sessione multimediale. Per ottenere un accesso di livello inferiore al contenuto ASF, un'applicazione deve usare i componenti ASF di livello WMContainer.

L'origine dei supporti ASF implementa l'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , che è l'interfaccia generica per le origini multimediali in Media Foundation. Analogamente a qualsiasi altra origine multimediale, l'origine dei supporti ASF fornisce un descrittore di presentazione che descrive principalmente l'oggetto intestazione ASF. Inoltre, l'origine dei supporti ASF fornisce descrittori di flusso che rappresentano ogni flusso nel contenuto multimediale. Per ulteriori informazioni, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).

-   [Creazione dell'origine dei supporti ASF](#creating-the-asf-media-source)
-   [Impostazioni di configurazione per l'origine dei supporti ASF](#configuration-settings-for-the-asf-media-source)
-   [Modello a oggetti di origine multimediale ASF](#asf-media-source-object-model)
-   [Servizi di origine multimediale ASF](#asf-media-source-services)
    -   [Conversione timecode](#timecode-translation)
-   [Argomenti correlati](#related-topics)

## <a name="creating-the-asf-media-source"></a>Creazione dell'origine dei supporti ASF

Per creare l'origine del supporto ASF, l'applicazione deve usare il [resolver di origine](source-resolver.md). Per creare l'origine dei supporti ASF, l'applicazione deve fornire l'origine per la quale il resolver di origine crea l'origine del supporto ASF. È necessario fornire le informazioni sull'origine specificando l'URL del file di origine o il flusso di byte che contiene il supporto. Se l'applicazione sceglie di creare l'origine del supporto ASF specificando l'URL, è necessario chiamare [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) per l'operazione sincrona o **IMFSourceResolver:: Begin... EndCreateObjectFromURL** per l'operazione asincrona. Il processo per la creazione dell'origine multimediale da un flusso di byte è simile. L'applicazione deve chiamare [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) per l'operazione sincrona o **IMFSourceResolver:: Begin... EndCreateObjectFromBytestream** per l'operazione asincrona. Queste chiamate devono specificare MF \_ risoluzione \_ MEDIASOURCE nel parametro *dwFlags* . Per ulteriori informazioni sull'utilizzo di questo flag, vedere Using the source resolver.

Se l'applicazione specifica un URL, per un file locale, la stringa URL può contenere il percorso del file multimediale o può essere preceduta dallo schema "file:". L'estensione del nome file deve essere ". asf", ". WM", L ". WMA" o ". wmv". Per un file ASF in rete, il resolver di origine crea l' [origine di rete](network-source-features.md), che usa l'origine del supporto ASF.

Durante il processo di creazione dell'oggetto, il resolver di origine cerca l'elenco dei gestori dello schema e dei gestori del flusso di byte nel registro di sistema e carica il gestore corrispondente più vicino in grado di analizzare il contenuto multimediale e creare anche l'oggetto di origine multimediale sottostante. Indipendentemente dal metodo utilizzato per creare l'origine multimediale (URL e flusso di byte), il resolver di origine crea un flusso di byte e legge il contenuto dei supporti di origine nel flusso di byte. Per altre informazioni, vedere [gestori di schemi e gestori di Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

Per un esempio di codice su come creare un'origine multimediale, vedere [using the source resolver](using-the-source-resolver.md).

## <a name="configuration-settings-for-the-asf-media-source"></a>Impostazioni di configurazione per l'origine dei supporti ASF

Il resolver di origine esegue una query per le funzionalità del flusso di byte sottostante e determina che le operazioni sono consentite sull'origine dei supporti appena creata. Una di queste funzionalità è la ricerca. Se è consentita un'operazione di ricerca, l'applicazione può specificare la modalità di ricerca utilizzata dall'origine multimediale durante la ricerca in un punto specifico della presentazione.

Un'applicazione può impostare la modalità di ricerca, che deve essere utilizzata dall'origine multimediale, durante la creazione dell'oggetto. Una volta creata l'origine del supporto ASF con la modalità di ricerca specificata, non è possibile modificarla nell'origine supporto o modificarla dinamicamente durante una presentazione. Le preferenze di ricerca vengono specificate come proprietà nella chiamata dell'applicazione ai metodi del resolver di origine pertinenti usati per creare l'origine multimediale. Questi set di proprietà vengono impostati in un archivio di proprietà e passati al parametro *pProps* . Se queste proprietà non vengono passate, l'origine supporto funziona con le impostazioni predefinite. Per ulteriori informazioni sull'impostazione di queste proprietà, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Se la ricerca è consentita, l'origine dei supporti ASF supporta le modalità di ricerca seguenti:

-   Ricerca esatta: in questa modalità, l'origine dei supporti ASF si basa sull'oggetto indice ASF del file ASF. Se il file non contiene l'oggetto indice, la ricerca esatta è disabilitata e viene utilizzata una delle altre modalità a seconda delle proprietà specificate dall'applicazione impostate nell'origine supporto.
-   Ricerca approssimativa: questa modalità viene richiesta dall'applicazione passando [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) nell'archivio delle proprietà ai metodi del resolver di origine pertinenti. Tuttavia, la ricerca approssimativa viene utilizzata solo se il flusso di byte non supporta la ricerca basata sul tempo. In questa modalità, l'origine multimediale determina un'ora di inizio relativamente più vicina al tempo di ricerca. Se il file ASF contiene un oggetto indice ASF, viene utilizzato per calcolare l'ora di inizio. La ricerca approssimativa è meno accurata ma più veloce rispetto alla ricerca esatta perché il tempo impiegato per il rendering del primo campione all'ora di inizio predeterminata è più veloce.
-   Ricerca iterativa: per impostare questa modalità, l'applicazione deve impostare la proprietà [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) . La ricerca iterativa è un algoritmo per trovare una posizione in un file ASF che non contiene alcun oggetto indice ASF. In questa modalità, l'origine multimediale determina una stima approssimativa del punto di ricerca leggendo l'offset del flusso di byte. Usa una serie di approssimazioni, in base alla velocità in bit media, per avvicinarsi progressivamente al tempo di ricerca di destinazione. L'algoritmo è simile a una ricerca binaria. La ricerca iterativa può richiedere più tempo rispetto alla ricerca tramite l'oggetto index, quindi è disabilitato per impostazione predefinita. Se si imposta questa proprietà, utilizzare le proprietà seguenti per impostare i parametri di ricerca: [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolleranza \_ in \_ millisecondi](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Queste proprietà impostano rispettivamente il numero massimo di iterazioni e la tolleranza. L'algoritmo si interrompe quando raggiunge il numero massimo di iterazioni oppure quando trova un pacchetto la cui distanza dal tempo di ricerca rientra nella tolleranza specificata.

In breve, l'applicazione ha la possibilità di scegliere la ricerca approssimativa o iterativa quando il file ASF non contiene un oggetto indice ASF.

## <a name="asf-media-source-object-model"></a>Modello a oggetti di origine multimediale ASF

L'origine dei supporti ASF implementa l'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) ed espone le interfacce seguenti. Un'applicazione può ottenere un riferimento a queste interfacce chiamando **IMFMediaSource:: QueryInterface** sull'origine dei supporti ASF.



| Interfaccia                                                | Descrizione                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Obbligatorio per tutte le origini supporti.                                                                                                                    |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Obbligatorio per tutte le origini supporti. Consente alle applicazioni di ottenere gli eventi dall'origine multimediale attraverso la sessione multimediale.                                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Esegue una query sull'origine multimediale per l'interfaccia del servizio specificata.                                                                                      |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Imposta e ottiene le proprietà nell'origine supporto. Ogni proprietà contiene un nome descrittivo e un valore.                                               |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Descrive i metadati per il file ASF.                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Recupera una raccolta di metadati per un'intera presentazione o per un flusso nella presentazione.                                      |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Esegue una query sull'intervallo di frequenze di riproduzione supportate, inclusa la riproduzione inversa.                                                                |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Ottiene o imposta la velocità di riproduzione.                                                                                                                    |
| [**IMFTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Ottiene l'ITA per ogni flusso ASF contenuto nell'origine.                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Consente a un'origine multimediale di ricevere un puntatore all'interfaccia [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , che viene usata per creare oggetti nel processo PMP. |
| [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Esegue la conversione tra i codici temporali SMPTE (Society of Motion Picture e Television Engineers) e le unità di tempo di 100 nanosecondi.                              |



 

## <a name="asf-media-source-services"></a>Servizi di origine multimediale ASF

L'origine dei supporti ASF fornisce vari servizi con ambito per il file ASF. Per ottenere un puntatore a un determinato servizio, l'applicazione deve usare uno dei seguenti identificatori di servizio nella chiamata a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice). Per informazioni, vedere [interfacce del servizio](service-interfaces.md).



| Identificatore servizio               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_servizio di \_ controllo della velocità MF \_       | Utilizzando questo identificatore, un'applicazione può ottenere un puntatore a interfacce [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) o [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) . Usando l'oggetto frequenza di supporto implementato dall'origine multimediale, l'applicazione può verificare se una determinata frequenza è supportata dal file multimediale ASF sottostante, anche per ottenere la tariffa più veloce e più lenta. Utilizzando l'oggetto di controllo della velocità, l'applicazione può ottenere e impostare la velocità di riproduzione. Se l'applicazione specifica una determinata frequenza per la riproduzione, l'origine dei supporti ASF verifica innanzitutto se la frequenza richiesta è entro i limiti di frequenza (determinati dalle tariffe veloci e più lente) e quindi imposta la frequenza. Questo non controlla le condizioni variabili perché la velocità in bit potrebbe cambiare in qualsiasi momento a seconda della larghezza di banda di rete. Per ulteriori informazioni, [controllare la frequenza](rate-control.md). |
| \_ \_ servizio provider di metadati MF \_  | Utilizzando questo identificatore, l'applicazione può ottenere un puntatore all'interfaccia [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) dell'origine dei supporti ASF. Questa interfaccia fornisce l'accesso alle informazioni sul file ASF in particolare gli oggetti intestazione ASF e i flussi contenuti nel contenuto multimediale. Le informazioni di intestazione sono esposte tramite gli attributi del descrittore di presentazione e le informazioni sul flusso vengono fornite tramite gli attributi Per ulteriori informazioni su questi attributi, vedere [Media Foundation attributi per gli oggetti intestazione ASF](media-foundation-attributes-for-asf-header-objects.md). Oltre alle informazioni esposte tramite attributi, esistono anche metadati descrittivi, impostati come proprietà.                                                                                                 |
| \_ \_ servizio Gestione proprietà \_ MF   | Utilizzando questo identificatore, l'applicazione può ottenere un puntatore all'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) dell'origine multimediale ASF. Nell'archivio delle proprietà sono contenuti tutti i metadati relativi al file ASF. Questo identificatore è una novità di Windows 7 e sostituisce \_ il \_ servizio del provider di metadati MF \_ per ottenere le proprietà dei metadati.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_servizio statistiche \_ MFNETSOURCE | Per ulteriori informazioni, vedere Recupero delle statistiche di rete nella [registrazione client](client-logging.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_servizio timecode \_ MF            | Utilizzando questo identificatore, l'applicazione può ottenere un puntatore all'interfaccia [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) dell'origine multimediale. Questa implementazione può essere usata per eseguire traduzioni di codice temporale, ad esempio la conversione del codice di ora SMPTE in unità di 100-nano secondo e viceversa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Conversione timecode

L'origine dei supporti ASF fornisce un servizio di conversione del codice temporale che consente all'applicazione di convertire il codice di ora SMPTE nel tempo di presentazione più vicino (in unità 100-nanosecondi). Viceversa, l'applicazione può ottenere anche il codice temporale per un'ora di presentazione richiesta. Il servizio è disponibile tramite l'interfaccia [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) , implementata dall'origine dei supporti ASF. Le chiamate al metodo su questo puntatore di interfaccia sono asincrone che possono essere eseguite dal thread dell'applicazione principale senza bloccare l'interfaccia utente dell'applicazione.

Nei passaggi seguenti viene riepilogata la procedura per la conversione del codice temporale:

1.  Ottenere un puntatore all'interfaccia [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) dell'origine multimediale ASF chiamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e specificando l'identificatore **del \_ \_ servizio del timecode MF** .
2.  Chiamare [**IMFTimecodeTranslate:: BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) o [**IMFTimecodeTranslate:: BeginConvertHNSToTimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) e specificare l'ora da tradurre. Per **BeginConvertTimecodeToHNS** è necessario specificare il codice temporale come variabile [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) con tipo di dati **VT \_ i8** . Il metodo **BeginConvertHNSToTimecode** richiede l'ora in unità 100-nanosecondi come tipo [**MFTIME**](mftime.md) .
3.  Completare l'operazione asincrona chiamando [**IMFTimecodeTranslate:: EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) o **IMFTimecodeTranslate:: EndConvertTimecodeToHNS** in modo appropriato.

Durante la creazione dell'origine multimediale, il resolver di origine crea un flusso di byte per il file da cui l'origine multimediale legge il contenuto ASF. Affinché le conversioni temporali abbiano esito positivo, il flusso di byte associato al file ASF deve avere funzionalità di ricerca; in caso contrario, l'applicazione ottiene \_ l' \_ errore MF E BYTESTREAM \_ non \_ ricercabile dalla chiamata **Begin...** . Un altro requisito per le conversioni temporali è che il file ASF, rappresentato dall'origine multimediale ASF, deve avere oggetti indice ASF. I tempi di presentazione e i codici temporali vengono estratti dagli oggetti indice ASF che gestiscono tutti gli indici e dai corrispondenti punti di ricerca per il file ASF. Per la conversione del codice time-to-time della presentazione, il file ASF deve contenere un oggetto indice semplice; per la conversione dell'ora da codice a presentazione, è necessario che il file ASF disponga di un oggetto index. Le operazioni di conversione si basano sull' *indicizzatore* sottostante (componente WMContainer) per analizzare e leggere l'oggetto index associato al file ASF. Se il file non contiene un oggetto index, l'applicazione riceve in modo asincrono il \_ codice di errore MF E \_ No \_ index.

Per tradurre il tempo richiesto dall'applicazione, l'origine multimediale enumera i flussi all'interno del file e trova il flusso che contiene l'oggetto indice ASF appropriato. Se viene trovato un flusso di questo tipo, l'origine multimediale analizza i pacchetti ASF del flusso viene analizzata fino a quando non viene raggiunto il codice di ora corretto. Dopo aver trovato l'esempio corretto, recupera l'ora di presentazione corrispondente o il codice temporale dall'esempio e lo restituisce al chiamante.

### <a name="script-command-support"></a>Supporto del comando script

Quando si compila una topologia ASF che contiene un flusso di script, viene aggiunto un nodo del flusso di script alla topologia. Questo nodo invierà IMFSamples al momento appropriato. Il IMFSample fornito dal nodo di origine dello script archivia i dati nel IMFMediaBuffer associato all'esempio. È possibile chiamare CopyToBuffer nell'esempio per ottenere un IMFMediaBuffer e quindi chiamare Lock sul buffer per ottenere i dati. 

I payload del flusso di script vengono compressi nel buffer come stringa di tipo, seguito da NULL, seguito dalla stringa di comando, seguito da NULL. Le stringhe sono Unicode nel formato ASF.

Un payload, ad esempio, potrebbe essere simile al seguente (dove \ 0 indica un carattere NULL):

*URL\0http://contoso.com\0*

*Text\0This è un caption\0*



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF a livello pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
