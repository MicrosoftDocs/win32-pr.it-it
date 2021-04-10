---
description: Questo argomento descrive il modo in cui un client usa una trasformazione Media Foundation (MFT) per elaborare i dati. Il client è qualsiasi elemento che chiama direttamente i metodi in MFT. Potrebbe trattarsi dell'applicazione o della pipeline Media Foundation.
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: Modello di elaborazione MFT di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca54df6d9765aaf54456c3d9dc4461a82a93d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049325"
---
# <a name="basic-mft-processing-model"></a>Modello di elaborazione MFT di base

Questo argomento descrive il modo in cui un client usa una trasformazione Media Foundation (MFT) per elaborare i dati. Il *client* è qualsiasi elemento che chiama direttamente i metodi in MFT. Potrebbe trattarsi dell'applicazione o della pipeline Media Foundation.

Leggere questo argomento se:

-   Scrittura di un'applicazione che effettua chiamate dirette a uno o più MFTs.
-   Scrittura di un MFT personalizzato e desidera comprendere il comportamento previsto di un MFT.

In questo argomento viene descritto un modello di elaborazione *sincrona* . In questo modello tutti i metodi di elaborazione dati si bloccano fino a quando non vengono completati. MFTs può inoltre supportare un modello *asincrono* , descritto nell'argomento [MFTS asincrono](asynchronous-mfts.md).

-   [Modello di elaborazione di base](#basic-processing-model)
    -   [Creare il MFT](#create-the-mft)
    -   [Ottenere gli identificatori di flusso](#get-stream-identifiers)
    -   [Imposta tipi di supporto](#set-media-types)
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

### <a name="create-the-mft"></a>Creare il MFT

Esistono diversi modi per creare un MFT:

-   Chiamare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .
-   Chiamare la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Se si conosce già il CLSID della MFT, è sufficiente chiamare **CoCreateInstance**.

Alcuni MFTs potrebbero fornire altre opzioni, ad esempio una funzione di creazione specializzata.

### <a name="get-stream-identifiers"></a>Ottenere gli identificatori di flusso

Un MFT ha uno o più *flussi*. I flussi di input ricevono i dati di input e i flussi di output generano dati di output. I flussi non sono rappresentati come oggetti distinti. Al contrario, diversi metodi MFT accettano gli identificatori di flusso come parametri.

Alcuni MFTs consentono al client di aggiungere o rimuovere flussi di input. Durante lo streaming, un MFT può aggiungere o rimuovere flussi di output. Il client non è in grado di aggiungere o rimuovere flussi di output.

1.  (Facoltativo). Chiamare [**IMFTransform:: GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) per ottenere il numero minimo e massimo di flussi che il MFT può supportare. Se il valore minimo e massimo sono gli stessi, la MFT dispone di un numero fisso di flussi.
2.  Chiamare [**IMFTransform:: GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) per ottenere il numero iniziale di flussi.
3.  Chiamare [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) per ottenere gli identificatori del flusso. Se questo metodo restituisce E \_ NOTIMPL, significa che la MFT ha un numero fisso di flussi e gli identificatori di flusso sono consecutivi a partire da zero.
4.  (Facoltativo). Se MFT non dispone di un numero fisso di flussi, chiamare [**IMFTransform:: AddInputStreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) per aggiungere altri flussi di input o [**IMFTransform::D eleteinputstream**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) per rimuovere i flussi di input. Non è possibile aggiungere o rimuovere flussi di output.

### <a name="set-media-types"></a>Imposta tipi di supporto

Prima che un MFT possa elaborare i dati, il client deve impostare un tipo di supporto per ognuno dei flussi della MFT. Un MFT potrebbe richiedere che il client imposti i tipi di input prima di impostare i tipi di output o potrebbe richiedere l'ordine opposto (prima i tipi di output). Alcuni MFTs non hanno un requisito per l'ordine.

Una MFT può fornire un elenco di tipi di supporti preferiti per un flusso. Inoltre, MFTs può indicare i formati generali supportati aggiungendo queste informazioni al registro di sistema.

Per impostare i tipi di supporto, effettuare le operazioni seguenti:

1.  (Facoltativo). Per ogni flusso di input, chiamare [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) per ottenere l'elenco di tipi preferiti per quel flusso.
    -   Se questo metodo restituisce \_ \_ il tipo di trasformazione MF E \_ \_ non \_ impostato, è necessario impostare prima i tipi di output; andare al passaggio 3.
    -   Se il metodo restituisce E \_ NOTIMPL, MFT non dispone di un elenco di tipi di input preferiti; andare al passaggio 2.
2.  Per ogni flusso di input, chiamare [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il tipo di input. È possibile usare un tipo di supporto del passaggio 1 o un tipo che descrive i dati di input. Se un flusso restituisce il \_ \_ tipo di trasformazione MF E \_ \_ non \_ impostato, andare al passaggio 3.
3.  (Facoltativo). Per ogni flusso di output, chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un elenco di tipi preferiti per quel flusso.
    -   Se questo metodo restituisce \_ \_ il tipo di trasformazione MF E \_ \_ non \_ impostato, è necessario impostare prima i tipi di input; tornare al passaggio 1.
    -   Se un flusso restituisce E \_ NOTIMPL, MFT non dispone di un elenco di tipi di output preferiti; andare al passaggio 4.
4.  Per ogni flusso di output, chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di output. È possibile usare un tipo di supporto del passaggio 3 o un tipo che descrive il formato di output necessario.
5.  Se i flussi di input non hanno un tipo di supporto, tornare al passaggio 1.

### <a name="get-buffer-requirements"></a>Ottenere i requisiti del buffer

Dopo aver impostato i tipi di supporto, il client deve ottenere i requisiti del buffer per ogni flusso:

-   Per ogni flusso di input, chiamare [**IMFTransform:: GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo).
-   Per ogni flusso di output, chiamare [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).

### <a name="process-data"></a>Elaborare dati

Un MFT è progettato per essere una macchina a stati affidabile. Non effettua alcuna chiamata al client.

1.  Call [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il [**messaggio \_ MFT \_ Notify \_ Begin \_ streaming**](mft-message-notify-begin-streaming.md) Message. Questo messaggio richiede a MFT di allocare le risorse necessarie durante il flusso.
2.  Chiamare [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) in almeno un flusso di input per recapitare un esempio di input alla MFT.
3.  (Facoltativo). Chiamare [**IMFTransform:: GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) per eseguire una query su se MFT è in grado di generare un esempio di output. Se il metodo restituisce S \_ OK, controllare il parametro *pdwFlags* . Se *pdwFlags* contiene il flag di **stato di output di MFT \_ \_ \_ campione \_ pronto** , andare al passaggio 4. Se *pdwFlags* è zero, tornare al passaggio 2. Se il metodo restituisce E \_ NOTIMPL, andare al passaggio 4.
4.  Chiamare [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere i dati di output.
    -   Se il metodo restituisce **MF \_ E \_ Transform \_ necessita di un \_ maggiore \_ input**, significa che il MFT richiede più dati di input; tornare al passaggio 2.
    -   Se il metodo restituisce **la \_ \_ modifica del \_ flusso \_ di trasformazione MF e**, significa che il numero di flussi di output è stato modificato o che il formato di output è stato modificato. Il client potrebbe dover eseguire una query per i nuovi identificatori di flusso o impostare nuovi tipi di supporto. Per ulteriori informazioni, vedere la documentazione relativa a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
5.  Se sono ancora presenti dati di input da elaborare, andare al passaggio 2. Se il MFT ha utilizzato tutti i dati di input disponibili, procedere con il passaggio 6.
6.  Chiamare [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio relativo alla [**\_ \_ \_ fine \_ del \_ messaggio di notifica del messaggio MFT**](mft-message-notify-end-of-stream.md) .
7.  Chiamare [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio di [**\_ svuotamento del \_ comando \_ del messaggio MFT**](mft-message-command-drain.md) .
8.  Chiamare [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere l'output rimanente. Ripetere questo passaggio fino a quando il metodo non restituisce **MF \_ E \_ Transform necessita di un \_ \_ maggiore \_ input**. Questo valore restituito segnala che tutto l'output è stato svuotato dalla MFT. (Non considerarlo come condizione di errore).

La sequenza descritta qui mantiene il minor consumo possibile di dati nella MFT. Al termine di ogni chiamata a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), il client tenta di ottenere l'output. Per produrre un esempio di output è possibile che siano necessari diversi esempi di input oppure un singolo esempio di input può generare diversi esempi di output. Il comportamento ottimale per il client consiste nel pull degli esempi di output dalla MFT fino a quando il MFT richiede un maggior numero di input.

Tuttavia, il MFT dovrebbe essere in grado di gestire un ordine diverso di chiamate al metodo da parte del client. Ad esempio, il client può semplicemente alternarsi tra le chiamate a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Il MFT deve limitare la quantità di input ottenuta restituendo **MF \_ E \_ NOTACCEPTING** da **ProcessInput** ogni volta che viene generato un output.

L'ordine delle chiamate al metodo descritte in questo articolo non è l'unica sequenza valida di eventi. Ad esempio, i passaggi 3 e 4 presuppongono che il client inizi con i tipi di input e quindi tenti i tipi di output. Il client può inoltre invertire questo ordine e iniziare con i tipi di output. In entrambi i casi, se il MFT richiede l'ordine opposto, deve restituire il codice di errore MF \_ E il \_ tipo di trasformazione \_ \_ non \_ impostato.

Il client può chiamare metodi informativi, ad esempio [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) e [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo), in qualsiasi momento durante il flusso. Il client può anche tentare di modificare i tipi di supporto in qualsiasi momento. Se questa operazione non è valida, la tabella MFT deve restituire un codice di errore. In breve, MFTs deve presupporre pochissimo l'ordine delle operazioni, oltre a quanto documentato nelle chiamate stesse.

Il diagramma seguente illustra un diagramma di flusso delle procedure descritte in questo argomento.

![diagramma di flusso che conduce da ottenere gli identificatori dei flussi tramite cicli che impostano i tipi di input, ottengono l'input e l'output del processo](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>Estensioni al modello di base

Facoltativamente, una MFT può supportare alcune estensioni per il modello di flusso di base.

-   Flussi letti Lazy. Se il metodo [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) restituisce il flag di **\_ \_ \_ \_ lettura lenta del flusso di output MFT** per un flusso di output, il client non deve raccogliere i dati dal flusso di output. Il MFT continua ad accettare l'input e a un certo punto la MFT eliminerà i dati di output dal flusso. Se tutti i flussi di output presentano questo flag, l'opzione MFT non avrà mai esito positivo per accettare l'input. Un esempio potrebbe essere una trasformazione di visualizzazione, in cui il client ottiene l'output solo quando dispone di cicli di CPU di riserva per tracciare la visualizzazione.
-   Flussi scartabili. Se il metodo [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) restituisce il flag rimuovibile del **\_ \_ flusso \_ di output MFT** per un flusso di output, il client può richiedere al MFT di scartare l'output, ma il MFT non eliminerà alcun output a meno che non sia richiesto. Quando il MFT raggiunge il buffer di input massimo, il client deve raccogliere alcuni dati di output o richiedere a MFT di rimuovere l'output.
-   Flussi facoltativi. Se il metodo [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) restituisce il **flag \_ \_ \_ facoltativo del flusso di output di MFT** per un flusso di output oppure il metodo [**IMFTransform:: GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) restituisce il flag **\_ \_ \_ facoltativo del flusso di input MFT** per un flusso di input, tale flusso è facoltativo. Il client non deve impostare un tipo di supporto per il flusso. Se il client non imposta il tipo, il flusso viene deselezionato. Un flusso di output deselezionato non produce esempi e il client non fornisce un buffer per il flusso quando chiama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Un flusso di input deselezionato non accetta dati di input. Un MFT può contrassegnare tutti i flussi di input e di output come facoltativi. È tuttavia previsto che sia necessario selezionare almeno un input e un output per il funzionamento della MFT.
-   Elaborazione asincrona. Il modello di elaborazione asincrona è stato introdotto in Windows 7. Viene descritto nell'argomento [MFTS asincrono](asynchronous-mfts.md).

## <a name="imf2dbuffer"></a>IMF2DBuffer

Se un MFT elabora dati video non compressi, deve usare l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) per modificare i buffer di esempio. Per ottenere questa interfaccia, eseguire una query sull'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) su qualsiasi buffer di input o di output. Se non si utilizza questa interfaccia se disponibile, è possibile che vengano generate ulteriori copie del buffer. Per usare correttamente questa interfaccia, la trasformazione non deve bloccare il buffer usando l'interfaccia **IMFMediaBuffer** quando **IMF2DBuffer** è disponibile.

Per ulteriori informazioni sull'elaborazione dei dati video, vedere [buffer video non compressi](uncompressed-video-buffers.md).

## <a name="flushing-an-mft"></a>Scaricamento di un MFT

*Scaricando* una MFT, il MFT Elimina tutti i dati di input. Ciò può causare un'interruzioni nel flusso di output. Un client in genere Scarica un MFT prima di cercare un nuovo punto nel flusso di input o passa a un nuovo flusso di input, quando il client non è interessato alla perdita di dati.

Per scaricare un MFT, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio di [**\_ \_ \_ scaricamento del comando del messaggio MFT**](mft-message-command-flush.md) .

## <a name="draining-an-mft"></a>Svuotamento di un MFT

Con lo *svuotamento* di un MFT, il MFT produce il maggior volume di output possibile da qualsiasi dato di input già inviato. Se MFT non è in grado di produrre un esempio di output completo dall'input disponibile, eliminerà i dati di input. Un client in genere svuota un MFT quando ha raggiunto la fine del flusso di origine o immediatamente prima di una modifica del formato nel flusso di origine. Per svuotare un MFT, eseguire le operazioni seguenti:

1.  Chiamare [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio di [**\_ svuotamento del \_ comando \_ del messaggio MFT**](mft-message-command-drain.md) . Questo messaggio notifica alla MFT che deve fornire il maggior quantità di dati di output possibili dai dati di input già inviati.
2.  Chiamare [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere i dati di output, fino a quando il metodo non restituisce **MF \_ E \_ Transform necessita di un \_ \_ maggiore \_ input**.

Mentre è in corso lo svuotamento della MFT, non verrà accettato alcun input.

## <a name="sample-attributes"></a>Attributi di esempio

Gli esempi di input possono avere attributi che devono essere copiati negli esempi di output corrispondenti.

-   Se MFT restituisce la **variante \_ true** per la [**proprietà \_ \_ supportata MFPKEY EXATTRIBUTE**](mfpkey-exattribute-supported-property.md) , è necessario che il MFT Copi gli attributi.
-   Se la proprietà [**MFPKEY \_ EXATTRIBUTE \_ supportata**](mfpkey-exattribute-supported-property.md) è **Variant \_ false** o non è impostata, il client deve copiare gli attributi.

Per un MFT con un input e un output, è possibile usare la regola generale seguente:

-   Se ogni esempio di input produce esattamente un esempio di output, è possibile consentire al client di copiare gli attributi. Lasciare invariata la proprietà [**\_ \_ supportata da MFPKEY EXATTRIBUTE**](mfpkey-exattribute-supported-property.md) .
-   Se non esiste una corrispondenza uno-a-uno tra gli esempi di input e di output, il MFT deve determinare gli attributi corretti per gli esempi di output. Impostare la [**proprietà \_ \_ supportata MFPKEY EXATTRIBUTE**](mfpkey-exattribute-supported-property.md) su **Variant \_ true**.

## <a name="discontinuities"></a>Discontinuità

Una discontinuità è un'interruzione in un flusso audio o video. Le discontinuità possono essere causate da pacchetti eliminati in una connessione di rete, dati di file danneggiati, un passaggio da un flusso di origine a un altro o un'ampia gamma di altre cause. Le discontinuità sono segnalate impostando l'attributo di [**\_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sul primo campione dopo la discontinuità. Non è possibile segnalare una discontinuità al centro di un campione. Pertanto, tutti i dati discontinui devono essere inviati in campioni distinti.

Alcune trasformazioni, in particolare quelle che gestiscono dati non compressi, ad esempio gli effetti audio e video, devono ignorare le discontinuità quando elaborano i dati di input. Questi MFTs sono in genere progettati per gestire i dati continui e devono trattare tutti i dati ricevuti come continui, anche dopo una discontinuità.

Se una MFT ignora una discontinuità sui dati di input, deve comunque impostare il flag di discontinuità nell'esempio di output, se l'esempio di output ha lo stesso timestamp dell'esempio di input. Se l'output di esempio ha un timestamp diverso, tuttavia, il MFT non deve propagare la discontinuità. Questo è il caso di alcuni ricampionatori audio, ad esempio. Una discontinuità nella posizione errata nel flusso è peggiore della discontinuità.

La maggior parte dei decodificatori non può ignorare le discontinuità, perché una discontinuità influiscono sull'interpretazione dell'esempio successivo. Qualsiasi tecnologia di codifica che usa la compressione tra frame, ad esempio MPEG-2, rientra in questa categoria. Alcuni schemi di codifica usano solo la compressione intra-frame, ad esempio DV e MJPEG. Questi decodificatori possono ignorare in modo sicuro le discontinuità.

Le trasformazioni che rispondono a discontinuità dovrebbero in genere restituire la maggior parte dei dati prima della discontinuità così come possono ed eliminare il resto. L'esempio di input con il flag di discontinuità deve essere elaborato come se fosse il primo campione nel flusso. Questo comportamento corrisponde a quanto specificato per il messaggio [**di \_ \_ \_ svuotamento del comando del messaggio MFT**](mft-message-command-drain.md) . Tuttavia, i dettagli esatti dipendono dal formato multimediale.

Se un decodificatore non esegue alcuna operazione per attenuare la discontinuità, deve copiare il flag di discontinuità nei dati di output. I Demultiplexer e altre MFTs che funzionano interamente con i dati compressi devono copiare eventuali discontinuità nei relativi flussi di output. In caso contrario, i componenti downstream potrebbero non essere in grado di decodificare correttamente i dati compressi. In generale, è quasi sempre corretto passare le discontinuità a valle, a meno che il MFT non contenga codice esplicito per smussare le discontinuità.

## <a name="dynamic-format-changes"></a>Modifiche al formato dinamico

I formati possono cambiare durante il flusso. Ad esempio, le proporzioni possono variare al centro di un flusso video.

Per informazioni dettagliate sul modo in cui le modifiche del flusso vengono gestite da un MFT, vedere [gestione delle modifiche al flusso](handling-stream-changes.md).

## <a name="stream-events"></a>Eventi di flusso

Per inviare un evento a un MFT, chiamare [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). Se il metodo restituisce **la \_ trasformazione MF S non \_ propaga l' \_ \_ \_ \_ evento**, l'oggetto MFT restituirà l'evento al chiamante in una chiamata successiva a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Se il metodo restituisce qualsiasi altro valore **HRESULT** , l'evento MFT non restituirà l'evento al client in **ProcessOutput**. In tal caso, il client è responsabile della propagazione dell'evento a valle al componente successivo nella pipeline, se applicabile. Per ulteriori informazioni, vedere [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



