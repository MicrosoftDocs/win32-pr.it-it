---
description: Questo argomento descrive come un client usa una trasformazione Media Foundation (MFT) per elaborare i dati. Il client è qualsiasi elemento che chiama direttamente i metodi in MFT. Potrebbe trattarsi dell'applicazione o della Media Foundation pipeline.
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: Modello di elaborazione MFT di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a1edb0c5144c6e3a3e1825e637cd5d19049699ad60bbf764629c9ade7cd3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035454"
---
# <a name="basic-mft-processing-model"></a>Modello di elaborazione MFT di base

Questo argomento descrive come un client usa una trasformazione Media Foundation (MFT) per elaborare i dati. Il *client* è qualsiasi elemento che chiama direttamente i metodi in MFT. Potrebbe trattarsi dell'applicazione o della Media Foundation pipeline.

Leggere questo argomento se si è:

-   Scrittura di un'applicazione che effettua chiamate dirette a uno o più MFT.
-   Scrittura di un MFT personalizzato e si vuole comprendere il comportamento previsto di un MFT.

Questo argomento descrive un *modello di elaborazione sincrono.* In questo modello tutti i metodi di elaborazione dati si bloccano fino al completamento. Le MFT possono supportare anche un modello *asincrono,* descritto nell'argomento [MFT asincroni](asynchronous-mfts.md).

-   [Modello di elaborazione di base](#basic-processing-model)
    -   [Creare MFT](#create-the-mft)
    -   [Ottenere gli identificatori di flusso](#get-stream-identifiers)
    -   [Impostare i tipi di supporti](#set-media-types)
    -   [Ottenere i requisiti del buffer](#get-buffer-requirements)
    -   [Elaborare i dati](#process-data)
-   [Estensioni al modello di base](#extensions-to-the-basic-model)
-   [IMF2DBuffer](#imf2dbuffer)
-   [Scaricamento di un MFT](#flushing-an-mft)
-   [Svuotamento di un MFT](#draining-an-mft)
-   [Attributi di esempio](#sample-attributes)
-   [Discontinuità](#discontinuities)
-   [Modifiche al formato dinamico](#dynamic-format-changes)
-   [Eventi di flusso](#stream-events)
-   [Argomenti correlati](#related-topics)

## <a name="basic-processing-model"></a>Modello di elaborazione di base

### <a name="create-the-mft"></a>Creare MFT

Esistono diversi modi per creare un MFT:

-   Chiamare la [**funzione MFTEnum.**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
-   Chiamare la [**funzione MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
-   Se si conosce già il CLSID di MFT, è sufficiente chiamare **CoCreateInstance**.

Alcuni MFT possono fornire altre opzioni, ad esempio una funzione di creazione specializzata.

### <a name="get-stream-identifiers"></a>Ottenere gli identificatori di flusso

Un MFT ha uno o *più flussi*. I flussi di input ricevono dati di input e i flussi di output generano dati di output. Flussi non sono rappresentati come oggetti distinti. I vari metodi MFT accettano invece gli identificatori di flusso come parametri.

Alcuni MFT consentono al client di aggiungere o rimuovere flussi di input. Durante lo streaming, un MFT può aggiungere o rimuovere flussi di output. Il client non può aggiungere o rimuovere flussi di output.

1.  (Facoltativo). Chiamare [**IMFTransform::GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) per ottenere il numero minimo e massimo di flussi supportati da MFT. Se i valori minimo e massimo sono uguali, il MFT ha un numero fisso di flussi.
2.  Chiamare [**IMFTransform::GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) per ottenere il numero iniziale di flussi.
3.  Chiamare [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) per ottenere gli identificatori di flusso. Se questo metodo restituisce E NOTIMPL, significa che MFT ha un numero fisso di flussi e gli identificatori di flusso sono \_ consecutivi a partire da zero.
4.  (Facoltativo). Se MFT non ha un numero fisso di flussi, chiamare [**IMFTransform::AddInputStreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) per aggiungere altri flussi di input o [**IMFTransform::D eleteInputStream**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) per rimuovere i flussi di input. Non è possibile aggiungere o rimuovere flussi di output.

### <a name="set-media-types"></a>Impostare i tipi di supporti

Prima che un MFT possa elaborare i dati, il client deve impostare un tipo di supporto per ognuno dei flussi di MFT. Un MFT potrebbe richiedere che il client imposta i tipi di input prima di impostare i tipi di output o richieda l'ordine opposto (prima i tipi di output). Alcuni MFT non hanno un requisito per l'ordine.

Un MFT può fornire un elenco di tipi di supporti preferiti per un flusso. Inoltre, le MFT possono indicare i formati generali supportati aggiungendo queste informazioni al Registro di sistema.

Per impostare i tipi di supporti, eseguire le operazioni seguenti:

1.  (Facoltativo). Per ogni flusso di input, chiamare [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) per ottenere l'elenco dei tipi preferiti per tale flusso.
    -   Se questo metodo restituisce MF E TRANSFORM TYPE NOT SET, è necessario impostare prima i tipi \_ \_ di \_ \_ \_ output. Andare al passaggio 3.
    -   Se il metodo restituisce E NOTIMPL, MFT non dispone di un elenco di tipi \_ di input preferiti. Andare al passaggio 2.
2.  Per ogni flusso di input, chiamare [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il tipo di input. È possibile usare un tipo di supporto del passaggio 1 o un tipo che descrive i dati di input. Se un flusso restituisce MF \_ E TRANSFORM TYPE NOT \_ \_ \_ \_ SET, andare al passaggio 3.
3.  (Facoltativo). Per ogni flusso di output, chiamare [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un elenco dei tipi preferiti per tale flusso.
    -   Se questo metodo restituisce MF E TRANSFORM TYPE NOT SET, è necessario impostare prima i tipi di input. Tornare \_ al \_ passaggio \_ \_ \_ 1.
    -   Se un flusso restituisce E NOTIMPL, MFT non dispone di un elenco di tipi \_ di output preferiti. Andare al passaggio 4.
4.  Per ogni flusso di output, chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di output. È possibile usare un tipo di supporto del passaggio 3 o un tipo che descrive il formato di output richiesto.
5.  Se i flussi di input non hanno un tipo di supporto, tornare al passaggio 1.

### <a name="get-buffer-requirements"></a>Ottenere i requisiti del buffer

Dopo che il client ha impostato i tipi di supporti, dovrebbe ottenere i requisiti del buffer per ogni flusso:

-   Per ogni flusso di input, chiamare [**IMFTransform::GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo).
-   Per ogni flusso di output, chiamare [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).

### <a name="process-data"></a>Elaborare dati

Un MFT è progettato per essere una macchina a stati affidabile. Non esegue alcuna chiamata al client.

1.  Chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio [**MFT \_ MESSAGE NOTIFY \_ \_ BEGIN \_ STREAMING.**](mft-message-notify-begin-streaming.md) Questo messaggio richiede al MFT di allocare tutte le risorse necessarie durante lo streaming.
2.  Chiamare [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) in almeno un flusso di input per recapitare un esempio di input al MFT.
3.  (Facoltativo). Chiamare [**IMFTransform::GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) per verificare se MFT può generare un esempio di output. Se il metodo restituisce S \_ OK, controllare il *parametro pdwFlags.* Se *pdwFlags contiene* il flag **MFT OUTPUT STATUS SAMPLE \_ \_ \_ \_ READY,** andare al passaggio 4. Se *pdwFlags* è zero, tornare al passaggio 2. Se il metodo restituisce E \_ NOTIMPL, andare al passaggio 4.
4.  Chiamare [**IMFTransform::P rocessOutput per**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ottenere i dati di output.
    -   Se il metodo restituisce **MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT,** significa che MFT richiede più dati di input. Tornare al passaggio 2.
    -   Se il metodo restituisce **MF \_ E TRANSFORM \_ STREAM \_ \_ CHANGE,** significa che il numero di flussi di output è stato modificato o il formato di output è stato modificato. Il client potrebbe dover eseguire una query per ottenere nuovi identificatori di flusso o impostare nuovi tipi di supporti. Per altre informazioni, vedere la documentazione di [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
5.  Se sono ancora presenti dati di input da elaborare, andare al passaggio 2. Se MFT ha utilizzato tutti i dati di input disponibili, procedere al passaggio 6.
6.  Chiamare [**ProcessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) il [**messaggio MFT MESSAGE NOTIFY END \_ OF \_ \_ \_ \_ STREAM.**](mft-message-notify-end-of-stream.md)
7.  Chiamare [**ProcessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) il [**messaggio MFT MESSAGE COMMAND \_ \_ \_ DRAIN.**](mft-message-command-drain.md)
8.  Chiamare [**ProcessOutput per**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ottenere l'output rimanente. Ripetere questo passaggio finché il metodo non restituisce **MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT**. Questo valore restituito segnala che tutto l'output è stato svuotato da MFT. Non considerare questa condizione come condizione di errore.

La sequenza descritta qui mantiene il meno possibile i dati in MFT. Dopo ogni chiamata a [**ProcessInput,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)il client tenta di ottenere l'output. Potrebbero essere necessari diversi esempi di input per produrre un campione di output oppure un singolo esempio di input potrebbe generare diversi esempi di output. Il comportamento ottimale per il client è eseguire il pull degli esempi di output da MFT fino a quando l'MFT non richiede più input.

Tuttavia, MFT deve essere in grado di gestire un ordine diverso di chiamate al metodo da parte del client. Ad esempio, il client potrebbe semplicemente alternare tra le chiamate a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). MFT deve limitare la quantità di input che ottiene restituisce **MF \_ E \_ NOTACCEPTING** da **ProcessInput** ogni volta che ha un output da produrre.

L'ordine delle chiamate al metodo descritto qui non è l'unica sequenza di eventi valida. Ad esempio, i passaggi 3 e 4 presuppongono che il client inizi con i tipi di input e quindi tenti i tipi di output. Il client può anche invertire questo ordine e iniziare con i tipi di output. In entrambi i casi, se MFT richiede l'ordine opposto, deve restituire il codice di errore MF \_ E TRANSFORM TYPE NOT \_ \_ \_ \_ SET.

Il client può chiamare metodi in forma informativo, ad esempio [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) e [**GetOutputStreamInfo,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)in qualsiasi momento durante lo streaming. Il client può anche tentare di modificare i tipi di supporti in qualsiasi momento. Se non si tratta di un'operazione valida, MFT deve restituire un codice di errore. In breve, i MFT devono presupporre molto poco sull'ordine delle operazioni, oltre a quanto documentato nelle chiamate stesse.

Il diagramma seguente illustra un diagramma di flusso delle procedure descritte in questo argomento.

![diagramma di flusso che deriva dagli identificatori di flusso get tramite cicli che impostano tipi di input, ottengono input ed elaborano l'output](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>Estensioni al modello di base

Facoltativamente, un MFT può supportare alcune estensioni al modello di streaming di base.

-   Flussi di lettura differita. Se il metodo [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) restituisce il flag **MFT \_ OUTPUT STREAM \_ \_ LAZY \_ READ** per un flusso di output, il client non deve raccogliere dati da tale flusso di output. MFT continua ad accettare l'input e a un certo punto il MFT rimuoverà i dati di output dal flusso. Se tutti i flussi di output hanno questo flag, MFT non accetterà mai l'input. Un esempio può essere una trasformazione di visualizzazione, in cui il client ottiene l'output solo quando dispone di cicli CPU di riserva per disegnare la visualizzazione.
-   Flussi eliminabili. Se il metodo [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) restituisce il flag **MFT \_ OUTPUT STREAM \_ \_ DISCARDABLE** per un flusso di output, il client può richiedere all'MFT di rimuovere l'output, ma MFT non scarterà alcun output se non richiesto. Quando MFT raggiunge il buffer di input massimo, il client deve raccogliere alcuni dati di output o richiedere all'MFT di eliminare l'output.
-   Flussi facoltativi. Se il metodo [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) restituisce il flag FACOLTATIVO MFT OUTPUT STREAM per un flusso di output oppure il metodo [**IMFTransform::GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) restituisce il flag **FACOLTATIVO MFT \_ INPUT \_ \_** **\_ \_ STREAM \_** per un flusso di input, tale flusso è facoltativo. Il client non deve impostare un tipo di supporto nel flusso. Se il client non imposta il tipo, il flusso viene deselezionato. Un flusso di output deselezionato non produce esempi e il client non fornisce un buffer per il flusso quando chiama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Un flusso di input deselezionato non accetta dati di input. Un MFT può contrassegnare tutti i flussi di input e output come facoltativi. Tuttavia, è previsto che sia necessario selezionare almeno un input e un output per il funzionamento dell'MFT.
-   Elaborazione asincrona. Il modello di elaborazione asincrona è stato introdotto nella Windows 7. È descritto nell'argomento [MFT asincroni](asynchronous-mfts.md).

## <a name="imf2dbuffer"></a>IMF2DBuffer

Se un MFT elabora dati video non compressi, deve usare [**l'interfaccia IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) per modificare i buffer di esempio. Per ottenere questa interfaccia, eseguire una query [**sull'interfaccia IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) su qualsiasi buffer di input o di output. L'uso di questa interfaccia quando è disponibile può comportare copie aggiuntive del buffer. Per usare correttamente questa interfaccia, la trasformazione non deve bloccare il buffer usando **l'interfaccia IMFMediaBuffer** quando **È disponibile IMF2DBuffer.**

Per altre informazioni sull'elaborazione dei dati video, vedere [Buffer video non compressi](uncompressed-video-buffers.md).

## <a name="flushing-an-mft"></a>Scaricamento di un MFT

*Lo scaricamento* di un MFT comporta la rimozione di tutti i dati di input da parte dell'MFT. Ciò può causare un'interruzione nel flusso di output. Un client scarica in genere un MFT prima di cercare un nuovo punto nel flusso di input o di passare a un nuovo flusso di input, quando il client non si preoccupa di perdere i dati.

Per scaricare un messaggio MFT, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio [**MFT \_ MESSAGE COMMAND \_ \_ FLUSH.**](mft-message-command-flush.md)

## <a name="draining-an-mft"></a>Svuotamento di un MFT

*Lo svuotamento* di un MFT causa la produzione di più output possibile da tutti i dati di input già inviati. Se MFT non è in grado di produrre un esempio di output completo dall'input disponibile, i dati di input verranno trascinati. Un client svuota in genere un MFT quando raggiunge la fine del flusso di origine o immediatamente prima di una modifica del formato nel flusso di origine. Per svuotare un MFT, eseguire le operazioni seguenti:

1.  Chiamare [**ProcessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) il [**messaggio MFT MESSAGE COMMAND \_ \_ \_ DRAIN.**](mft-message-command-drain.md) Questo messaggio notifica all'MFT che deve recapitare il maggior numero possibile di dati di output dai dati di input già inviati.
2.  Chiamare [**ProcessOutput per**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ottenere i dati di output, finché il metodo non restituisce **MF E TRANSFORM NEED \_ MORE \_ \_ \_ \_ INPUT**.

Durante l'svuotamento dell'MFT, non accetterà più input.

## <a name="sample-attributes"></a>Attributi di esempio

Gli esempi di input possono avere attributi che devono essere copiati negli esempi di output corrispondenti.

-   Se MFT restituisce **VARIANT \_ TRUE per** la proprietà [**MFPKEY \_ EXATTRIBUTE \_ SUPPORTED,**](mfpkey-exattribute-supported-property.md) MFT deve copiare gli attributi.
-   Se la [**proprietà MFPKEY \_ EXATTRIBUTE \_ SUPPORTED**](mfpkey-exattribute-supported-property.md) è **VARIANT \_ FALSE** o non è impostata, il client deve copiare gli attributi.

Per un MFT con un input e un output, è possibile usare la regola generale seguente:

-   Se ogni esempio di input produce esattamente un esempio di output, è possibile consentire al client di copiare gli attributi. Lasciare la [**proprietà MFPKEY \_ EXATTRIBUTE \_ SUPPORTED**](mfpkey-exattribute-supported-property.md) non impostata.
-   Se non esiste una corrispondenza uno-a-uno tra gli esempi di input e gli esempi di output, MFT deve determinare gli attributi corretti per gli esempi di output. Impostare la [**proprietà MFPKEY \_ EXATTRIBUTE \_ SUPPORTED**](mfpkey-exattribute-supported-property.md) su **VARIANT \_ TRUE.**

## <a name="discontinuities"></a>Discontinuità

Una discontinuità è un'interruzione in un flusso audio o video. Le discontinuità possono essere causate da pacchetti eliminati in una connessione di rete, dati di file danneggiati, passaggio da un flusso di origine a un altro o un'ampia gamma di altre cause. Le discontinuità vengono segnalate impostando [**l'attributo MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) nel primo esempio dopo la discontinuità. Non è possibile segnalare una discontinuità nel mezzo di un campione. Pertanto, tutti i dati discontinui devono essere inviati in esempi separati.

Alcune trasformazioni, in particolare quelle che gestiscono dati non compressi, ad esempio gli effetti audio e video, devono ignorare le discontinuità quando elaborano i dati di input. Questi MFT sono in genere progettati per gestire i dati continui e devono considerare tutti i dati ricevuti come continui, anche dopo una discontinuità.

Se un MFT ignora una discontinuità nei dati di input, deve comunque impostare il flag di discontinuità nell'esempio di output, se l'esempio di output ha lo stesso timestamp dell'esempio di input. Se l'esempio di output ha un timestamp diverso, tuttavia, MFT non deve propagare la discontinuità. Questo è il caso, ad esempio, di alcuni resampler audio. Una discontinuità nella posizione errata nel flusso è peggiore di nessuna discontinuità.

La maggior parte dei decodificatori non può ignorare le discontinuità, perché una discontinuità influisce sull'interpretazione dell'esempio successivo. Qualsiasi tecnologia di codifica che usa la compressione tra frame, ad esempio MPEG-2, rientra in questa categoria. Alcuni schemi di codifica usano solo la compressione intra-frame, ad esempio DV e MJPEG. Questi decodificatori possono ignorare in modo sicuro le discontinuità.

Le trasformazioni che rispondono alle discontinuità devono in genere eseguire l'output della maggior parte dei dati prima della discontinuità possibile e rimuovere il resto. L'esempio di input con il flag di discontinuità deve essere elaborato come se fosse il primo esempio nel flusso. Questo comportamento corrisponde a quello specificato per il messaggio [**MFT \_ MESSAGE COMMAND \_ \_ DRAIN.**](mft-message-command-drain.md) Tuttavia, i dettagli esatti dipendono dal formato multimediale.

Se un decodificatore non esegue alcuna operazione per attenuare una discontinuità, deve copiare il flag di discontinuità nei dati di output. I demultiplexer e altri MFT che funzionano interamente con i dati compressi devono copiare eventuali discontinuità nei flussi di output. In caso contrario, i componenti downstream potrebbero non essere in grado di decodificare correttamente i dati compressi. In generale, è quasi sempre corretto passare le discontinuità a valle, a meno che MFT non contenga codice esplicito per attenuare le discontinuità.

## <a name="dynamic-format-changes"></a>Modifiche al formato dinamico

I formati possono cambiare durante lo streaming. Ad esempio, le proporzioni possono cambiare nel mezzo di un flusso video.

Per informazioni dettagliate sul modo in cui le modifiche del flusso vengono gestite da un MFT, vedere [Gestione delle modifiche al flusso](handling-stream-changes.md).

## <a name="stream-events"></a>Trasmettere eventi

Per inviare un evento a un MFT, chiamare [**IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). Se il metodo restituisce **MF \_ S TRANSFORM DO NOT \_ \_ \_ \_ PROPAGATE \_ EVENT,** MFT restituirà l'evento al chiamante in una chiamata successiva a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Se il metodo restituisce qualsiasi altro **valore HRESULT,** MFT non restituirà l'evento al client in **ProcessOutput**. In tal caso, il client è responsabile della propagazione dell'evento a valle al componente successivo nella pipeline, se applicabile. Per altre informazioni, vedere [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 



