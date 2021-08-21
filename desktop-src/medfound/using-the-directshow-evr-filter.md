---
description: Uso del DirectShow EVR
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Uso del DirectShow EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc454b6d298546afdbb5a06b7081505d9ddd7c2ab87a816e79bdb13836e9a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737314"
---
# <a name="using-the-directshow-evr-filter"></a>Uso del DirectShow EVR

Per creare il filtro EVR (Enhanced Video Renderer), chiamare **CoCreateInstance.** Il CLSID è CLSID \_ EnhancedVideoRenderer, definito in uuids.h. Non è necessario chiamare [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) o [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per usare il filtro EVR.

Per altre informazioni sull'uso del filtro EVR in un'applicazione DirectShow, vedere [Riproduzione audio/video in DirectShow](../directshow/audio-video-playback-in-directshow.md).

Il filtro EVR inizia con un pin di input, che corrisponde al flusso di riferimento. Per aggiungere pin per i sottostream, eseguire una query sul filtro per [**l'interfaccia IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) e chiamare [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Chiamare questo metodo prima di connettere eventuali pin di input. Il pin 0 è sempre il flusso di riferimento. Connessione questo pin prima di qualsiasi altro pin, perché il formato del flusso di riferimento potrebbe limitare i formati di flusso secondari disponibili.

Prima di avviare il grafico, impostare la finestra di ritaglio del video e il rettangolo di destinazione. Per altre informazioni, vedere [Uso dei controlli di visualizzazione video.](using-the-video-display-controls.md)

A differenza del renderer di combinazione di video (VMR), EVR non dispone di modalità operative (finestra, senza finestra e così via). In particolare:

-   EVR non supporta la modalità finestra. L'applicazione deve fornire la finestra di ritaglio.
-   EVR non ha una modalità senza rendering. Per sostituire il presentatore predefinito, chiamare [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   EVR non ha una modalità di combinazione. EVR crea sempre il mixer. Se è disponibile un flusso di input, non è necessario chiamare [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) per forzare l'uso del mixer da parte di EVR.

## <a name="filter-interfaces"></a>Interfacce di filtro

Il filtro EVR espone le interfacce seguenti. Alcune di queste interfacce sono documentate in DirectShow SDK. Usare **QueryInterface** per recuperare i puntatori a queste interfacce:

-   [**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)
-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **Ipersiststream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **ISpecifyPropertyPages**

## <a name="input-pin-interfaces"></a>Interfacce pin di input

I pin di input nel filtro EVR espongono le interfacce seguenti. Usare **QueryInterface** per recuperare i puntatori a queste interfacce:

-   [**IEVRVideoStreamControl**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

È anche possibile usare [**l'interfaccia IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) per recuperare l'interfaccia seguente:

-   [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione audio/video in DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Renderer video avanzato](enhanced-video-renderer.md)
</dt> </dl>

 

 
