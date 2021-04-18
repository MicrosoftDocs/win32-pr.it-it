---
description: In questo argomento viene descritta l'elaborazione asincrona dei dati per le trasformazioni di Media Foundation (MFTs).
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: MFTs asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a16950cf431eff16f2befb382a77910c49ccb2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305518"
---
# <a name="asynchronous-mfts"></a>MFTs asincrono

In questo argomento viene descritta l'elaborazione asincrona dei dati per le trasformazioni di Media Foundation (MFTs).

> [!Note]  
> Questo argomento si applica a Windows 7 o versione successiva.

 

-   [Informazioni su MFTs asincrono](#about-asynchronous-mfts)
-   [Requisiti generali](#general-requirements)
-   [Eventi](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Svuotamento](#draining)
-   [Flushing](#flushing)
-   [Indicatori](#markers)
-   [Modifiche al formato](#format-changes)
-   [Attributes (Attributi)](#attributes)
-   [Sblocco MFTs asincrono](#unlocking-asynchronous-mfts)
-   [Arresto della MFT](#shutting-down-the-mft)
-   [Registrazione ed enumerazione](#registration-and-enumeration)
-   [Argomenti correlati](#related-topics)

## <a name="about-asynchronous-mfts"></a>Informazioni su MFTs asincrono

Quando MFTs è stato introdotto in Windows Vista, l'API è stata progettata per l'elaborazione *sincrona* dei dati. In tale modello, il MFT è sempre in attesa di ottenere l'input o di generare l'output.

Si consideri un decodificatore video tipico. Per ottenere un frame decodificato, il client chiama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Se il decodificatore ha un numero sufficiente di dati per decodificare un frame, **ProcessOutput** si blocca mentre il MFT decodifica il frame. In caso contrario, **ProcessOutput** restituisce **MF_E_TRANSFORM_NEED_MORE_INPUT**, che indica che il client deve chiamare [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Questo modello funziona bene se il decodificatore esegue tutte le operazioni di decodifica su un solo thread. Si supponga, tuttavia, che il decodificatore usi diversi thread per decodificare i frame in parallelo. Per prestazioni ottimali, il decodificatore deve ricevere nuovo input ogni volta che un thread di decodifica diventa inattivo. Ma la velocità con cui i thread completano le operazioni di decodifica non verranno allineati esattamente con le chiamate del client a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput), ottenendo thread in attesa di lavoro.

Windows 7 introduce l'elaborazione *asincrona* guidata dagli eventi per MFTS. In questo modello, ogni volta che il MFT necessita di input o di output, invia un evento al client.

## <a name="general-requirements"></a>Requisiti generali

In questo argomento viene descritto come MFTs asincrono differiscono da MFT sincrono. Eccetto laddove indicato in questo argomento, i due modelli di elaborazione sono gli stessi. In particolare, la negoziazione del formato è la stessa.

Un MFT asincrono deve implementare le interfacce seguenti:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>Eventi

Una MFT asincrona utilizza gli eventi seguenti per segnalare lo stato di elaborazione dei dati:



| Event                                                    | Descrizione                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [METransformNeedInput](metransformneedinput.md)         | Inviato quando MFT può accettare più input.                          |
| [METransformHaveOutput](metransformhaveoutput.md)       | Inviato quando il MFT ha output.                                     |
| [METransformDrainComplete](metransformdraincomplete.md) | Inviato quando viene completata un'operazione di svuotamento. Vedere [svuotamento](#draining). |
| [METransformMarker](metransformmarker.md)               | Inviato quando un marcatore viene elaborato. Vedere [marcatori](#markers).           |



 

Questi eventi vengono inviati fuori banda. È importante comprendere la differenza tra gli eventi in banda e fuori banda nel contesto di un MFT.

La progettazione MFT originale supporta gli eventi *in banda* . Un evento in banda contiene informazioni sul flusso di dati, ad esempio informazioni su una modifica del formato. Il client invia eventi in banda alla MFT chiamando [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). Il MFT può inviare gli eventi in banda al client nel metodo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . In particolare, gli eventi vengono trasmessi nel membro **pEvents** della struttura [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) .)

Un MFT invia eventi fuori banda tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , come indicato di seguito:

1.  MFT implementa l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , come descritto in [generatori di eventi multimediali](media-event-generators.md).
2.  Il client chiama **IUnknown:: QueryInterface** sulla MFT per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Un MFT asincrono deve esporre questa interfaccia. MFTs sincroni non devono esporre questa interfaccia.
3.  Il client chiama [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) e [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) per ricevere eventi fuori banda dalla MFT.

## <a name="processinput"></a>ProcessInput

Il metodo [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) viene modificato nel modo seguente:

1.  All'avvio del flusso, il client invia il messaggio di [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
2.  Durante lo streaming, il MFT richiede i dati inviando un evento [METransformNeedInput](metransformneedinput.md) . I dati dell'evento sono l'identificatore del flusso.
3.  Per ogni evento [METransformNeedInput](metransformneedinput.md) , il client chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per il flusso specificato.
4.  Al termine dello streaming, il client può chiamare [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .

Note sull'implementazione:

-   Il MFT non deve inviare eventi [METransformNeedInput](metransformneedinput.md) fino a quando non riceve il messaggio di [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
-   Durante lo streaming, il MFT può inviare eventi [METransformNeedInput](metransformneedinput.md) in qualsiasi momento.
-   Il MFT deve mantenere un conteggio degli eventi [METransformNeedInput](metransformneedinput.md) in sospeso. Qualsiasi chiamata a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) che non corrisponde a un evento METransformNeedInput deve restituire **MF_E_NOTACCEPTING**.
-   Quando il MFT riceve il messaggio di [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) , reimposta il numero di eventi [METransformNeedInput](metransformneedinput.md) in sospeso su zero.
-   Il MFT non deve inviare eventi [METransformNeedInput](metransformneedinput.md) dopo la ricezione del messaggio di [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .
-   Se [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) viene chiamato prima [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) o dopo [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md), il metodo deve restituire **MF_E_NOTACCEPTING**.

## <a name="processoutput"></a>ProcessOutput

Il metodo [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) viene modificato nel modo seguente:

1.  Ogni volta che il MFT ha output, invia un evento [METransformHaveOutput](metransformhaveoutput.md) .
2.  Per ogni evento [METransformHaveOutput](metransformhaveoutput.md) , il client chiama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Note sull'implementazione:

-   Se il client chiama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in qualsiasi altro momento, il metodo restituisce **E_UNEXPECTED**.
-   Un MFT asincrono non deve mai restituire **MF_E_TRANSFORM_NEED_MORE_INPUT** dal metodo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Se il MFT richiede un maggior numero di input, invia un evento [METransformNeedInput](metransformneedinput.md) .

## <a name="draining"></a>Svuotamento

Con lo svuotamento di un MFT, il MFT produce il maggior volume di output possibile da qualsiasi dato di input già inviato. Lo svuotamento di un MFT asincrono funziona nel modo seguente:

1.  Il client invia il messaggio di [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) .
2.  Il MFT continua a inviare gli eventi [METransformHaveOutput](metransformhaveoutput.md) fino a quando non sono disponibili altri dati da elaborare. Non invia eventi [METransformNeedInput](metransformneedinput.md) durante questo periodo di tempo.
3.  Dopo l'invio dell'ultimo evento [METransformHaveOutput](metransformhaveoutput.md) da parte di MFT, viene inviato un evento [METransformDrainComplete](metransformdraincomplete.md) .

Al termine dello svuotamento, il MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino a quando non riceve un messaggio [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) dal client.

## <a name="flushing"></a>Flushing

Il client può scaricare il MFT inviando il messaggio di [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) . Il MFT Elimina tutti gli esempi di input e di output che contiene.

Il MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino a quando non riceve un messaggio [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) dal client.

## <a name="markers"></a>Indicatori

Il client può contrassegnare un punto nel flusso inviando il messaggio di [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) . Il MFT risponde nel modo seguente:

1.  Il MFT genera il numero di campioni di output possibili dai dati di input esistenti, inviando un evento [METransformHaveOutput](metransformhaveoutput.md) per ogni esempio di output.
2.  Una volta generato tutto l'output, il MFT Invia un evento [METransformMarker](metransformmarker.md) . Questo evento deve essere inviato dopo tutti gli eventi [METransformHaveOutput](metransformhaveoutput.md) .

Si supponga, ad esempio, che un decodificatore disponga di dati di input sufficienti per produrre quattro esempi di output. Se il client invia il messaggio di [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) , la funzione MFT Accoda quattro eventi [METransformHaveOutput](metransformhaveoutput.md) (uno per esempio di output), seguiti da un evento [METransformMarker](metransformmarker.md) .

Il messaggio del marcatore è simile al messaggio di svuotamento. Uno svuotamento viene tuttavia considerato un'interruzioni nel flusso, mentre un marcatore non lo è. Lo svuotamento e i marcatori presentano le differenze seguenti.

Svuotamento

-   Durante lo svuotamento, il MFT non invia gli eventi [METransformNeedInput](metransformneedinput.md) .
-   Il MFT Elimina tutti i dati di input che non possono essere usati per creare un esempio di output.
-   Alcuni MFTs producono una "coda" alla fine dei dati. Ad esempio, gli effetti audio come Reverb o echo producono dati aggiuntivi dopo l'arresto dei dati di input. Un MFT che genera una coda dovrebbe farlo al termine di un'operazione di svuotamento.
-   Al termine dello svuotamento del MFT, l'esempio di output successivo viene contrassegnato con l'attributo [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) per indicare una discontinuità nel flusso.

Marcatore

-   Il MFT continua a inviare gli eventi [METransformNeedInput](metransformneedinput.md) prima di inviare l'evento del marcatore.
-   Il MFT non rimuove i dati di input. Se sono presenti dati parziali, devono essere elaborati dopo il punto del marcatore.
-   Il MFT non produce una coda in corrispondenza del punto del marcatore.
-   Il MFT non imposta il flag di discontinuità dopo il punto del marcatore.

## <a name="format-changes"></a>Modifiche al formato

Un MFT asincrono deve supportare le modifiche del formato dinamico, come descritto in [gestione delle modifiche al flusso](handling-stream-changes.md).

## <a name="attributes"></a>Attributi

Un MFT asincrono deve implementare il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per restituire un archivio di attributi valido. Gli attributi seguenti si applicano a MFTs asincrono:



| Attributo                                                                                    | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | Il MFT deve impostare questo attributo su **true** (1). Il client può eseguire una query su questo attributo per individuare se il MFT è asincrono. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | Il MFT deve impostare questo attributo su **true** (1). Il client può presumere che l'attributo sia impostato.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Sblocco MFTs asincrono

MFTs asincroni non sono compatibili con il modello di elaborazione dati MFT originale. Per impedire che MFTs asincrono interferisca con le applicazioni esistenti, viene definito il meccanismo seguente:

<dl> Il client chiama <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform:: GetAttributes</a> in MFT.  
Il client esegue una query per l'attributo <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> . Per un MFT asincrono, il valore di questo attributo è **true**.  
Per sbloccare il MFT, il client deve impostare l'attributo <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK</a> su **true**.  
</dl>

Fino a quando il client non sblocca il MFT, tutti i metodi [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) devono restituire **MF_E_TRANSFORM_ASYNC_LOCKED**, con le eccezioni seguenti:

-   [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (tutti MFTS asincroni)
-   [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (tutti MFTS asincroni)
-   [**IMFTransform:: GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (solo codificatori)
-   [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (solo codificatori)
-   [**IMFTransform:: GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (tutti MFTS asincroni)
-   [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (tutti MFTS asincroni)

Il codice seguente illustra come sbloccare un MFT asincrono:


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="shutting-down-the-mft"></a>Arresto della MFT

MFTs asincrono deve implementare l'interfaccia [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) .

-   [**Arresto**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown): il MFT deve arrestare la coda degli eventi. Se si usa la coda degli eventi standard, chiamare [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown). Facoltativamente, il MFT può rilasciare altre risorse. Il client non deve usare il MFT dopo la chiamata di **Shutdown**.
-   [**GetShutdownStatus**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus): dopo la chiamata di [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) , l'oggetto MFT deve restituire il valore **MFSHUTDOWN_COMPLETED** nel parametro *pStatus* . Non deve restituire il valore **MFSHUTDOWN_INITIATED**.

## <a name="registration-and-enumeration"></a>Registrazione ed enumerazione

Per registrare un MFT asincrono, chiamare la funzione [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) e impostare il flag **MFT_ENUM_FLAG_ASYNCMFT** nel parametro *Flags* . (In precedenza questo flag era riservato).

Per enumerare MFTs asincrone, chiamare la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) e impostare il flag **MFT_ENUM_FLAG_ASYNCMFT** nel parametro *Flags* . Per compatibilità con le versioni precedenti, la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) non enumera MFTS asincrono. In caso contrario, l'installazione di un MFT asincrono sul computer dell'utente potrebbe interrompere le applicazioni esistenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



