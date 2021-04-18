---
description: Mixer personalizzati
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Mixer personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7e56c578a7081de7c71ae3abaf9fc45d085827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305458"
---
# <a name="custom-mixers"></a>Mixer personalizzati

Questo argomento descrive come scrivere un mixer personalizzato per il renderer video avanzato (EVR). È possibile usare un mixer personalizzato con il Media Foundation sink di supporto EVR o il filtro EVR DirectShow. Per altre informazioni sui mixer e sui Presenter, vedere [renderer video migliorato](enhanced-video-renderer.md).

Il mixer è una trasformazione Media Foundation (MFT) con uno o più input (il flusso di riferimento più i flussi sottoflussi) e un output. Il flusso di input riceve esempi da upstream. Il flusso di output recapita esempi al Presenter. Il EVR è responsabile della chiamata a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) nel mixer e il presentatore è responsabile della chiamata a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Come minimo, un mixer EVR deve implementare le interfacce seguenti:



| Interfaccia                                                                | Descrizione                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Fornisce la funzionalità di base di MFT.                                                                 |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Consente al mixer di ottenere le interfacce dal EVR.                                                |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Consente al mixer di ottenere le interfacce dal EVR.                                                |
| [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Utilizzato per esporre l'attributo in [**\_ grado di \_ \_ riconoscere**](mf-sa-d3d-aware-attribute.md) la compatibilità con l'amministratore MF SA a EVR. |



 

Facoltativamente, un MFT può implementare una delle interfacce seguenti:



| Interfaccia                                                | Descrizione                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Obbligatorio per riprodurre contenuti protetti.                                                                                                                  |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Espone interfacce quali [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) e [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) all'applicazione. |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Consente al gestore della qualità di regolare la qualità del video.                                                                                             |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Consente all'applicazione di combinare una bitmap statica nel video.                                                                                       |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Esegue il mapping delle coordinate del fotogramma video di output alle coordinate del fotogramma video di input.                                                                  |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Espone alcune funzionalità di elaborazione video DXVA all'applicazione.                                                                                      |



 

La negoziazione del formato con il mixer funziona nel modo seguente:

1.  EVR imposta il tipo di supporto nel flusso di riferimento.
2.  EVR chiama [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) sul Presenter con il messaggio **MFVP \_ \_ INVALIDATEMEDIATYPE** Message.

3.  Il relatore imposta il tipo di supporto nel flusso di output del mixer.
4.  EVR imposta il tipo di supporto nei flussi sottoflussi.

Se il tipo di supporto per il flusso di riferimento cambia, gli altri tipi di supporto del mixer non sono più validi. Il metodo [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer avrà quindi esito negativo e restituirà la **modifica del \_ flusso MF e \_ Transform \_ \_**. A questo punto il presentatore non deve eseguire alcuna operazione. Il EVR avvierà nuovamente il processo di negoziazione del formato.

Quando un flusso di input raggiunge la fine del flusso, EVR chiama [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) sul mixer con la [**\_ \_ \_ fine \_ del \_ flusso di notifica del messaggio MFT**](mft-message-notify-end-of-stream.md).

Il mixer invia gli eventi seguenti a EVR usando l'interfaccia [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) di EVR. Questa interfaccia è documentata nella documentazione di DirectShow SDK.



| Event                                            | Descrizione                            |
|--------------------------------------------------|----------------------------------------|
| [**\_esempio EC \_ necessario**](../directshow/ec-sample-needed.md) | Il mixer richiede un nuovo esempio di input. |



 

EVR potrebbe chiamare [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer prima dell'avvio del flusso. Il mixer non deve avere esito negativo per queste chiamate. Al contrario, deve riempire la superficie di output con i pixel neri. Il mixer deve continuare a riempire gli esempi di output fino a quando non riceve un messaggio [**MFT \_ \_ Notify \_ Begin \_ streaming**](mft-message-notify-begin-streaming.md) Message o viene chiamato il metodo [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) . Se il mixer riceve un messaggio di [**\_ notifica del messaggio MFT \_ \_ End \_ streaming**](mft-message-notify-end-streaming.md) , dovrebbe tornare alla modalità di riempimento del colore.

## <a name="implementing-imfvideodeviceid"></a>Implementazione di IMFVideoDeviceID

L'interfaccia [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un metodo, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), che restituisce un GUID del dispositivo. Il GUID del dispositivo garantisce che il relatore e il mixer usino tecnologie compatibili. Se i GUID del dispositivo non corrispondono, l'inizializzazione di EVR non riesce.

Il mixer e il Presenter standard usano entrambi Direct3D 9, con il GUID del dispositivo uguale a IID \_ IDirect3DDevice9. Se si intende usare il Presenter personalizzato con il mixer standard, il GUID del dispositivo del relatore deve essere IID \_ IDirect3DDevice9. Se si sostituiscono entrambi i componenti, è possibile definire un nuovo GUID del dispositivo.

## <a name="implementing-imftopologyservicelookupclient"></a>Implementazione di IMFTopologyServiceLookupClient

Il mixer deve implementare l'interfaccia [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) . Prima dell'inizio del flusso, EVR chiama [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e passa un puntatore all'interfaccia [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) di EVR. Il mixer usa questo puntatore per ottenere i puntatori di interfaccia dal EVR.

Come minimo, il mixer deve eseguire una query per l'interfaccia seguente:

-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Quando EVR chiama [**IMFTopologyServiceLookupClient:: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers), il mixer deve rilasciare tutti i puntatori ottenuti dalla chiamata a [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers).

## <a name="mixer-attributes"></a>Attributi mixer

Un mixer deve supportare gli attributi seguenti.



| Attributo                                                                        | Descrizione                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Compatibile con \_ D3D \_**](mf-sa-d3d-aware-attribute.md)                          | Specifica se il mixer supporta l'accelerazione video DirectX (DXVA).                                                                                                                                                                               |
| [**\_ \_ \_ conteggio campioni richiesti per MF SA \_**](mf-sa-required-sample-count-attribute.md) | Il numero di campioni video che il EVR deve allocare per ogni flusso di mixer. Questo attributo si applica ai singoli flussi; usare l'archivio di attributi restituito da [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes). |



 

## <a name="setting-the-mixer-on-the-evr"></a>Impostazione del mixer in EVR

Per impostare un mixer personalizzato in EVR, chiamare [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer). Il filtro EVR DirectShow e il sink multimediale EVR implementano questo metodo.

**Oggetto attivazione EVR**. Se si usa l'oggetto attivazione EVR, è possibile fornire un mixer personalizzato impostando uno degli attributi seguenti nell'oggetto attivazione di EVR:



| Attributo                                                                                                 | Descrizione                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_attivazione del \_ \_ mixer video \_ personalizzato \_ MF Activate**](mf-activate-custom-video-mixer-activate-attribute.md) | Puntatore a un oggetto di attivazione per il mixer. L'oggetto Activation deve implementare l'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . |
| [**MF \_ attivazione \_ del \_ mixer video personalizzato \_ \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID del mixer.                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> </dl>

 

 
