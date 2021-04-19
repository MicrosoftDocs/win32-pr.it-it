---
description: Uso del filtro EVR DirectShow
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Uso del filtro EVR DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310173"
---
# <a name="using-the-directshow-evr-filter"></a>Uso del filtro EVR DirectShow

Per creare il filtro EVR (Enhanced video renderer), chiamare **CoCreateInstance**. Il CLSID è CLSID \_ EnhancedVideoRenderer, definito in UUIDs. h. Non è necessario chiamare [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) o [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per usare il filtro EVR.

Per altre informazioni sull'uso del filtro EVR in un'applicazione DirectShow, vedere [riproduzione audio/video in DirectShow](../directshow/audio-video-playback-in-directshow.md).

Il filtro EVR inizia con un pin di input, che corrisponde al flusso di riferimento. Per aggiungere PIN per i sottoflussi, eseguire una query sul filtro per l'interfaccia [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) e chiamare [**IEVRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Chiamare questo metodo prima di connettere i pin di input. Il pin 0 è sempre il flusso di riferimento. Connettere questo pin prima di qualsiasi altro pin, perché il formato del flusso di riferimento potrebbe limitare i formati dei sottoflussi disponibili.

Prima di avviare il grafo, impostare la finestra ritaglio video e il rettangolo di destinazione. Per altre informazioni, vedere [uso dei controlli video display](using-the-video-display-controls.md).

A differenza del renderer video mixing (VMR), EVR non dispone di modalità operative (finestra, senza finestra e così via). In particolare:

-   EVR non supporta la modalità finestra. L'applicazione deve fornire la finestra di ridimensionamento.
-   Il EVR non dispone di una modalità di rendering. Per sostituire il Presenter predefinito, chiamare [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   Il EVR non dispone di una modalità di combinazione. Il EVR crea sempre il mixer. Se si dispone di un flusso di input, non è necessario chiamare [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) per forzare il EVR a usare il mixer.

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
-   **IPersistStream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **ISpecifyPropertyPages**

## <a name="input-pin-interfaces"></a>Interfacce pin di input

I pin di input nel filtro EVR espongono le interfacce seguenti. Usare **QueryInterface** per recuperare i puntatori a queste interfacce:

-   [**IEVRVideoStreamControl**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**Ipin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

Inoltre, è possibile utilizzare l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) per recuperare l'interfaccia seguente:

-   [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione audio/video in DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> </dl>

 

 
