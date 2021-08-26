---
description: Interfacce del servizio
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Interfacce del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d99155eb5cfb8c435281a5f23567759931cc53fae3743d9c76ce7be75f68c380
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060413"
---
# <a name="service-interfaces"></a>Interfacce del servizio

Alcune interfacce in Media Foundation devono essere ottenute chiamando [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) anziché **chiamando QueryInterface**. Il [**metodo GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) funziona come QueryInterface, ma con le differenze seguenti:

-   Accetta un GUID dell'identificatore di servizio oltre all'identificatore di interfaccia.
-   Può restituire un puntatore a un altro oggetto che implementa l'interfaccia , anziché restituire un puntatore all'oggetto originale su cui viene eseguita una query.

> [!Note]  
> [**L'interfaccia IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) è molto simile all'interfaccia **IServiceProvider** usata in altre API.

 

Un *servizio* è una particolare interfaccia ottenuta da una particolare classe di oggetti tramite [**l'interfaccia IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) Vengono definiti i servizi seguenti.



| Identificatore del servizio                          | Interfaccia                                                                                                                                | Oggetti che potrebbero esporre questo servizio                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| SERVIZIO DEL \_ PROVIDER DI \_ METADATI MF \_             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Origini multimediali                                                                                                                                     |
| SERVIZIO \_ MF \_ MEDIASOURCE                    | [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Supportato in Windows 8.1 e versioni successive.<br/>                                                                                                    |
| CONTESTO DEL \_ SERVER MF PMP \_ \_                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | Sessione multimediale PMP (Protected Media Path).                                                                                                         |
| MF \_ QUALITY \_ SERVICES                       | [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Origini multimediali.                                                                                                                                    |
| SERVIZIO DI \_ CONTROLLO DELLA \_ FREQUENZA \_ MF                  | [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Origini multimediali, sessione multimediale                                                                                                                      |
| SERVIZIO DI \_ CONTROLLO DELLA \_ FREQUENZA \_ MF                  | [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Origini multimediali, sink multimediali, sessione multimediale                                                                                                         |
| PROXY \_ REMOTO MF \_                           | [**IMFRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Proxy per oggetti remoti.                                                                                                                       |
| SERVIZIO \_ SAMI MF \_                           | [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Origine multimediale SAMI (Accessible Media Interchange) sincronizzata.                                                                                    |
| SERVIZIO PROVIDER DI \_ PRESENTAZIONE \_ DI \_ ORIGINE \_ MF | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Origine Sequencer                                                                                                                                  |
| SERVIZIO \_ TIMECODE MF \_                       | [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | Origine multimediale ASF.                                                                                                                                 |
| MF \_ TOPONODE \_ ATTRIBUTE \_ EDITOR \_ SERVICE    | [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Sessione multimediale                                                                                                                                     |
| OGGETTO DI CUI È STATO ESEGUITO IL WRAPPING MF \_ \_                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Oggetti di cui è stato eseguito il wrapping                                                                                                                                   |
| SERVIZIO BUFFER DI CUI È STATO ESEGUITO \_ \_ IL WRAPPING MF \_                |                                                                                                                                          | Supportato in Windows 8.1 e versioni successive.<br/>                                                                                                    |
| MF \_ WRAPPED \_ SAMPLE \_ SERVIC                 |                                                                                                                                          | Supportato in Windows 8.1 e versioni successive.<br/>                                                                                                    |
| MF \_ WORKQUEUE \_ SERVICES                     | [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Sessione multimediale                                                                                                                                     |
| SERVIZIO MFNET \_ \_ SAVEJOB                     | [**IMFSaveJob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Flussi di byte                                                                                                                                      |
| SERVIZIO STATISTICHE \_ MFNETSOURCE \_            | **Ipropertystore**                                                                                                                       | Origine di rete. Usare questo servizio per recuperare le statistiche di rete. Vedere [**Proprietà MFNETSOURCE \_ STATISTICS**](mfnetsource-statistics-property.md). |
| SERVIZIO \_ CRITERI AUDIO \_ \_ MR                  | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Renderer audio                                                                                                                                    |
| SERVIZIO \_ BUFFER \_ MR                         | **IDirect3DSurface9**                                                                                                                    | Buffer di superficie DirectX                                                                                                                           |
| SERVIZIO \_ VOLUME CRITERI DI ACQUISIZIONE \_ \_ \_ MR        | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Origine di acquisizione audio                                                                                                                              |
| MR \_ POLICY \_ VOLUME \_ SERVICE                 | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Renderer audio                                                                                                                                    |
| MR \_ STREAM \_ VOLUME \_ SERVICE                 | [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Renderer audio                                                                                                                                    |
| SERVIZIO \_ DI ACCELERAZIONE VIDEO \_ \_ MR            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Renderer video migliorato (EVR)                                                                                                                     |
| SERVIZIO \_ DI ACCELERAZIONE VIDEO \_ \_ MR            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Pin di input sul DirectShow EVR                                                                                                           |
| SERVIZIO \_ DI ACCELERAZIONE VIDEO \_ \_ MR            | [**Interfaccia IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | Sink di flusso EVR.                                                                                                                                 |
| SERVIZIO \_ MR VIDEO \_ \_ MIXER                   | Varie interfacce esposte dal mixer EVR. Vedere [Uso dei controlli Mixer video.](using-the-video-mixer-controls.md)                   | Evr                                                                                                                                               |
| SERVIZIO \_ RENDERING VIDEO \_ \_ MR                  | Varie interfacce esposte dal presentatore EVR. Vedere [Uso dei controlli di visualizzazione video.](using-the-video-display-controls.md)           | Evr                                                                                                                                               |



 

È necessario usare [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere le interfacce elencate in questa tabella dagli oggetti elencati in questa tabella.

In alcuni casi, un'interfaccia viene restituita come servizio da una classe di oggetti e restituita tramite **QueryInterface** da un'altra classe di oggetti. Le pagine di riferimento per ogni interfaccia indicano quando usare [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) e quando usare **QueryInterface.**

> [!Caution]  
> Un oggetto può essere implementato in modo che restituisca un'interfaccia del servizio tramite **QueryInterface** e [**GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Tuttavia, **l'uso di QueryInterface** quando **è necessario GetService** potrebbe causare problemi di compatibilità in un secondo momento.

 

La [**funzione MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) è una funzione helper che esegue una query su un oggetto [**per IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e quindi chiama il metodo [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) dell'oggetto.

## <a name="examples"></a>Esempio

L'esempio seguente esegue una query sulla sessione multimediale [**per IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e ottiene [**l'interfaccia IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)


```C++
IMFGetService *pGetService = NULL;
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = pMediaSession->QueryInterface(
    IID_IMFGetService, 
    (void**)&pGetService);

if (SUCCEEDED(hr))
{
    hr = pGetService->GetService(
        MF_RATE_CONTROL_SERVICE, 
        IID_IMFRateControl,
        (void**)&pRateControl);
}
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_REELEASE(pGetService);
SAFE_RELEASE(pRateControl);
```



L'esempio seguente è equivalente all'esempio precedente, ma usa la [**funzione MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)


```C++
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = MFGetService(
    pMediaSession, 
    MF_RATE_CONTROL_SERVICE, 
    IID_IMFRateControl, 
    (void**) &pRateCtl 
); 
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_RELEASE(pRateControl);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[API Media Foundation platform](media-foundation-platform-apis.md)
</dt> </dl>

 

 




