---
description: Mixer personalizzati
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Mixer personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587206f7bc34d1fad4a64a12aeff9ab8ad21e18a84c92c8f2302776fdc126a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605991"
---
# <a name="custom-mixers"></a>Mixer personalizzati

Questo argomento descrive come scrivere un mixer personalizzato per il renderer video avanzato (EVR). È possibile usare un mixer personalizzato con il sink Media Foundation supporto EVR o il DirectShow EVR. Per altre informazioni su mixer e relatori, vedere [Renderer video avanzato.](enhanced-video-renderer.md)

Il mixer è una Media Foundation (MFT) con uno o più input (il flusso di riferimento più i flussi secondari) e un output. Il flusso di input riceve esempi da upstream. Il flusso di output fornisce esempi al presentatore. EVR è responsabile della chiamata di [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) sul mixer e il presentatore è responsabile della chiamata di [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Come minimo, un mixer EVR deve implementare le interfacce seguenti:



| Interfaccia                                                                | Descrizione                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Fornisce la funzionalità MFT di base.                                                                 |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Consente al mixer di ottenere le interfacce da EVR.                                                |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Consente al mixer di ottenere le interfacce da EVR.                                                |
| [**Attributi IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Usato per esporre [**l'attributo \_ MF SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) all'EVR. |



 

Facoltativamente, un MFT può implementare una delle interfacce seguenti:



| Interfaccia                                                | Descrizione                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Necessario per riprodurre contenuto protetto.                                                                                                                  |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Espone all'applicazione interfacce come [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) e [**IMFVideoProcessor.**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Consente al gestore della qualità di regolare la qualità del video.                                                                                             |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Consente all'applicazione di combinare una bitmap statica nel video.                                                                                       |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Mappe coordinate del fotogramma video di output alle coordinate sul fotogramma video di input.                                                                  |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Espone alcune funzionalità di elaborazione video DXVA all'applicazione.                                                                                      |



 

La negoziazione del formato con il mixer funziona come segue:

1.  L'EVR imposta il tipo di supporto nel flusso di riferimento.
2.  L'EVR chiama [**IMFVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) sul presentatore con il messaggio **MFVP \_ MESSAGE \_ INVALIDATEMEDIATYPE.**

3.  Il presentatore imposta il tipo di supporto nel flusso di output del mixer.
4.  L'EVR imposta il tipo di supporto nei sottostream.

Se il tipo di supporto nel flusso di riferimento cambia, gli altri tipi di supporti del mixer non sono più validi. Il metodo [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer avrà quindi esito negativo e restituirà **MF \_ E TRANSFORM STREAM \_ \_ \_ CHANGE**. A questo punto, il presentatore non deve eseguire alcun'operazione. EVR avvierà di nuovo il processo di negoziazione del formato.

Quando un flusso di input raggiunge la fine del flusso, EVR chiama [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) sul mixer con [**MFT \_ MESSAGE NOTIFY END OF \_ \_ \_ \_ STREAM**](mft-message-notify-end-of-stream.md).

Il mixer invia gli eventi seguenti all'EVR, usando [**l'interfaccia IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) di EVR. Questa interfaccia è documentata nella documentazione DirectShow SDK.



| Event                                            | Descrizione                            |
|--------------------------------------------------|----------------------------------------|
| [**EC \_ SAMPLE \_ NEEDED**](../directshow/ec-sample-needed.md) | Il mixer richiede un nuovo esempio di input. |



 

L'EVR potrebbe chiamare [**ProcessOutput sul**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) mixer prima dell'avvio dello streaming. Il mixer non deve avere esito negativo per queste chiamate. Deve invece riempire la superficie di output con pixel neri. Il mixer deve continuare a color fill output samples fino a quando non riceve un messaggio [**MFT \_ MESSAGE NOTIFY \_ BEGIN \_ \_ STREAMING**](mft-message-notify-begin-streaming.md) o non viene chiamato il metodo [**ProcessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) Se il mixer riceve un messaggio [**MFT \_ MESSAGE NOTIFY \_ END \_ \_ STREAMING,**](mft-message-notify-end-streaming.md) deve tornare alla modalità di riempimento a colori.

## <a name="implementing-imfvideodeviceid"></a>Implementazione di IMFVideoDeviceID

[**L'interfaccia IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un metodo, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)che restituisce un GUID del dispositivo. Il GUID del dispositivo garantisce che il presentatore e il mixer usino tecnologie compatibili. Se i GUID del dispositivo non corrispondono, l'inizializzazione dell'EVR non riesce.

Il mixer e il presentatore standard usano entrambi Direct3D 9, con il GUID del dispositivo uguale a IID \_ IDirect3DDevice9. Se si intende usare il presentatore personalizzato con il mixer standard, il GUID del dispositivo del presentatore deve essere IID \_ IDirect3DDevice9. Se si sostituiscono entrambi i componenti, è possibile definire un nuovo GUID del dispositivo.

## <a name="implementing-imftopologyservicelookupclient"></a>Implementazione di IMFTopologyServiceLookupClient

Il mixer deve implementare [**l'interfaccia IMFTopologyServiceLookupClient.**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) Prima dell'inizio del flusso, EVR chiama [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e passa un puntatore [**all'interfaccia IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) di EVR. Il mixer usa questo puntatore per ottenere i puntatori a interfaccia da EVR.

Come minimo, il mixer deve eseguire una query per l'interfaccia seguente:

-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Quando EVR chiama [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers), il mixer deve rilasciare tutti i puntatori ottenuti dalla chiamata [**a InitServicePointers.**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)

## <a name="mixer-attributes"></a>Mixer Attributi

Un mixer deve supportare gli attributi seguenti.



| Attributo                                                                        | Descrizione                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md)                          | Specifica se il mixer supporta l'accelerazione video DirectX (DXVA).                                                                                                                                                                               |
| [**MF \_ SA \_ REQUIRED \_ SAMPLE \_ COUNT**](mf-sa-required-sample-count-attribute.md) | Numero di campioni video che l'EVR deve allocare per ogni flusso mixer. Questo attributo si applica ai singoli flussi. usare l'archivio attributi restituito [**da IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes). |



 

## <a name="setting-the-mixer-on-the-evr"></a>Impostazione del Mixer nell'EVR

Per impostare un mixer personalizzato in EVR, chiamare [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer). Sia il DirectShow EVR che il sink dei supporti EVR implementano questo metodo.

**Oggetto di attivazione EVR.** Se si usa l'oggetto attivazione EVR, è possibile fornire un mixer personalizzato impostando uno degli attributi seguenti nell'oggetto attivazione EVR:



| Attributo                                                                                                 | Descrizione                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ ACTIVATE**](mf-activate-custom-video-mixer-activate-attribute.md) | Puntatore a un oggetto attivazione per il mixer. L'oggetto attivazione deve implementare [**l'interfaccia IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID del mixer.                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video avanzato](enhanced-video-renderer.md)
</dt> </dl>

 

 
