---
description: Questo argomento descrive l'elaborazione asincrona dei dati Media Foundation trasformazioni MFT (Media Foundation Transform).
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: MFT asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cab2ef683ef22fd22a911c045a1a744f1c0d561b3e8e66d46ca2cf6c6f0ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959521"
---
# <a name="asynchronous-mfts"></a>MFT asincroni

Questo argomento descrive l'elaborazione asincrona dei dati Media Foundation trasformazioni MFT (Media Foundation Transform).

> [!Note]  
> Questo argomento si applica a Windows 7 o versioni successive.

 

-   [Informazioni sui MFT asincroni](#about-asynchronous-mfts)
-   [Requisiti generali](#general-requirements)
-   [Eventi](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Drenante](#draining)
-   [Flushing](#flushing)
-   [Marcatori](#markers)
-   [Modifiche al formato](#format-changes)
-   [Attributes (Attributi)](#attributes)
-   [Sblocco di MFT asincroni](#unlocking-asynchronous-mfts)
-   [Arresto di MFT](#shutting-down-the-mft)
-   [Registrazione ed enumerazione](#registration-and-enumeration)
-   [Argomenti correlati](#related-topics)

## <a name="about-asynchronous-mfts"></a>Informazioni sui MFT asincroni

Quando sono stati introdotti MFT in Windows Vista, l'API è stata progettata per *l'elaborazione sincrona* dei dati. In tale modello, il MFT è sempre in attesa di ottenere l'input o in attesa di produrre output.

Si consideri un tipico decodificatore video. Per ottenere un frame decodificato, il client chiama [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Se il decodificatore dispone di dati sufficienti per decodificare un frame, **ProcessOutput** si blocca mentre MFT decodifica il frame. In caso **contrario, ProcessOutput** **restituisce MF_E_TRANSFORM_NEED_MORE_INPUT**, che indica che il client deve chiamare [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Questo modello funziona bene se il decodificatore esegue tutte le operazioni di decodifica in un unico thread. Si supponga tuttavia che il decodificatore usi più thread per decodificare i fotogrammi in parallelo. Per ottenere prestazioni ottimali, il decodificatore deve ricevere nuovo input ogni volta che un thread di decodifica diventa inattivo. Tuttavia, la frequenza con cui i thread completano le operazioni di decodifica non sarà allineata esattamente con le chiamate del client a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)determinando l'attesa del lavoro da parte dei thread.

Windows 7 introduce l'elaborazione asincrona *basata* su eventi per MFT. In questo modello, ogni volta che il MFT necessita di input o di output, invia un evento al client.

## <a name="general-requirements"></a>Requisiti generali

Questo argomento descrive le differenze tra MFT asincroni e MFT sincroni. Ad eccezione dei casi in cui è stato illustrato in questo argomento, i due modelli di elaborazione sono gli stessi. In particolare, la negoziazione del formato è la stessa.

Un MFT asincrono deve implementare le interfacce seguenti:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>Eventi

Un MFT asincrono usa gli eventi seguenti per segnalare lo stato di elaborazione dei dati:



| Event                                                    | Descrizione                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [METransformNeedInput](metransformneedinput.md)         | Inviato quando il MFT può accettare più input.                          |
| [METransformHaveOutput](metransformhaveoutput.md)       | Inviato quando l'output di MFT è .                                     |
| [METransformDrainComplete](metransformdraincomplete.md) | Inviato al completamento di un'operazione di svuotamento. Vedere [Svuotamento.](#draining) |
| [METransformMarker](metransformmarker.md)               | Inviato quando è in corso l'elaborazione di un marcatore. Vedere [Marcatori.](#markers)           |



 

Questi eventi vengono inviati fuori banda. È importante comprendere la differenza tra gli eventi in banda e fuori banda nel contesto di un MFT.

La progettazione MFT originale supporta *gli eventi in banda.* Un evento in banda contiene informazioni sul flusso di dati, ad esempio informazioni su una modifica del formato. Il client invia gli eventi in banda al MFT chiamando [**IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). MFT può inviare eventi in banda al client nel [**metodo ProcessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) In particolare, gli eventi vengono trasmessi nel **membro pEvents** della [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) struttura .

Un MFT invia eventi fuori banda tramite [**l'interfaccia IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) come indicato di seguito:

1.  MFT implementa [**l'interfaccia IMFMediaEventGenerator,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) come descritto in [Generatori di eventi multimediali.](media-event-generators.md)
2.  Il client chiama **IUnknown::QueryInterface** su MFT per [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Un MFT asincrono deve esporre questa interfaccia. I MFT sincroni non devono esporre questa interfaccia.
3.  Il client chiama [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) e [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) per ricevere eventi fuori banda da MFT.

## <a name="processinput"></a>ProcessInput

Il [**metodo IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) viene modificato come segue:

1.  All'avvio del flusso, il client invia [**il MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) messaggio.
2.  Durante lo streaming, MFT richiede i dati inviando un [evento METransformNeedInput.](metransformneedinput.md) I dati dell'evento sono l'identificatore del flusso.
3.  Per ogni [evento METransformNeedInput,](metransformneedinput.md) il client chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per il flusso specificato.
4.  Al termine del flusso, il client può chiamare [**ProcessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) il [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) messaggio.

Note sull'implementazione:

-   MFT non deve inviare alcun [evento METransformNeedInput](metransformneedinput.md) fino a quando non riceve il [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) messaggio.
-   Durante lo streaming, il MFT può [inviare eventi METransformNeedInput](metransformneedinput.md) in qualsiasi momento.
-   MFT deve mantenere un conteggio degli eventi [METransformNeedInput](metransformneedinput.md) in sospeso. Qualsiasi chiamata a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) che non corrisponde a un evento METransformNeedInput deve restituire **MF_E_NOTACCEPTING**.
-   Quando il MFT riceve il [**messaggio MFT_MESSAGE_NOTIFY_END_OF_STREAM,**](mft-message-notify-end-of-stream.md) reimposta il conteggio degli eventi [METransformNeedInput](metransformneedinput.md) in sospeso su zero.
-   Il MFT non deve inviare alcun [evento METransformNeedInput](metransformneedinput.md) dopo aver ricevuto il [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) messaggio.
-   Se [**ProcessInput viene**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) chiamato [**prima**](mft-message-notify-start-of-stream.md) MFT_MESSAGE_NOTIFY_START_OF_STREAM [**o**](mft-message-notify-end-of-stream.md)dopo MFT_MESSAGE_NOTIFY_END_OF_STREAM , il metodo deve restituire **MF_E_NOTACCEPTING**.

## <a name="processoutput"></a>ProcessOutput

Il [**metodo IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) viene modificato come segue:

1.  Ogni volta che l'output di MFT è , invia un [evento METransformHaveOutput.](metransformhaveoutput.md)
2.  Per ogni [evento METransformHaveOutput,](metransformhaveoutput.md) il client chiama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Note sull'implementazione:

-   Se il client chiama [**ProcessOutput in**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) qualsiasi altro momento, il metodo restituisce **E_UNEXPECTED**.
-   Un MFT asincrono non deve mai **MF_E_TRANSFORM_NEED_MORE_INPUT** dal [**metodo ProcessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Se MFT richiede più input, invia un [evento METransformNeedInput.](metransformneedinput.md)

## <a name="draining"></a>Drenante

Lo svuotamento di un MFT fa sì che il MFT produca la maggior quantità possibile di output da tutti i dati di input già inviati. Lo svuotamento di un MFT asincrono funziona come segue:

1.  Il client invia il [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) messaggio.
2.  MFT continua a inviare [gli eventi METransformHaveOutput](metransformhaveoutput.md) finché non contiene altri dati da elaborare. Non invia eventi [METransformNeedInput](metransformneedinput.md) durante questo periodo di tempo.
3.  Dopo l'invio dell'ultimo [evento METransformHaveOutput,](metransformhaveoutput.md) MFT invia un [evento METransformDrainComplete.](metransformdraincomplete.md)

Al termine dello svuotamento, MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino [**a**](mft-message-notify-start-of-stream.md) quando non riceve un messaggio MFT_MESSAGE_NOTIFY_START_OF_STREAM dal client.

## <a name="flushing"></a>Flushing

Il client può scaricare il MFT inviando il [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) messaggio. MFT elimina tutti i campioni di input e output che contiene.

MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino a quando non riceve un messaggio [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) dal client.

## <a name="markers"></a>Marcatori

Il client può contrassegnare un punto nel flusso inviando il [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) messaggio. MFT risponde come segue:

1.  MFT genera il maggior numero possibile di esempi di output dai dati di input esistenti, inviando un evento [METransformHaveOutput](metransformhaveoutput.md) per ogni esempio di output.
2.  Dopo la generazione di tutto l'output, MFT invia un [evento METransformMarker.](metransformmarker.md) Questo evento deve essere inviato dopo tutti gli [eventi METransformHaveOutput.](metransformhaveoutput.md)

Si supponga, ad esempio, che un decodificatore abbia dati di input sufficienti per produrre quattro campioni di output. Se il client invia il [**messaggio MFT_MESSAGE_COMMAND_MARKER,**](mft-message-command-marker.md) MFT accoderà quattro eventi [METransformHaveOutput](metransformhaveoutput.md) (uno per ogni esempio di output), seguiti da un [evento METransformMarker.](metransformmarker.md)

Il messaggio del marcatore è simile al messaggio di svuotamento. Tuttavia, uno svuotamento è considerato un'interruzione nel flusso, mentre un marcatore non lo è. Lo svuotamento e i marcatori hanno le differenze seguenti.

Drenante:

-   Durante lo svuotamento, MFT non invia [eventi METransformNeedInput.](metransformneedinput.md)
-   MFT elimina tutti i dati di input che non possono essere utilizzati per creare un esempio di output.
-   Alcuni MFT producono una "coda" alla fine dei dati. Ad esempio, gli effetti audio come riverbero o echo producono dati aggiuntivi dopo l'arresto dei dati di input. Un MFT che genera una coda deve eseguire questa operazione alla fine di un'operazione di svuotamento.
-   Al termine dello svuotamento, il MFT contrassegna l'esempio di output successivo con l'attributo [**MFSampleExtension_Discontinuity,**](mfsampleextension-discontinuity-attribute.md) per indicare una discontinuità nel flusso.

Marcatore:

-   MFT continua a inviare gli [eventi METransformNeedInput](metransformneedinput.md) prima di inviare l'evento marcatore.
-   MFT non elimina i dati di input. Se sono presenti dati parziali, devono essere elaborati dopo il punto marcatore.
-   MFT non produce una coda in corrispondenza del punto del marcatore.
-   MFT non imposta il flag di discontinuità dopo il punto marcatore.

## <a name="format-changes"></a>Modifiche al formato

Un MFT asincrono deve supportare le modifiche di formato dinamico, come descritto in [Gestione delle modifiche del flusso.](handling-stream-changes.md)

## <a name="attributes"></a>Attributi

Un MFT asincrono deve implementare [**il metodo IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per restituire un archivio di attributi valido. Gli attributi seguenti si applicano ai MFT asincroni:



| Attributo                                                                                    | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | MFT deve impostare questo attributo su **TRUE** (1). Il client può eseguire una query su questo attributo per individuare se l'MFT è asincrono. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | MFT deve impostare questo attributo su **TRUE** (1). Il client può presupporre che questo attributo sia impostato.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Sblocco di MFT asincroni

I MFT asincroni non sono compatibili con il modello di elaborazione dati MFT originale. Per impedire l'interruzione di applicazioni esistenti da parte di MFT asincroni, viene definito il meccanismo seguente:

<dl> Il client chiama <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform::GetAttributes</a> su MFT.  
Il client esegue una query su per questo <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> attributo . Per un MFT asincrono, il valore di questo attributo è **TRUE.**  
Per sbloccare MFT, il client deve impostare <a href="mf-transform-async-unlock.md">l'attributo MF_TRANSFORM_ASYNC_UNLOCK</a> su **TRUE.**  
</dl>

Finché il client non sblocca MFT, tutti i metodi [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) devono restituire MF_E_TRANSFORM_ASYNC_LOCKED **,** con le eccezioni seguenti:

-   [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (tutti i MFT asincroni)
-   [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (tutti i MFT asincroni)
-   [**IMFTransform::GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (solo codificatori)
-   [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (solo codificatori)
-   [**IMFTransform::GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (tutti i MFT asincroni)
-   [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (tutti i MFT asincroni)

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



## <a name="shutting-down-the-mft"></a>Arresto di MFT

I MFT asincroni devono implementare [**l'interfaccia IMFShutdown.**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

-   [**Shutdown:**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown)MFT deve arrestare la coda degli eventi. Se si usa la coda eventi standard, chiamare [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown). Facoltativamente, MFT può rilasciare altre risorse. Il client non deve usare MFT dopo aver chiamato **Shutdown**.
-   [**GetShutdownStatus:**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus)dopo la chiamata di [**Shutdown,**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) MFT deve restituire il valore MFSHUTDOWN_COMPLETED **nel** *parametro pStatus.* Non deve restituire il valore **MFSHUTDOWN_INITIATED**.

## <a name="registration-and-enumeration"></a>Registrazione ed enumerazione

Per registrare un MFT asincrono, chiamare la [**funzione MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) e impostare il flag **MFT_ENUM_FLAG_ASYNCMFT** nel *parametro Flags.* In precedenza questo flag era riservato.

Per enumerare i flag MFT asincroni, chiamare la [**funzione MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) e impostare **MFT_ENUM_FLAG_ASYNCMFT** flag nel *parametro Flags.* Per compatibilità con le versioni precedenti, [**la funzione MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) non enumera i MFT asincroni. In caso contrario, l'installazione di un MFT asincrono nel computer dell'utente potrebbe interrompere le applicazioni esistenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 



