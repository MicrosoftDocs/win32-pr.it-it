---
description: Buffer della superficie DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Buffer della superficie DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127903"
---
# <a name="directx-surface-buffer"></a>Buffer della superficie DirectX

L'oggetto buffer della superficie DirectX è un buffer multimediale che gestisce una superficie Direct3D. Per creare un'istanza di questo oggetto, chiamare [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) e passare un puntatore alla superficie DirectX. Il buffer di superficie DirectX espone le interfacce seguenti:

-   [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Sono disponibili diversi modi per accedere alla memoria della superficie dall'oggetto buffer:

-   Consigliato: chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nel buffer. Usare il **\_ \_ servizio buffer** di identificazione del servizio. Il metodo restituisce un puntatore alla superficie Direct3D sottostante.
-   Chiamare [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d). Questo metodo chiama **IDirect3DSurface9:: LockRect** direttamente sulla superficie. Il metodo [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) chiama **UnlockRect** sulla superficie.
-   Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). In genere questa operazione non è consigliata, perché impone all'oggetto di copiare la memoria dall'area Direct3D e quindi di nuovo. Il metodo [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) è più efficiente.

Sia [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) che [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) possono avere esito negativo se la superficie sottostante non è bloccabile. Il buffer di superficie DirectX implementa questi due metodi principalmente per i componenti che non sono progettati per funzionare con le superfici Direct3D.

Il renderer video avanzato (EVR) crea buffer della superficie DirectX quando il decodificatore non è configurato per l'accelerazione video DirectX (DXVA). Per ulteriori informazioni, vedere [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).

### <a name="obtaining-the-direct3d-surface"></a>Recupero della superficie Direct3D

Per ottenere una superficie Direct3D da un esempio video, eseguire le operazioni seguenti:

1.  Chiamare [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) con un valore di indice pari a zero.
2.  Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e specificare l'identificatore del servizio del **\_ \_ servizio di buffer** .

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

 

 



