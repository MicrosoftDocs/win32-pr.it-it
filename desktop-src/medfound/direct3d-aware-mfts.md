---
description: Questo argomento descrive come implementare una trasformazione Media Foundation direct3D per i video.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae3bc071ee707505fd7412cba6f0a5aa397fd4c3f623225da28cc5490bf3323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958739"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware MFT

Questo argomento descrive come implementare una trasformazione Media Foundation *direct3D* per i video.

Un video MFT è considerato *in grado di riconoscere Direct3D* se è in grado di elaborare campioni che contengono superfici Direct3D. Il motivo tipico per il supporto di Direct3D in un video MFT è l'abilitazione della decodifica con accelerazione hardware, usando DirectX Video Acceleration (DXVA).

In questo argomento vengono descritti i passaggi necessari per rendere il dispositivo MFT in grado di riconoscere Direct3D. Questo argomento non illustra i meccanismi della decodifica DXVA. Per informazioni su DXVA, vedere [Accelerazione video DirectX 2.0.](directx-video-acceleration-2-0.md)

> [!IMPORTANT]
> A partire Windows 8, è possibile usare [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) anziché [**IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) Per Windows store, è necessario usare **IMFDXGIDeviceManager** e Microsoft Direct3D 11. Per altre informazioni, vedere le API [Direct3D 11 Video.](direct3d-11-video-apis.md)

 

1.  Implementare [**il metodo IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Questo metodo restituisce un puntatore a un archivio di attributi.
2.  MFT deve impostare il valore dell'attributo [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) su **TRUE** nel proprio archivio attributi. A partire Windows 8, se si usa Direct3D 11 usare [MF \_ SA \_ D3D11 \_ AWARE.](mf-sa-d3d11-aware.md)
3.  Durante la negoziazione del formato, se l'attributo [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) (o [MF \_ SA \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) se si usa Direct3D 11) è **TRUE,** il client può inviare il messaggio [**MFT MESSAGE SET \_ \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) a MFT. Il *parametro di evento ulParam* è un puntatore [**all'interfaccia IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) A partire Windows 8, è possibile usare [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) anziché **IDirect3DDeviceManager9.** Il client non deve inviare questo messaggio.
4.  MFT chiama [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) per eseguire una query per il servizio DXVA necessario. A partire Windows 8, se È stato usato [**IMFDXGIDeviceManager,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) MFT chiama [**IMFDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). In genere un decodificatore esegue una query per [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)e un processore video esegue una query per [**IDirectXVideoProcessorService.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
5.  Supponendo che il passaggio precedente abbia esito positivo, i metodi [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) e [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) devono restituire formati compatibili con DXVA.
6.  Il client configura i tipi di supporti in MFT. Se un tipo di supporto non è compatibile con DXVA, MFT deve restituire il codice di errore **MF \_ E \_ UNSUPPORTED \_ D3D \_ TYPE**.
7.  A questo punto, sono disponibili due opzioni, a seconda che il client trovi un formato DXVA appropriato.
    -   Se il client configura correttamente un formato DXVA, potrebbe iniziare l'elaborazione. A questo punto, MFT può usare DXVA per l'elaborazione o eseguire il fall back all'elaborazione software.
    -   In alternativa, se il client non trova un formato DXVA accettabile, il client può inviare un altro messaggio [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER,**](mft-message-set-d3d-manager.md) questa volta impostando *ulParam* su **NULL.** MFT deve rilasciare il puntatore [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) (il puntatore [**IMFDXGIDeviceManager,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) se è stato usato **IMFDXGIDeviceManager)** e qualsiasi altra interfaccia DXVA e ripristinare l'elaborazione software. A questo punto, MFT non deve usare l'elaborazione DXVA.

È necessario preparare un MFT che sia in grado di riconoscere Direct3D per gestire campioni che contengono una superficie Direct3D. L'esempio conterrà esattamente un buffer multimediale. Per ottenere la superficie Direct3D dal buffer, chiamare la [**funzione MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e specificare il **servizio BUFFER \_ \_ MR.** Per altre informazioni, vedere [DirectX Surface Buffer.](directx-surface-buffer.md)

Un MFT che usa DXVA deve allocare i propri campioni di output, come indicato di seguito:

1.  Nel metodo [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) impostare il flag **MFT \_ OUTPUT STREAM \_ PROVIDES \_ \_ SAMPLES.**
2.  Creare un pool di superfici DXVA, come descritto nella specifica DXVA.
3.  Creare esempi multimediali chiamando [**MFCreateVideoSampleFromSurface.**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface)

MFT deve sempre supportare l'elaborazione software come fallback, perché l'elaborazione DXVA potrebbe non essere disponibile per diversi motivi:

-   La GPU potrebbe non supportare DXVA.
-   Il client potrebbe non usare Direct3D.
-   I profili DXVA non sono definiti per ogni formato video.

Un MFT che è in grado di riconoscere Direct3D deve avere un singolo flusso di output. Non può avere più output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



