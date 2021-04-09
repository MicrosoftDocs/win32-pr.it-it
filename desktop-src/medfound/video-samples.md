---
description: Esempi video
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Esempi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880569"
---
# <a name="video-samples"></a>Esempi video

L'oggetto di esempio video è un'implementazione specializzata dell'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) per l'uso con il [renderer video avanzato](enhanced-video-renderer.md) (EVR). Per creare un'istanza di questo oggetto, chiamare la funzione [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) . La funzione accetta un puntatore a una superficie Direct3D e restituisce un puntatore all'interfaccia **IMFSample** . I tipi di oggetti seguenti devono allocare esempi utilizzando questa funzione:

-   Presenter EVR personalizzati. Un presentatore alloca gli esempi video e li invia al metodo [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer. Per altre informazioni, vedere [How to write an EVR Presenter](how-to-write-an-evr-presenter.md).

-   Decodificatori video che supportano l'accelerazione video. Per ulteriori informazioni, vedere [supporto di DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

L'oggetto di esempio video implementa le interfacce seguenti:

-   [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Se il parametro *pUnkSurface* di [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) è diverso da **null**, l'esempio video risultante contiene un singolo buffer multimediale che incapsula la superficie Direct3D. Questo oggetto buffer ha funzionalità limitate:

-   Il metodo [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) del buffer restituisce E \_ NOTIMPL.

-   Il buffer non implementa l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .

L'unico modo per accedere alla superficie dal buffer consiste nel chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), usando il servizio buffer di identificazione del servizio \_ \_ .

Se il parametro *pUnkSurface* è **null**, l'esempio video viene creato con zero buffer multimediali. Per aggiungere un buffer all'esempio, eseguire le operazioni seguenti:

1.  Creare una superficie Direct3D.

2.  Creare un buffer di superficie chiamando [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer). Per ulteriori informazioni, vedere la pagina relativa al [buffer della superficie DirectX](directx-surface-buffer.md).

3.  Aggiungere il buffer all'esempio chiamando [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Utilizzare questo approccio se è necessario che la memoria della superficie sia accessibile tramite l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer multimediali](media-buffers.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 
