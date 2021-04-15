---
description: In questo argomento viene descritto come implementare una trasformazione di Media Foundation compatibile con Direct3D (MFT) per i video.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad50438250c0ee1627cc20aebb49262ec8eec9ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524561"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware MFTs

In questo argomento viene descritto come implementare una trasformazione di Media Foundation *compatibile con Direct3D* (MFT) per i video.

Un video MFT viene considerato *compatibile con Direct3D* se può elaborare esempi che contengono superfici Direct3D. Il motivo tipico per il supporto di Direct3D in un video MFT consiste nell'abilitare la decodifica con accelerazione hardware, usando l'accelerazione video DirectX (DXVA).

In questo argomento vengono descritti i passaggi necessari per rendere compatibile con Direct3D. Questo argomento non copre i meccanismi di decodifica DXVA. Per informazioni su DXVA, vedere [accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md).

> [!IMPORTANT]
> A partire da Windows 8, è possibile usare [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) invece di [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). Per le app di Windows Store, è necessario usare **IMFDXGIDeviceManager** e Microsoft Direct3D 11. Per altre informazioni, vedere le [API video di Direct3D 11](direct3d-11-video-apis.md).

 

1.  Implementare il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Questo metodo restituisce un puntatore a un archivio di attributi.
2.  Il file MFT deve impostare il valore dell'attributo in grado di riconoscere il valore [**MF \_ sa \_ D3D \_**](mf-sa-d3d-aware-attribute.md) su **true** nel relativo archivio attributi. A partire da Windows 8, se si usa Direct3D 11 usare [MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md).
3.  Durante la negoziazione del formato, se l'attributo per la compatibilità con la compatibilità con l'utilizzo di Direct3D [**\_ sa \_ \_**](mf-sa-d3d-aware-attribute.md) o [MF \_ sa \_ d3d11 \_](mf-sa-d3d11-aware.md) è **true**, il client può inviare il messaggio [**MFT \_ message \_ set \_ \_ gestione D3D**](mft-message-set-d3d-manager.md) alla MFT. Il parametro dell'evento *ulParam* è un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . A partire da Windows 8, è possibile usare [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) anziché **IDirect3DDeviceManager9**. Il client non è necessario per l'invio di questo messaggio.
4.  Il MFT chiama [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) per eseguire una query per il servizio DXVA necessario. A partire da Windows 8, se è stato usato [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) , il MFT chiama [**IMFDXGIDeviceManager:: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). In genere, un decodificatore esegue una query per [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)e un processore video esegue una query per [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice).
5.  Supponendo che il passaggio precedente abbia esito positivo, i metodi [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) e [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) devono restituire formati compatibili con DXVA.
6.  Il client configura i tipi di supporto in MFT. Se un tipo di supporto non è compatibile con DXVA, MFT deve restituire il codice di errore **MF \_ E il \_ \_ \_ tipo D3D non supportato**.
7.  A questo punto, sono disponibili due opzioni, a seconda che il client trovi un formato DXVA appropriato.
    -   Se il client configura correttamente un formato DXVA, può iniziare l'elaborazione. A questo punto, la MFT può usare DXVA per l'elaborazione o eseguire il fallback all'elaborazione software.
    -   In alternativa, se il client non trova un formato DXVA accettabile, il client può inviare un altro messaggio di [**\_ \_ \_ \_ gestione D3D del set di messaggi MFT**](mft-message-set-d3d-manager.md) , questa volta impostando *ulParam* su **null**. Il MFT deve rilasciare il puntatore [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) (il puntatore [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) se è stato usato **IMFDXGIDeviceManager** ) e qualsiasi altra interfaccia DXVA e ripristinare l'elaborazione del software. A questo punto, il MFT non deve usare l'elaborazione DXVA.

Un MFT compatibile con Direct3D deve essere preparato per gestire esempi che contengono una superficie Direct3D. L'esempio conterrà esattamente un buffer multimediale. Per ottenere la superficie Direct3D dal buffer, chiamare la funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e specificare il servizio **del \_ \_ servizio buffer di Mr** . Per ulteriori informazioni, vedere la pagina relativa al [buffer della superficie DirectX](directx-surface-buffer.md).

Un MFT che usa DXVA deve allocare i propri esempi di output, come indicato di seguito:

1.  Nel metodo [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) impostare il flusso di **output di MFT fornisce il flag \_ \_ \_ \_ Samples** .
2.  Creare un pool di superfici DXVA, come descritto nella specifica DXVA.
3.  Creare esempi di supporti chiamando [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface).

La MFT deve sempre supportare l'elaborazione software come fallback, perché l'elaborazione del DXVA potrebbe non essere disponibile, per diversi motivi:

-   La GPU potrebbe non supportare DXVA.
-   Il client potrebbe non usare Direct3D.
-   I profili DXVA non sono definiti per ogni formato video.

Un MFT compatibile con Direct3D deve avere un singolo flusso di output. Non può avere più output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



