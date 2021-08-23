---
description: DirectX Surface Buffer
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: DirectX Surface Buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cff1489a644fd5c4144c8c0d923f11e5ca4555886e8defbce3b9b26a16a35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828271"
---
# <a name="directx-surface-buffer"></a>DirectX Surface Buffer

L'oggetto surface buffer DirectX è un buffer multimediale che gestisce una superficie Direct3D. Per creare un'istanza di questo oggetto, chiamare [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) e passare un puntatore alla superficie DirectX. Il surface buffer DirectX espone le interfacce seguenti:

-   [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Esistono diversi modi per accedere alla memoria di superficie dall'oggetto buffer:

-   Consigliato: chiamare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nel buffer. Usare l'identificatore di **servizio MR \_ BUFFER \_ SERVICE**. Il metodo restituisce un puntatore alla superficie Direct3D sottostante.
-   Chiamare [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d). Questo metodo chiama **IDirect3DSurface9::LockRect** direttamente sulla superficie. Il [**metodo IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) chiama **UnlockRect** sulla superficie.
-   Chiamare [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). In genere questa operazione non è consigliata, perché impone all'oggetto di copiare la memoria dalla superficie Direct3D e quindi di nuovo. Il [**metodo Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) è più efficiente.

Sia [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) che [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) possono avere esito negativo se la superficie sottostante non è bloccabile. Il buffer di superficie DirectX implementa questi due metodi principalmente per i componenti che non sono progettati per funzionare con le superfici Direct3D.

Il renderer video avanzato (EVR) crea buffer di superficie DirectX quando il decodificatore non è configurato per l'accelerazione video DirectX (DXVA). Per altre informazioni, vedere [**IMFVideoSampleAllocator.**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)

### <a name="obtaining-the-direct3d-surface"></a>Recupero della superficie Direct3D

Per ottenere una superficie Direct3D da un esempio video, seguire questa procedura:

1.  Chiamare [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) con un valore di indice pari a zero.
2.  Chiamare [**MFGetService e**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) specificare l'identificatore **del servizio BUFFER \_ \_ SERVICE MR.**

Il codice seguente illustra questi passaggi:


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer multimediali](media-buffers.md)
</dt> <dt>

[Esempi video](video-samples.md)
</dt> </dl>

 

 



