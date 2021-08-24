---
description: Supporto di DXVA 2.0 in Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Supporto di DXVA 2.0 in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170b9c8ccdbdb7e0844b79e5743c4a84b033b7d504378dba083be5adfb244fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721930"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Supporto di DXVA 2.0 in Media Foundation

Questo argomento descrive come supportare DirectX Video Acceleration (DXVA) 2.0 in una trasformazione Media Foundation (MFT) usando Microsoft Direct3D 9 In particolare, descrive la comunicazione tra il decodificatore e il renderer video, mediato dal caricatore della topologia. Questo argomento non descrive come implementare la decodifica DXVA.

Nella parte restante di questo argomento, il termine *decodificatore* si riferisce al decodificatore MFT, che riceve video compresso e restituisce video non compressi. Il termine *dispositivo decodificatore si* riferisce a un acceleratore video hardware implementato dal driver di grafica.

> [!TIP]
> Per informazioni sulla decodifica video Di Microsoft Direct3D 11, vedere [Supporting Direct3D 11 Video Decoding in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Windows Le app dello Store devono usare Direct3D 11.

 

Ecco i passaggi di base che un decodificatore deve eseguire per supportare DXVA 2.0 in Media Foundation:

1.  Aprire un handle per il dispositivo Direct3D 9.
2.  Trovare una configurazione del decodificatore DXVA.
3.  Allocare buffer non compressi.
4.  Decodificare i fotogrammi.

Questi passaggi sono descritti in modo più dettagliato nella parte restante di questo argomento.

## <a name="opening-a-direct3d-device-handle"></a>Apertura di un handle di dispositivo Direct3D

MFT usa Gestione dispositivi Microsoft Direct3D per ottenere un handle per il dispositivo Direct3D 9. Per aprire l'handle del dispositivo, seguire questa procedura:

1.  Esporre [l'attributo MF \_ SA \_ D3D \_ AWARE](mf-sa-d3d-aware-attribute.md) con il valore **TRUE**. Il caricatore della topologia esegue una query su questo attributo chiamando [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). L'impostazione **dell'attributo** su TRUE notifica al caricatore della topologia che MFT supporta DXVA.
2.  Quando inizia la negoziazione del formato, il caricatore della topologia chiama [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md) Il *parametro ulParam* è un **puntatore IUnknown** al gestore di dispositivi Direct3D del renderer video. Eseguire una query su questo puntatore [**per l'interfaccia IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)
3.  Chiamare [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) per ottenere un handle per il dispositivo Direct3D del renderer.
4.  Chiamare [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) e passare l'handle del dispositivo. Questo metodo restituisce un puntatore [**all'interfaccia IDirectXVideoDecoderService.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)
5.  Memorizzare nella cache i puntatori e l'handle del dispositivo.

## <a name="finding-a-decoder-configuration"></a>Ricerca di una configurazione del decodificatore

MFT deve trovare una configurazione compatibile per il dispositivo decodificatore DXVA. Eseguire i passaggi seguenti all'interno [**del metodo IMFTransform::SetInputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) dopo la convalida del tipo di input:

1.  Chiamare [**IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Questo metodo restituisce una matrice di GUID del dispositivo decodificatore.
2.  Scorrere la matrice di GUID del decodificatore per trovare quelli supportati dal decodificatore. Ad esempio, per un decodificatore MPEG-2, è necessario cercare **DXVA2 \_ ModeMPEG2 \_ MOCOMP,** **DXVA2 \_ ModeMPEG2 \_ IDCT** o **DXVA2 \_ ModeMPEG2 \_ VLD.**

3.  Quando si trova un GUID del dispositivo decodificatore candidato, passare il GUID al metodo [**IDirectXVideoDecoderService::GetDecoderRenderTargets.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) Questo metodo restituisce una matrice di formati di destinazione di rendering, specificati come **valori D3DFORMAT.**
4.  Scorrere i formati di destinazione di rendering e cercare un formato supportato dal decodificatore.
5.  Chiamare [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Passare lo stesso GUID del dispositivo decodificatore, insieme a una struttura [**\_ VideoDesc DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) che descrive il formato di output proposto. Il metodo restituisce una matrice di [**strutture \_ ConfigPictureDecode DXVA2.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) Ogni struttura descrive una possibile configurazione per il dispositivo decodificatore. Cercare una configurazione che il decodificatore supporta.
6.  Archiviare il formato e la configurazione della destinazione di rendering.

Nel metodo [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) restituire un formato video non compresso, in base al formato di destinazione di rendering proposto.

Nel metodo [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) controllare il tipo di supporto rispetto al formato di destinazione di rendering.

### <a name="fallback-to-software-decoding"></a>Fallback alla decodifica software

Se MFT non riesce a trovare una configurazione DXVA (ad esempio, se il driver di grafica non dispone delle funzionalità giuste), deve restituire il codice di errore **MF \_ E \_ UNSUPPORTED \_ D3D \_ TYPE** dai metodi [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) [**e SetOutputType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) Il caricatore della topologia risponde inviando il messaggio [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) con il **valore NULL** per il *parametro ulParam.* MFT deve rilasciare il puntatore [**all'interfaccia IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) Il caricatore della topologia rinegozia il tipo di supporto e MFT può usare la decodifica software.

## <a name="allocating-uncompressed-buffers"></a>Allocazione di buffer non compressi

In DXVA 2.0 il decodificatore è responsabile dell'allocazione delle superfici Direct3D da usare come buffer video non compressi. Il decodificatore deve allocare 3 superfici per l'EVR da usare per la deinterlacing. Questo numero è fisso, perché Media Foundation non consente all'EVR di specificare il numero di superfici richiesto dal driver di grafica per la deinterlacing. Tre superfici devono essere sufficienti per qualsiasi driver.

Nel metodo [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) impostare il flag **MFT \_ OUTPUT STREAM \_ PROVIDES \_ \_ SAMPLES** nella struttura [**MFT OUTPUT STREAM \_ \_ \_ INFO.**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) Questo flag notifica alla sessione multimediale che MFT alloca i propri esempi di output.

Per creare le superfici, chiamare [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface). [**L'interfaccia IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) eredita questo metodo da [**IDirectXVideoAccelerationService.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) È possibile eseguire questa operazione in [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)dopo aver trovato il formato di destinazione del rendering.

Per ogni superficie, chiamare [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) per creare un campione multimediale per contenere la superficie. Il metodo restituisce un puntatore [**all'interfaccia IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="decoding"></a>Decodifica

Per creare il dispositivo decodificatore, chiamare [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). Il metodo restituisce un puntatore [**all'interfaccia IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) del dispositivo decodificatore.

La decodifica deve avvenire all'interno [**del metodo IMFTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) In ogni frame chiamare [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) per testare l'handle del dispositivo. Se il dispositivo è stato modificato, il metodo restituisce **DXVA2 \_ E NEW VIDEO \_ \_ \_ DEVICE**. In questo caso, eseguire le operazioni seguenti:

1.  Chiudere l'handle del dispositivo chiamando [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Rilasciare [**i puntatori IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) e [**IDirectXVideoDecoder.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)
3.  Aprire un nuovo handle di dispositivo.
4.  Negoziare una nuova configurazione del decodificatore, come descritto in "Ricerca di una configurazione del decodificatore" più indietro in questa pagina.
5.  Creare un nuovo dispositivo decodificatore.

Supponendo che l'handle del dispositivo sia valido, il processo di decodifica funziona come segue:

1.  Ottenere una superficie disponibile che non è attualmente in uso. Inizialmente sono disponibili tutte le superfici.
2.  Eseguire una query sull'esempio multimediale per [**l'interfaccia IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)
3.  Chiamare [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) e fornire un puntatore [**all'interfaccia IMFAsyncCallback,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementata dal decodificatore. Quando il renderer video rilascia l'esempio, viene richiamato il callback del decodificatore.
4.  Chiamare [**IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
5.  Eseguire le operazioni seguenti una o più volte:
    1.  Chiamare [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) per ottenere un buffer del decodificatore DXVA.
    2.  Riempire il buffer.
    3.  Chiamare [**IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
    4.  Chiamare [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) per eseguire le operazioni di decodifica sul frame.

DXVA 2.0 usa le stesse strutture di dati di DXVA 1.0 per le operazioni di decodifica. Per il set originale di profili DXVA (per H.261, H.263 e MPEG-2), queste strutture di dati sono descritte nella [specifica DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

All'interno di ogni coppia di chiamate [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)Execute, è possibile chiamare GetBuffer più volte, ma una sola / [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) volta per ogni tipo di buffer DXVA. [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) Se si chiama due volte con lo stesso tipo di buffer, i dati verranno sovrascritti.

Usare il callback del [**metodo SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (passaggio 3) per tenere traccia degli esempi attualmente disponibili e degli esempi in uso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 
