---
description: Interfacce del servizio
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Interfacce del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31687cc1c1283eb59c7731743eaf4ece0127b392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309002"
---
# <a name="service-interfaces"></a>Interfacce del servizio

Alcune interfacce in Media Foundation devono essere ottenute chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) anziché chiamando **QueryInterface**. Il metodo [**GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) funziona come QueryInterface, ma con le differenze seguenti:

-   Accetta un GUID identificatore del servizio oltre all'identificatore di interfaccia.
-   Può restituire un puntatore a un altro oggetto che implementa l'interfaccia, anziché restituire un puntatore all'oggetto originale su cui viene eseguita una query.

> [!Note]  
> L'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) è molto simile all'interfaccia **IServiceProvider** utilizzata in altre API.

 

Un *servizio* è una particolare interfaccia ottenuta da una particolare classe di oggetti tramite l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Sono definiti i servizi seguenti.



| Identificatore servizio                          | Interfaccia                                                                                                                                | Oggetti che potrebbero esporre questo servizio                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ servizio provider di metadati MF \_             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Origini supporti                                                                                                                                     |
| servizio di MF \_ MEDIASOURCE \_                    | [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Supportato in Windows 8.1 e versioni successive.<br/>                                                                                                    |
| \_ \_ contesto server MF \_ PMP                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | Sessione multimediale del percorso multimediale protetto (PMP).                                                                                                         |
| \_servizi di qualità MF \_                       | [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Origini multimediali.                                                                                                                                    |
| \_servizio di \_ controllo della velocità MF \_                  | [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Origini supporti, sessione multimediale                                                                                                                      |
| \_servizio di \_ controllo della velocità MF \_                  | [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Origini supporti, sink multimediali, sessione multimediale                                                                                                         |
| \_proxy remoto \_ MF                           | [**IMFRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Proxy per gli oggetti remoti.                                                                                                                       |
| \_servizio MF Sami \_                           | [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Origine multimediale SAMI (Synchronized Accessible Media Interchange).                                                                                    |
| \_servizio del \_ provider di presentazione di origine MF \_ \_ | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Origine sequencer                                                                                                                                  |
| \_servizio timecode \_ MF                       | [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | Origine dei supporti ASF.                                                                                                                                 |
| \_ \_ \_ servizio Editor attributi MF \_ TOPONODE    | [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Sessione multimediale                                                                                                                                     |
| \_oggetto con incapsulamento MF \_                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Oggetti con wrapper                                                                                                                                   |
| \_servizio buffer con incapsulamento MF \_ \_                |                                                                                                                                          | Supportato in Windows 8.1 e versioni successive.<br/>                                                                                                    |
| \_manutenzione di esempio con incapsulamento MF \_ \_                 |                                                                                                                                          | Supportato in Windows 8.1 e versioni successive.<br/>                                                                                                    |
| \_Servizi WORKQUEUE \_ MF                     | [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Sessione multimediale                                                                                                                                     |
| \_servizio MFNET SAVEJOB \_                     | [**IMFSaveJob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Flussi di byte                                                                                                                                      |
| \_servizio statistiche \_ MFNETSOURCE            | **IPropertyStore**                                                                                                                       | Origine di rete. Utilizzare questo servizio per recuperare le statistiche di rete. Vedere [**MFNETSOURCE \_ Statistics Property**](mfnetsource-statistics-property.md). |
| \_ \_ servizio criteri audio di Mr \_                  | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Renderer audio                                                                                                                                    |
| \_servizio buffer \_ Mr                         | **IDirect3DSurface9**                                                                                                                    | Buffer della superficie DirectX                                                                                                                           |
| \_ \_ servizio volume di criteri di acquisizione di \_ Mr \_        | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Origine acquisizione audio                                                                                                                              |
| \_servizio del \_ volume di criteri di Mr \_                 | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Renderer audio                                                                                                                                    |
| \_ \_ servizio volume di flusso di Mr \_                 | [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Renderer audio                                                                                                                                    |
| \_ \_ servizio accelerazione video di Mr \_            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Renderer video migliorato (EVR)                                                                                                                     |
| \_ \_ servizio accelerazione video di Mr \_            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Pin di input nel filtro EVR DirectShow                                                                                                           |
| \_ \_ servizio accelerazione video di Mr \_            | [**Interfaccia IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | Sink di flusso EVR.                                                                                                                                 |
| \_ \_ servizio mixer video di Mr \_                   | Varie interfacce esposte dal mixer EVR. Vedere [uso dei controlli mixer video](using-the-video-mixer-controls.md).                   | EVR                                                                                                                                               |
| \_servizio di \_ rendering \_ video di Mr                  | Varie interfacce esposte da EVR Presenter. Vedere [uso dei controlli video display](using-the-video-display-controls.md).           | EVR                                                                                                                                               |



 

È necessario utilizzare [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere le interfacce elencate in questa tabella dagli oggetti elencati in questa tabella.

In alcuni casi, un'interfaccia viene restituita come servizio da una classe di oggetti e restituita tramite **QueryInterface** da un'altra classe di oggetti. Le pagine di riferimento per ogni interfaccia indicano quando utilizzare [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) e quando utilizzare **QueryInterface**.

> [!Caution]  
> Un oggetto può essere implementato in modo tale che restituisca un'interfaccia del servizio tramite **QueryInterface** e [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Tuttavia, l'utilizzo di **QueryInterface** quando è richiesto **GetService** potrebbe causare problemi di compatibilità in un secondo momento.

 

La funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) è una funzione helper che esegue una query su un oggetto per [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e quindi chiama il metodo [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) dell'oggetto.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene eseguita una query sulla sessione multimediale per [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e viene ottenuta l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .


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



L'esempio seguente è equivalente all'esempio precedente, ma usa la funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) .


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

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 




