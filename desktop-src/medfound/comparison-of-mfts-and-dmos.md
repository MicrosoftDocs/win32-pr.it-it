---
description: Media Foundation trasformazioni (MFT) sono un'evoluzione del modello di trasformazione introdotto per la prima volta con DirectX Media Objects (DMO).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Confronto tra MFT e DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e145effed095fb22f6bfeb07cbee23ab3d30836a404f36a2bad4b9fbeb1dd81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958981"
---
# <a name="comparison-of-mfts-and-dmos"></a>Confronto tra MFT e DMO

Media Foundation trasformazioni (MFT) sono un'evoluzione del modello di trasformazione introdotto per la prima volta con DirectX Media Objects (DMO). Questo argomento riepiloga i modi principali in cui le MFT differiscono dalle DMO. Leggere questo argomento se si ha già familiarità con le interfacce DMO o se si vuole convertire un DMO esistente in MFT.

In questo argomento sono incluse le sezioni seguenti:

-   [Numero di Flussi](#number-of-streams)
-   [Negoziazione del formato](#format-negotiation)
-   [Streaming](#streaming)
    -   [Allocazione di risorse](#allocating-resources)
    -   [Elaborazione dei dati](#processing-data)
    -   [Flushing](#flushing)
    -   [Discontinuità dei flussi](#stream-discontinuities)
-   [Differenze varie](#miscellaneous-differences)
-   [Flag](#flags)
    -   [Flag ProcessInput](#processinput-flags)
    -   [Flag ProcessOutput](#processoutput-flags)
    -   [Flag GetInputStatus](#getinputstatus-flags)
    -   [Flag GetOutputStatus](#getoutputstatus-flags)
    -   [Flag GetInputStreamInfo](#getinputstreaminfo-flags)
    -   [Flag GetOutputStreamInfo](#getoutputstreaminfo-flags)
    -   [Flag SetInputType/SetOutputType](#setinputtypesetoutputtype-flags)
-   [Codici errore](#error-codes)
-   [Creazione di DMO/MFT ibridi](#creating-hybrid-dmomft-objects)
-   [Argomenti correlati](#related-topics)

## <a name="number-of-streams"></a>Numero di Flussi

Un DMO ha un numero fisso di flussi, mentre un MFT può supportare un numero dinamico di flussi. Il client può aggiungere flussi di input e MFT può aggiungere nuovi flussi di output durante l'elaborazione. Tuttavia, le MFT non sono necessarie per supportare i flussi dinamici. Un MFT può avere un numero fisso di flussi, proprio come un DMO.

I metodi seguenti vengono usati per supportare flussi dinamici in un MFT:

-   [**IMFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMFTransform::D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMFTransform::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Inoltre, il [**metodo IMFTransform::P rocessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) definisce il comportamento per l'aggiunta o la rimozione di flussi di output.

Poiché le DMO hanno flussi fissi, i flussi in un DMO vengono identificati usando valori di indice in base zero. Le MFT, d'altra parte, usano identificatori di flusso che non corrispondono necessariamente ai valori di indice. Ciò è dovuto al fatto che il numero di flussi in un MFT potrebbe cambiare. Ad esempio, il flusso 0 potrebbe essere rimosso, lasciando il flusso 1 come primo flusso. Tuttavia, un MFT con un numero fisso di flussi deve osservare la stessa convenzione delle DMO e usare i valori di indice per gli identificatori di flusso.

## <a name="format-negotiation"></a>Negoziazione del formato

Le MFT usano [**l'interfaccia IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) per descrivere i tipi di supporti. In caso contrario, la negoziazione del formato con mFT funziona sugli stessi principi di base delle DMO. Nella tabella seguente sono elencati i metodi di negoziazione del formato per le DMO e i metodi corrispondenti per mFT.



| DMO metodo                                                                        | Metodo MFT                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMFTransform::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**IMFTransform::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMFTransform::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**IMFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Streaming

Come le DMO, le MFT elaborano i dati tramite chiamate [**ai metodi ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) [**e ProcessOutput.**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) Ecco le principali differenze tra i processi DMO e MFT durante lo streaming dei dati.

### <a name="allocating-resources"></a>Allocazione di risorse

I MFT non hanno i metodi [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) e [**IMediaObject::FreeStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) usati con DMO. Per gestire in modo efficiente l'allocazione e la deallocazione delle risorse, un MFT può rispondere ai messaggi seguenti nel metodo [**IMFTransform::P rocessMessage:**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage)

-   [**MFT \_ MESSAGE \_ NOTIFY \_ BEGIN \_ STREAMING**](mft-message-notify-begin-streaming.md)
-   [**MFT \_ MESSAGE \_ NOTIFY \_ START \_ OF \_ STREAM**](mft-message-notify-start-of-stream.md)

Inoltre, il client può segnalare l'inizio e la fine di un flusso chiamando [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con i messaggi seguenti:

-   [**MFT \_ MESSAGE \_ NOTIFY \_ END \_ OF \_ STREAM**](mft-message-notify-end-of-stream.md)
-   [**MFT \_ MESSAGE \_ NOTIFY \_ END \_ STREAMING**](mft-message-notify-end-streaming.md)

Questi due messaggi non hanno un DMO equivalente.

### <a name="processing-data"></a>Elaborazione dei dati

Le MFT usano esempi di supporti per contenere i dati di input e output. Gli esempi di supporti [**espongono l'interfaccia IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) e contengono i dati seguenti:

-   Timestamp e durata.
-   Attributi che contengono informazioni per ogni esempio. Per un elenco di attributi, vedere [Attributi di esempio.](sample-attributes.md)
-   Zero o più buffer multimediali. Ogni buffer multimediale espone [**l'interfaccia IMFMediaBuffer.**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)

[**L'interfaccia IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) è simile all'DMO **IMediaBuffer.** Per accedere al buffer di memoria sottostante, chiamare [**IMFMediaBuffer::Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Questo metodo equivale approssimativamente a [**IMediaBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) per dmo.

Per i dati video non compressi, un buffer multimediale potrebbe supportare anche [**l'interfaccia IMF2DBuffer.**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) Un MFT che elabora video non compresso (come input o output) deve essere preparato per usare **l'interfaccia IMF2DBuffer** se il buffer lo espone. Per altre informazioni, vedere Buffer video non [compressi.](uncompressed-video-buffers.md)

Media Foundation alcune implementazioni standard di [**IMFMediaBuffer,**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)pertanto in genere non è necessario scrivere un'implementazione personalizzata. Per creare un buffer DMO da un buffer Media Foundation, chiamare [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).

### <a name="flushing"></a>Flushing

Le MFT non hanno un [**metodo Flush.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) Per scaricare un messaggio MFT, chiamare [**IMFTransform::P rocessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio [**MFT \_ MESSAGE COMMAND \_ \_ FLUSH.**](mft-message-command-flush.md)

### <a name="stream-discontinuities"></a>Discontinuità dei flussi

Le MFT non hanno un [**metodo Discontinuity.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) Per segnalare una discontinuità in un flusso, impostare l'attributo [**MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) nell'esempio di input.

## <a name="miscellaneous-differences"></a>Differenze varie

Ecco alcune differenze secondarie aggiuntive tra MFT e DMO.

-   Non sono disponibili equivalenti MFT per i metodi DMO seguenti:
    -   [**IMediaObject::Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   I MFT non sono necessari per supportare l'aggregazione.
-   I messaggi MFT supportano un'operazione *denominata svuotamento di*. Lo scopo dello svuotamento è elaborare tutti i dati che rimangono in MF, senza fornire altri dati di input al MFT (ad esempio, alla fine del flusso). Per svuotare un messaggio MFT, chiamare [**IMFTransform::P rocessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con il [**messaggio MFT \_ MESSAGE COMMAND \_ \_ DRAIN.**](mft-message-command-drain.md) Per altre informazioni, vedere [Modello di elaborazione MFT di base.](basic-mft-processing-model.md)
-   I file MFT possono avere attributi, inclusi gli attributi per flusso. Usare i metodi seguenti per ottenere gli attributi da un MFT:

    -   [**IMFTransform::GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   I MFT possono elaborare gli eventi. Per inviare un evento a un MFT, chiamare [**IMFTransform::P rocessEvent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent). Un MFT può inviare un evento al client tramite il [**metodo ProcessOutput.**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) Per altre informazioni, vedere [Modello di elaborazione MFT di base.](basic-mft-processing-model.md)

## <a name="flags"></a>Flags

Nelle tabelle seguenti sono elencati i vari flag DMO e i relativi equivalenti MFT. Ogni volta che DMO flag viene mappato direttamente a un flag MFT, entrambi i flag hanno lo stesso valore numerico. Tuttavia, alcuni DMO non hanno equivalenti MFT e viceversa.

### <a name="processinput-flags"></a>Flag ProcessInput

DMO: [**\_ \_ DMO'enumerazione BUFFER \_ \_ FLAGS \_ di INPUT**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) DATA.

MFT: nessuna enumerazione equivalente.



| DMO flag                                  | Flag MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DMO BUFFERF \_ \_ \_ SYNCPOINT DI INPUT**  | Nessun flag equivalente. Impostare invece [**l'attributo \_ CleanPoint MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) nell'esempio. |
| **\_DMO ORA \_ \_ BUFFERF DEI DATI DI \_ INPUT**       | Nessun flag equivalente. Chiamare invece [**IMFSample::SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) nell'esempio.                                  |
| **\_DMO BUFFERF \_ \_ TIMELENGTH DEI DATI \_ DI INPUT** | Nessun flag equivalente. Chiamare invece [**IMFSample::SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) nell'esempio.                          |



 

### <a name="processoutput-flags"></a>Flag ProcessOutput

DMO: DMO [**\_ enumerazione PROCESS OUTPUT \_ \_ \_ FLAGS.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags)

MFT: [**\_ enumerazione MFT \_ PROCESS OUTPUT \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags)



| DMO flag                                            | Flag MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **\_DMO ELABORAZIONE \_ DELL'OUTPUT \_ DISCARD QUANDO NESSUN \_ \_ \_ BUFFER** | **MFT \_ PROCESS \_ OUTPUT \_ DISCARD \_ WHEN \_ NO \_ BUFFER** |



 

DMO: [**\_ \_ DMO'enumerazione BUFFER FLAGS di OUTPUT \_ DATA. \_ \_**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags)


MFT: [**\_ enumerazione MFT \_ OUTPUT DATA BUFFER \_ \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags)



| DMO flag                                   | Flag MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DMO OUTPUT \_ DATA \_ BUFFERF \_ SYNCPOINT**  | Nessun flag equivalente. Controllare invece l'attributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) nell'esempio. |
| **\_DMO ORA \_ \_ BUFFERF DEI DATI DI \_ OUTPUT**       | Nessun flag equivalente. Chiamare invece [**IMFSample::GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) nell'esempio.                                        |
| **\_DMO BUFFERF \_ \_ TIMELENGTH DEI DATI \_ DI OUTPUT** | Nessun flag equivalente. Chiamare invece [**IMFSample::GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) sull'esempio.                                |
| **\_DMO BUFFERF DEI DATI DI OUTPUT \_ \_ \_ INCOMPLETO** | **BUFFER DEI DATI DI OUTPUT MFT \_ \_ \_ \_ INCOMPLETO**                                                                                                           |
| Nessun flag equivalente.                        | **MODIFICA DEL FORMATO \_ DEL BUFFER DEI DATI DI OUTPUT \_ \_ \_ \_ MFT**                                                                                                       |
| Nessun flag equivalente.                        | **MFT \_ OUTPUT \_ DATA \_ BUFFER \_ STREAM \_ END**                                                                                                          |
| Nessun flag equivalente.                        | **BUFFER DI DATI DI OUTPUT MFT \_ \_ NO \_ \_ \_ SAMPLE**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Flag GetInputStatus

DMO: **\_ \_ DMO'enumerazione INPUT \_ STATUS \_ FLAGS.**

MFT: [**\_ enumerazione MFT \_ INPUT STATUS \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags)



| DMO flag                              | Flag MFT                             |
|---------------------------------------|--------------------------------------|
| **\_DMO STATO \_ DI INPUTF \_ ACCEPT \_ DATA** | **MFT \_ INPUT \_ STATUS \_ ACCEPT \_ DATA** |



 

### <a name="getoutputstatus-flags"></a>Flag GetOutputStatus

DMO: nessuna enumerazione equivalente.

MFT: [**\_ enumerazione MFT \_ OUTPUT STATUS \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags)



| DMO flag            | Flag MFT                               |
|---------------------|----------------------------------------|
| Nessun flag equivalente. | **MFT \_ OUTPUT \_ STATUS \_ SAMPLE \_ READY** |



 

### <a name="getinputstreaminfo-flags"></a>Flag GetInputStreamInfo

DMO: [**\_ \_ DMO'enumerazione INPUT \_ STREAM INFO \_ \_ FLAGS.**](/previous-versions/windows/embedded/aa451600(v=msdn.10))

MFT: [**\_ enumerazione MFT \_ INPUT STREAM INFO \_ \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags)



| DMO flag                                             | Flag MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **\_DMO ESEMPI \_ INTERI DI STREAMF \_ DI \_ INPUT**              | **ESEMPI \_ INTERI DEL FLUSSO DI INPUT \_ \_ \_ MFT**              |
| **\_DMO SINGOLO CAMPIONE STREAMF DI INPUT \_ \_ PER \_ \_ \_ BUFFER** | **SINGOLO CAMPIONE DI FLUSSO DI INPUT MFT \_ \_ PER \_ \_ \_ \_ BUFFER** |
| **\_DMO DIMENSIONI \_ FISSE DEL CAMPIONE STREAMF \_ DI \_ \_ INPUT**         | **DIMENSIONI \_ FISSE DEL CAMPIONE DEL FLUSSO \_ \_ \_ DI \_ INPUT MFT**         |
| **\_DMO IL FLUSSO DI INPUT \_ \_ CONTIENE \_ BUFFER**              | **IL FLUSSO DI INPUT MFT \_ \_ CONTIENE \_ \_ BUFFER**              |
| Nessun flag equivalente.                                  | **IL FLUSSO DI INPUT MFT \_ \_ NON È \_ \_ \_ ADDREF**           |
| Nessun flag equivalente.                                  | **FLUSSO DI INPUT MFT \_ \_ \_ RIMOVIBILE**                   |
| Nessun flag equivalente.                                  | **FLUSSO DI INPUT MFT \_ \_ \_ FACOLTATIVO**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Flag GetOutputStreamInfo

DMO: [**\_ \_ DMO'enumerazione OUTPUT \_ STREAM INFO \_ \_ FLAGS.**](/previous-versions/ms806053(v=msdn.10))

MFT: [**\_ enumerazione MFT \_ OUTPUT STREAM INFO \_ \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags)



| DMO flag                                              | Flag MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **\_DMO OUTPUT \_ STREAMF \_ WHOLE \_ SAMPLES**              | **ESEMPI INTERI \_ DEL FLUSSO DI OUTPUT \_ \_ \_ MFT**              |
| **\_DMO OUTPUT \_ STREAMF \_ SINGLE \_ SAMPLE \_ PER \_ BUFFER** | **SINGOLO CAMPIONE DI FLUSSO DI OUTPUT MFT \_ \_ PER \_ \_ \_ \_ BUFFER** |
| **\_DMO DIMENSIONI \_ FISSE DEL CAMPIONE STREAMF \_ DI \_ \_ OUTPUT**         | **DIMENSIONI FISSE DEL CAMPIONE \_ \_ DEL FLUSSO \_ \_ DI \_ OUTPUT MFT**         |
| **\_DMO OUTPUT \_ STREAMF \_ DISCARDABLE**                 | **MFT \_ OUTPUT \_ STREAM \_ DISCARDABLE**                 |
| **\_DMO OUTPUT \_ STREAMF \_ FACOLTATIVO**                    | **FLUSSO DI OUTPUT MFT \_ \_ \_ FACOLTATIVO**                    |
| Nessun flag equivalente.                                   | **IL FLUSSO DI OUTPUT MFT \_ \_ FORNISCE \_ \_ ESEMPI**           |
| Nessun flag equivalente.                                   | **IL FLUSSO DI OUTPUT MFT \_ \_ PUÒ FORNIRE \_ \_ \_ ESEMPI**       |
| Nessun flag equivalente.                                   | **LETTURA \_ DIFFERITA \_ DEL FLUSSO \_ DI OUTPUT MFT \_**                  |
| Nessun flag equivalente.                                   | **FLUSSO DI OUTPUT MFT \_ \_ \_ RIMOVIBILE**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Flag SetInputType/SetOutputType

DMO: [**\_ \_ DMO'enumerazione SET \_ TYPE \_ FLAGS.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags)

MFT: [**\_ enumerazione MFT \_ SET TYPE \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags)



| DMO flag                        | Flag MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **\_DMO SET \_ TYPEF TEST ONLY (IMPOSTA SOLO \_ TEST TYPEF) \_** | **MFT \_ SET \_ TYPE \_ TEST \_ ONLY**                                                       |
| **\_DMO SET \_ TYPEF \_ CLEAR**      | Nessun flag equivalente. Impostare invece il tipo di supporto su **NULL per** cancellare il tipo di supporto. |



 

## <a name="error-codes"></a>Codici errore

Nella tabella seguente viene illustrato come eseguire il mapping DMO di errore a codici di errore MFT. Un oggetto MFT/DMO ibrido deve restituire i DMO di errore dai metodi [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e i codici di errore MFT dai [**metodi IMFTransform.**](/windows/win32/api/mftransform/nn-mftransform-imftransform) I DMO di errore sono definiti nel file di intestazione MediaErr.h. I codici di errore MFT sono definiti nel file di intestazione mferror.h.



| DMO codice di errore                  | Codice di errore MFT                       |
|---------------------------------|--------------------------------------|
| **\_DMO E \_ INVALIDTYPE**         | **MF \_ E \_ INVALIDTYPE**               |
| **\_DMO E \_ INVALIDSTREAMINDEX**  | **MF \_ E \_ INVALIDSTREAMNUMBER**       |
| **\_DMO E \_ NOTACCEPTING**        | **MF \_ E \_ NOTACCEPTING**              |
| **\_DMO E \_ NON \_ PIÙ \_ ELEMENTI**     | **MF \_ E NON PIÙ \_ \_ \_ TIPI**           |
| **\_DMO TIPO \_ E \_ NON \_ ACCETTATO** | **MF \_ E \_ INVALIDMEDIATYPE**          |
| **\_DMO TIPO \_ E \_ NON \_ IMPOSTATO**      | **TIPO DI \_ TRASFORMAZIONE MF \_ E NON \_ \_ \_ IMPOSTATO** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Creazione di oggetti DMO/MFT ibridi

[**L'interfaccia IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) è basata in modo libero su [**IMediaObject,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)che è l'interfaccia principale per gli oggetti multimediali (DMO) DirectX. È possibile creare oggetti che espongono entrambe le interfacce. Tuttavia, ciò può causare conflitti di denominazione, perché le interfacce hanno alcuni metodi che condividono lo stesso nome. È possibile risolvere questo problema in uno dei due modi seguenti:

Soluzione 1: includere la riga seguente all'inizio di qualsiasi file con estensione cpp che contiene funzioni MFT:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

In questo modo viene modificata la dichiarazione [**dell'interfaccia IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) in modo che la maggior parte dei nomi di metodo sia preceduta da "MFT". Di conseguenza, [**IMFTransform::P rocessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) diventa **IMFTransform::MFTProcessInput,** mentre [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) mantiene il nome originale. Questa tecnica è particolarmente utile se si converte un DMO esistente in un DMO/MFT ibrido. È possibile aggiungere i nuovi metodi MFT senza modificare i DMO mft.

Soluzione 2: usare la sintassi C++ per disambiguare i nomi ereditati da più interfacce. Ad esempio, dichiarare la versione MFT di [**ProcessInput come**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) segue:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Dichiarare la versione DMO di [**ProcessInput come**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) segue:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Se si effettua una chiamata interna a un metodo all'interno dell'oggetto , è possibile usare questa sintassi, ma in questo modo verrà eseguito l'override dello stato virtuale del metodo. Un modo migliore per effettuare chiamate dall'interno dell'oggetto è il seguente:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

In questo modo, se si deriva un'altra classe da **CMyHybridObject** ed si esegue l'override del metodo CMyHybridObject::IMediaObject::P rocessInput, viene chiamato il metodo virtuale corretto. Le DMO sono documentate nella documentazione DirectShow SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 
