---
description: Le trasformazioni di Media Foundation (MFTs) sono un'evoluzione del modello di trasformazione introdotto per la prima volta con DirectX Media Objects (DMOs).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Confronto tra MFT e DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e76e128ece1609f25e053486dbb6bcf4578161c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049317"
---
# <a name="comparison-of-mfts-and-dmos"></a>Confronto tra MFT e DMO

Le trasformazioni di Media Foundation (MFTs) sono un'evoluzione del modello di trasformazione introdotto per la prima volta con DirectX Media Objects (DMOs). Questo argomento riepiloga i modi principali in cui MFTs è diverso da DMOs. Leggere questo argomento se si ha già familiarità con le interfacce DMO o se si vuole convertire un DMO esistente in un MFT.

In questo argomento sono incluse le sezioni seguenti:

-   [Numero di flussi](#number-of-streams)
-   [Negoziazione del formato](#format-negotiation)
-   [Streaming](#streaming)
    -   [Allocazione di risorse](#allocating-resources)
    -   [Elaborazione dei dati](#processing-data)
    -   [Flushing](#flushing)
    -   [Discontinuità di flusso](#stream-discontinuities)
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
-   [Creazione di oggetti DMO/MFT ibridi](#creating-hybrid-dmomft-objects)
-   [Argomenti correlati](#related-topics)

## <a name="number-of-streams"></a>Numero di flussi

Un DMO ha un numero fisso di flussi, mentre un MFT può supportare un numero dinamico di flussi. Il client può aggiungere flussi di input e MFT può aggiungere nuovi flussi di output durante l'elaborazione. Tuttavia, MFTs non devono supportare flussi dinamici. Un MFT può avere un numero fisso di flussi, proprio come un DMO.

Per supportare i flussi dinamici in un MFT, vengono usati i metodi seguenti:

-   [**IMFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMFTransform::D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMFTransform::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Inoltre, il metodo [**IMFTransform::P rocessoutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) definisce il comportamento per l'aggiunta o la rimozione di flussi di output.

Poiché DMOs hanno flussi fissi, i flussi in un DMO vengono identificati con valori di indice in base zero. MFTs, d'altra parte, usare gli identificatori di flusso che non necessariamente corrispondono ai valori di indice. Questo perché il numero di flussi in un MFT potrebbe cambiare. Ad esempio, il flusso 0 potrebbe essere rimosso, lasciando il flusso 1 come primo flusso. Tuttavia, un MFT con un numero fisso di flussi deve osservare la stessa convenzione di DMOs e usare i valori di indice per gli identificatori di flusso.

## <a name="format-negotiation"></a>Negoziazione del formato

MFTs usare l'interfaccia [**IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) per descrivere i tipi di supporto. In caso contrario, la negoziazione del formato con MFTs funziona sugli stessi principi di base di DMOs. La tabella seguente elenca i metodi di negoziazione del formato per DMOs e i metodi corrispondenti per MFTs.



| DMO (metodo)                                                                        | MFT (metodo)                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMFTransform::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**IMFTransform::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMFTransform::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**IMFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Streaming

Analogamente a DMOs, MFTs elaborano i dati tramite chiamate a metodi [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Di seguito sono riportate le principali differenze tra i processi DMO e MFT durante il flusso di dati.

### <a name="allocating-resources"></a>Allocazione di risorse

Per MFTs non sono disponibili i metodi [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) e [**IMediaObject:: FreeStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) utilizzati con DMOS. Per gestire l'allocazione e la deallocazione delle risorse in modo efficiente, un MFT può rispondere ai messaggi seguenti nel metodo [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) :

-   [**\_notifica di \_ \_ inizio \_ trasmissione del messaggio MFT**](mft-message-notify-begin-streaming.md)
-   [**\_ \_ avvio notifica messaggio \_ MFT \_ del \_ flusso**](mft-message-notify-start-of-stream.md)

Inoltre, il client può segnalare l'inizio e la fine di un flusso chiamando [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con i messaggi seguenti:

-   [**\_ \_ \_ fine \_ del flusso di notifica del messaggio MFT \_**](mft-message-notify-end-of-stream.md)
-   [**\_ \_ \_ flusso finale notifiche messaggio \_ MFT**](mft-message-notify-end-streaming.md)

Questi due messaggi non hanno un equivalente DMO esatto.

### <a name="processing-data"></a>Elaborazione dei dati

MFTs usano esempi di supporti per conservare i dati di input e di output. Gli esempi di supporti espongono l'interfaccia [**IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) e contengono i dati seguenti:

-   Timestamp e durata.
-   Attributi contenenti informazioni per campione. Per un elenco di attributi, vedere [esempi di attributi](sample-attributes.md).
-   Zero o più buffer multimediali. Ogni buffer multimediale espone l'interfaccia [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) .

L'interfaccia [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) è simile all'interfaccia DMO **IMediaBuffer** . Per accedere al buffer di memoria sottostante, chiamare [**IMFMediaBuffer:: Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Questo metodo è approssimativamente equivalente a [**IMediaBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) per DMOS.

Per i dati video non compressi, un buffer multimediale potrebbe supportare anche l'interfaccia [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) . Un MFT che elabora il video non compresso (come input o output) deve essere preparato per usare l'interfaccia **IMF2DBuffer** se il buffer lo espone. Per altre informazioni, vedere [buffer video non compressi](uncompressed-video-buffers.md).

Media Foundation fornisce alcune implementazioni standard di [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer), pertanto non è in genere necessario scrivere un'implementazione personalizzata. Per creare un buffer DMO da un buffer di Media Foundation, chiamare [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).

### <a name="flushing"></a>Flushing

MFTs non dispone di un metodo di [**svuotamento**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) . Per scaricare un MFT, chiamare [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio di [**\_ \_ \_ scaricamento del comando del messaggio MFT**](mft-message-command-flush.md) .

### <a name="stream-discontinuities"></a>Discontinuità di flusso

MFTs non hanno un metodo di [**discontinuità**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) . Per segnalare una discontinuità in un flusso, impostare l'attributo di [**\_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) nell'esempio di input.

## <a name="miscellaneous-differences"></a>Differenze varie

Di seguito sono riportate alcune differenze secondarie aggiuntive tra MFTs e DMOs.

-   Non sono presenti equivalenti MFT per i seguenti metodi DMO:
    -   [**IMediaObject:: Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   MFTs non sono necessarie per supportare l'aggregazione.
-   MFTs supporta un'operazione denominata *svuotamento*. Lo scopo dello svuotamento consiste nell'elaborare tutti i dati che rimangono in MF, senza fornire altri dati di input alla MFT, ad esempio alla fine del flusso. Per svuotare un MFT, chiamare [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio di [**svuotamento del \_ \_ comando \_ del messaggio MFT**](mft-message-command-drain.md) . Per altre informazioni, vedere [modello di elaborazione MFT di base](basic-mft-processing-model.md).
-   MFTs può includere attributi, inclusi gli attributi per flusso. Usare i metodi seguenti per ottenere gli attributi da un MFT:

    -   [**IMFTransform:: GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   MFTs è in grado di elaborare gli eventi. Per inviare un evento a un MFT, chiamare [**IMFTransform::P rocessevent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent). Un MFT può inviare un evento al client tramite il metodo [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Per altre informazioni, vedere [modello di elaborazione MFT di base](basic-mft-processing-model.md).

## <a name="flags"></a>Flags

Le tabelle seguenti elencano i diversi flag DMO e i rispettivi equivalenti MFT. Ogni volta che viene eseguito il mapping diretto di un flag DMO a un flag MFT, entrambi i flag hanno lo stesso valore numerico. Alcuni flag DMO, tuttavia, non hanno esattamente equivalenti MFT e viceversa.

### <a name="processinput-flags"></a>Flag ProcessInput

Enumerazione [**\_ flag del \_ \_ buffer dei \_ \_ dati di input**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) DMOS: DMO.

MFTs: nessuna enumerazione equivalente.



| Flag DMO                                  | Flag MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ BUFFERF \_ SyncPoint dati di input DMO**  | Nessun flag equivalente. Impostare invece l'attributo [**\_ CleanPoint di MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) nell'esempio. |
| **\_ \_ \_ tempo BUFFERF dati di input DMO \_**       | Nessun flag equivalente. In alternativa, chiamare [**IMFSample:: SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) nell'esempio.                                  |
| **\_ \_ \_ BUFFERF \_ TIMELENGTH dati di input DMO** | Nessun flag equivalente. In alternativa, chiamare [**IMFSample:: SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) nell'esempio.                          |



 

### <a name="processoutput-flags"></a>Flag ProcessOutput

Enumerazione [**\_ flag di \_ \_ output del \_ processo**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) DMOS: DMO.

MFTs: enumerazione di [**\_ \_ flag di \_ output \_ del processo MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags) .



| Flag DMO                                            | Flag MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **\_ \_ eliminazione output processo \_ DMO \_ se \_ nessun \_ buffer** | **\_ \_ eliminazione output processo \_ MFT \_ se \_ nessun \_ buffer** |



 

Enumerazione [**\_ flag del \_ \_ buffer dei \_ \_ dati di output**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) DMOS: DMO.


MFTs: enumerazione [**\_ \_ \_ dei \_ \_ flag del buffer dei dati di output di MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags) .



| Flag DMO                                   | Flag MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ SyncPoint BUFFERF dati di output DMO \_**  | Nessun flag equivalente. Controllare invece l'attributo [**\_ CleanPoint di MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) nell'esempio. |
| **\_ \_ \_ tempo BUFFERF dati di output DMO \_**       | Nessun flag equivalente. In alternativa, chiamare [**IMFSample:: GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) nell'esempio.                                        |
| **\_ \_ \_ TIMELENGTH BUFFERF dati di output DMO \_** | Nessun flag equivalente. In alternativa, chiamare [**IMFSample:: GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) nell'esempio.                                |
| **\_BUFFERF dati di output DMO \_ \_ \_ incompleti** | **\_ \_ buffer dei dati di output MFT \_ \_ incompleto**                                                                                                           |
| Nessun flag equivalente.                        | **\_modifica del \_ formato del buffer dei dati di output MFT \_ \_ \_**                                                                                                       |
| Nessun flag equivalente.                        | **\_ \_ \_ \_ fine flusso buffer dei dati di output MFT \_**                                                                                                          |
| Nessun flag equivalente.                        | **\_ \_ buffer dei dati di output MFT \_ \_ nessun \_ esempio**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Flag GetInputStatus

Enumerazione **\_ flag di \_ \_ stato di \_ input** DMOS: DMO.

MFTs: enumerazione [**\_ \_ flag di \_ stato \_ di input MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags) .



| Flag DMO                              | Flag MFT                             |
|---------------------------------------|--------------------------------------|
| **\_STATUSF di input DMO \_ \_ accetta \_ dati** | **\_stato input MFT- \_ \_ accetta \_ dati** |



 

### <a name="getoutputstatus-flags"></a>Flag GetOutputStatus

DMOs: nessuna enumerazione equivalente.

MFTs: enumerazione di [**\_ \_ flag di \_ stato \_ dell'output di MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags) .



| Flag DMO            | Flag MFT                               |
|---------------------|----------------------------------------|
| Nessun flag equivalente. | **\_esempio di stato dell'output MFT \_ \_ \_ pronto** |



 

### <a name="getinputstreaminfo-flags"></a>Flag GetInputStreamInfo

Enumerazione [**\_ \_ \_ \_ \_ flag info flusso di input**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) DMOS: DMO.

MFTs: enumerazione [**\_ \_ \_ \_ \_ flag info flusso di input MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags) .



| Flag DMO                                             | Flag MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **\_esempi di \_ STREAMF di input \_ DMO \_**              | **\_esempi di \_ tutti i flussi di input MFT \_ \_**              |
| **\_esempio di STREAMF di input DMO \_ \_ singolo \_ \_ per \_ buffer** | **\_esempio di flusso di input MFT \_ \_ singolo \_ \_ per \_ buffer** |
| **\_ \_ \_ \_ dimensioni campione fisse STREAMF input \_ DMO**         | **\_dimensioni del \_ \_ campione fisso \_ del flusso di input MFT \_**         |
| **\_STREAMF di input DMO \_ \_ contengono \_ buffer**              | **il \_ flusso di input MFT \_ \_ include \_ buffer**              |
| Nessun flag equivalente.                                  | **\_il flusso di input MFT non \_ \_ \_ \_ ADDREF**           |
| Nessun flag equivalente.                                  | **\_flusso di input MFT \_ \_ rimovibile**                   |
| Nessun flag equivalente.                                  | **\_flusso di input MFT \_ \_ facoltativo**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Flag GetOutputStreamInfo

Enumerazione [**\_ \_ \_ \_ \_ flag info flusso di output**](/previous-versions/ms806053(v=msdn.10)) DMOS: DMO.

MFTs: enumerazione [**\_ \_ \_ \_ \_ flag info flusso di output MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) .



| Flag DMO                                              | Flag MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **\_esempi di output DMO \_ STREAMF \_ interi \_**              | **\_esempi di flusso di output MFT \_ \_ completo \_**              |
| **\_esempio di output DMO \_ STREAMF \_ singolo \_ \_ per \_ buffer** | **\_esempio di flusso di output MFT \_ \_ singolo \_ \_ per \_ buffer** |
| **\_dimensioni del \_ \_ campione fisso \_ output DMO STREAMF \_**         | **\_dimensioni del \_ \_ campione fisso \_ del flusso di output MFT \_**         |
| **\_STREAMF output \_ DMO \_**                 | **\_flusso di output MFT \_ \_ scartabile**                 |
| **\_STREAMF output \_ DMO \_ facoltativo**                    | **\_flusso di output MFT \_ \_ facoltativo**                    |
| Nessun flag equivalente.                                   | **il \_ flusso di output MFT \_ \_ fornisce \_ esempi**           |
| Nessun flag equivalente.                                   | **il \_ flusso di output MFT \_ \_ può \_ fornire \_ esempi**       |
| Nessun flag equivalente.                                   | **\_ \_ \_ lettura Lazy flusso di output MFT \_**                  |
| Nessun flag equivalente.                                   | **\_flusso di output MFT \_ \_ rimovibile**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Flag SetInputType/SetOutputType

Enumerazione DMOs: [**\_ DMO \_ imposta \_ \_ flag di tipo**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags) .

MFTs: enumerazione di [**\_ \_ \_ \_ flag di tipo set MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags) .



| Flag DMO                        | Flag MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **\_ \_ \_ solo test TYPEF set \_ DMO** | **\_ \_ solo test del tipo di set di \_ MFT \_**                                                       |
| **\_set DMO \_ TYPEF \_ Clear**      | Nessun flag equivalente. Impostare invece il tipo di supporto su **null** per cancellare il tipo di supporto. |



 

## <a name="error-codes"></a>Codici errore

La tabella seguente illustra come eseguire il mapping dei codici di errore DMO ai codici di errore MFT. Un oggetto MFT/DMO ibrido deve restituire i codici di errore DMO dai metodi [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e i codici di errore MFT dei metodi [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) . I codici di errore DMO sono definiti nel file di intestazione MediaErr. h. I codici di errore MFT sono definiti nel file di intestazione mferror. h.



| Codice di errore DMO                  | Codice errore MFT                       |
|---------------------------------|--------------------------------------|
| **DMO \_ E \_ INVALIDTYPE**         | **MF \_ E \_ INVALIDTYPE**               |
| **DMO \_ E \_ INVALIDSTREAMINDEX**  | **MF \_ E \_ INVALIDSTREAMNUMBER**       |
| **DMO \_ E \_ NOTACCEPTING**        | **MF \_ E \_ NOTACCEPTING**              |
| **DMO \_ E \_ nessun \_ altro \_ elemento**     | **MF \_ E \_ nessun \_ altro \_ tipo**           |
| **\_tipo DMO \_ E \_ non \_ accettato** | **MF \_ E \_ INVALIDMEDIATYPE**          |
| **\_tipo DMO \_ E \_ non \_ impostato**      | **\_tipo di trasformazione MF E \_ \_ \_ non \_ impostato** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Creazione di oggetti DMO/MFT ibridi

L'interfaccia [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) è vagamente basata su [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), che è l'interfaccia principale per gli oggetti multimediali DirectX (DMOS). È possibile creare oggetti che espongono entrambe le interfacce. Tuttavia, ciò può causare conflitti di denominazione, perché le interfacce hanno alcuni metodi che condividono lo stesso nome. È possibile risolvere questo problema in uno dei due modi seguenti:

Soluzione 1: includere la riga seguente all'inizio di un file con estensione cpp contenente funzioni MFT:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

In questo modo viene modificata la dichiarazione dell'interfaccia [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) in modo che la maggior parte dei nomi di metodo siano preceduti da "MFT". Quindi, [**IMFTransform::P rocessinput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) diventa **IMFTransform:: MFTProcessInput**, mentre [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) mantiene il nome originale. Questa tecnica è particolarmente utile se si converte un DMO esistente in un DMO/MFT ibrido. È possibile aggiungere i nuovi metodi MFT senza modificare i metodi DMO.

Soluzione 2: usare la sintassi C++ per evitare ambiguità nei nomi ereditati da più di un'interfaccia. Ad esempio, dichiarare la versione MFT di [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) come indicato di seguito:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Dichiarare la versione DMO di [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) come segue:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Se si effettua una chiamata interna a un metodo all'interno dell'oggetto, è possibile usare questa sintassi, ma in questo modo verrà eseguito l'override dello stato virtuale del metodo. Un modo migliore per effettuare chiamate dall'interno dell'oggetto è il seguente:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

In questo modo, se si deriva un'altra classe da **CMyHybridObject** e si esegue l'override del metodo CMyHybridObject:: IMediaObject::P rocessinput, viene chiamato il metodo virtuale corretto. Le interfacce DMO sono documentate nella documentazione di DirectShow SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
