---
description: Esempi video
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Esempi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3883b3a62cd907c89dd46d14681e28ad9a4d4d94653a9f04a9097707d22cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972600"
---
# <a name="video-samples"></a>Esempi video

L'oggetto di esempio video è un'implementazione specializzata [**dell'interfaccia IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) da usare con [enhanced video renderer](enhanced-video-renderer.md) (EVR). Per creare un'istanza di questo oggetto, chiamare la [**funzione MFCreateVideoSampleFromSurface.**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) La funzione accetta un puntatore a una superficie Direct3D e restituisce un puntatore **all'interfaccia IMFSample.** I tipi di oggetti seguenti devono allocare esempi usando questa funzione:

-   Relatori EVR personalizzati. Un presentatore alloca esempi video e li invia al metodo [**IMFTransform::P rocessOutput del mixer.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Per altre informazioni, vedere [How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).

-   Decodificatori video che supportano l'accelerazione video. Per altre informazioni, vedere [Supporto di DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

L'oggetto di esempio video implementa le interfacce seguenti:

-   [**Esempio IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Se il *parametro pUnkSurface* di [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) è diverso da **NULL,** l'esempio video risultante contiene un singolo buffer multimediale che incapsula la superficie Direct3D. Questo oggetto buffer ha funzionalità limitate:

-   Il metodo [**IMFMediaBuffer::Lock del**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) buffer restituisce E \_ NOTIMPL.

-   Il buffer non implementa [**l'interfaccia IMF2DBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)

L'unico modo per accedere alla superficie dal buffer è chiamare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)usando l'identificatore di servizio MR \_ BUFFER \_ SERVICE.

Se il *parametro pUnkSurface* è **NULL,** l'esempio video viene creato con zero buffer multimediali. Per aggiungere un buffer all'esempio, eseguire le operazioni seguenti:

1.  Creare una superficie Direct3D.

2.  Creare un surface buffer chiamando [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer). Per altre informazioni, vedere [DirectX Surface Buffer.](directx-surface-buffer.md)

3.  Aggiungere il buffer all'esempio chiamando [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Usare questo approccio se è necessario che la memoria di superficie sia accessibile tramite [**l'interfaccia IMF2DBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer multimediali](media-buffers.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 
