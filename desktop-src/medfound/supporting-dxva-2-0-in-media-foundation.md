---
description: Supporto di DXVA 2,0 in Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Supporto di DXVA 2,0 in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce144c24a1aeeda6281ddb423757f3e339903440
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320700"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Supporto di DXVA 2,0 in Media Foundation

In questo argomento viene descritto come supportare l'accelerazione video DirectX (DXVA) 2,0 in una trasformazione Media Foundation (MFT) utilizzando Microsoft Direct3D 9 in modo specifico, viene descritta la comunicazione tra il decodificatore e il renderer video, che viene mediato dal caricatore della topologia. In questo argomento non viene descritto come implementare la decodifica DXVA.

Nella parte restante di questo argomento, il termine *decodificatore* si riferisce al decodificatore MFT, che riceve video compresso e genera video non compressi. Il termine *dispositivo decodificatore* si riferisce a un acceleratore video hardware implementato dal driver Graphics.

> [!TIP]
> Per informazioni sulla decodifica video Microsoft Direct3D 11, vedere [supporto della decodifica video Direct3D 11 in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Le app di Windows Store devono usare Direct3D 11.

 

Ecco i passaggi di base che devono essere eseguiti da un decodificatore per supportare DXVA 2,0 in Media Foundation:

1.  Aprire un handle per il dispositivo Direct3D 9.
2.  Trovare una configurazione del decodificatore DXVA.
3.  Allocare buffer non compressi.
4.  Decodificare i frame.

Questi passaggi sono descritti in modo più dettagliato nella parte restante di questo argomento.

## <a name="opening-a-direct3d-device-handle"></a>Apertura di un handle di dispositivo Direct3D

Il MFT USA gestione dispositivi Microsoft Direct3D per ottenere un handle per il dispositivo Direct3D 9. Per aprire l'handle del dispositivo, seguire questa procedura:

1.  Esporre l'attributo in grado di riconoscere il valore [MF \_ sa \_ D3D \_](mf-sa-d3d-aware-attribute.md) con il valore **true**. Il caricatore della topologia esegue una query su questo attributo chiamando [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Se si imposta l'attributo su **true** , viene inviata una notifica al caricatore della topologia supportata da DXVA.
2.  Quando viene avviata la negoziazione del formato, il caricatore della topologia chiama [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio di [**\_ \_ \_ \_ gestione D3D del set di messaggi di MFT**](mft-message-set-d3d-manager.md) . Il parametro *ulParam* è un puntatore **IUnknown** alla gestione dispositivi Direct3D del renderer video. Eseguire una query su questo puntatore per l'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Chiamare [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) per ottenere un handle per il dispositivo Direct3D del renderer.
4.  Chiamare [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) e passare l'handle del dispositivo. Questo metodo restituisce un puntatore all'interfaccia [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Memorizzare nella cache i puntatori e l'handle del dispositivo.

## <a name="finding-a-decoder-configuration"></a>Ricerca di una configurazione del decodificatore

MFT deve trovare una configurazione compatibile per il dispositivo di decodificatore DXVA. Eseguire i passaggi seguenti all'interno del metodo [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , dopo aver convalidato il tipo di input:

1.  Chiamare [**IDirectXVideoDecoderService:: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Questo metodo restituisce una matrice di GUID del dispositivo del decodificatore.
2.  Scorrere la matrice dei GUID del decodificatore per trovare quelli supportati dal decodificatore. Per un decodificatore MPEG-2, ad esempio, si cercherà **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** o **DXVA2 \_ ModeMPEG2 \_ VLD.**

3.  Quando si trova un GUID del dispositivo del decodificatore candidato, passare il GUID al metodo [**IDirectXVideoDecoderService:: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Questo metodo restituisce una matrice di formati di destinazione di rendering, specificati come valori **D3DFORMAT** .
4.  Scorrere i formati della destinazione di rendering e cercare un formato supportato dal decodificatore.
5.  Chiamare [**IDirectXVideoDecoderService:: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Passare lo stesso GUID del dispositivo di decodificatore, insieme a una struttura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) che descrive il formato di output proposto. Il metodo restituisce una matrice di [**strutture \_ ConfigPictureDecode di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Ogni struttura descrive una possibile configurazione per il dispositivo di decodificatore. Cercare una configurazione supportata dal decodificatore.
6.  Archiviare il formato e la configurazione della destinazione di rendering.

Nel metodo [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) restituire un formato video non compresso, in base al formato di destinazione di rendering proposto.

Nel metodo [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) controllare il tipo di supporto in base al formato di destinazione di rendering.

### <a name="fallback-to-software-decoding"></a>Fallback alla decodifica software

Se MFT non riesce a trovare una configurazione DXVA (ad esempio, se il driver di grafica non ha le funzionalità appropriate), deve restituire il codice di errore **MF \_ e il \_ \_ \_ tipo D3D non supportato** dai metodi [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) e [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . Il caricatore della topologia risponderà inviando il messaggio [**MFT \_ \_ \_ \_ gestione D3D message set**](mft-message-set-d3d-manager.md) con il valore **null** per il parametro *ulParam* . Il MFT deve rilasciare il puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Il caricatore della topologia rinegozierà quindi il tipo di supporto e la MFT potrà usare la decodifica software.

## <a name="allocating-uncompressed-buffers"></a>Allocazione di buffer non compressi

In DXVA 2,0, il decodificatore è responsabile dell'allocazione di superfici Direct3D da usare come buffer video non compressi. Il decodificatore deve allocare 3 superfici per il EVR da usare per la deinterlacciamento. Questo numero è fisso, perché Media Foundation non fornisce un modo per EVR di specificare il numero di superfici richieste dal driver grafico per la deinterlacciamento. Tre superfici dovrebbero essere sufficienti per tutti i driver.

Nel metodo [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) impostare il flusso di **output di MFT fornisce il flag \_ \_ \_ \_ Samples** nella struttura di [**informazioni del flusso di output di MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Questo flag notifica alla sessione multimediale che la MFT alloca gli esempi di output.

Per creare le superfici, chiamare [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface). (L'interfaccia [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) eredita questo metodo da [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)). Questa operazione può essere eseguita in [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)dopo aver individuato il formato della destinazione di rendering.

Per ogni superficie, chiamare [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) per creare un esempio multimediale che contenga la superficie. Il metodo restituisce un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .

## <a name="decoding"></a>Decodifica

Per creare il dispositivo di decodificatore, chiamare [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). Il metodo restituisce un puntatore all'interfaccia [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) del dispositivo di decodificatore.

La decodifica deve essere eseguita all'interno del metodo [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . In ogni frame, chiamare [**IDirect3DDeviceManager9:: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) per testare l'handle del dispositivo. Se il dispositivo è stato modificato, il metodo restituisce il **\_ \_ nuovo \_ \_ dispositivo video DXVA2 E**. In tal caso, effettuare le operazioni seguenti:

1.  Chiudere l'handle del dispositivo chiamando [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Rilasciare i puntatori [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) e [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Aprire un nuovo handle di dispositivo.
4.  Negoziare una nuova configurazione del decodificatore, come descritto in "ricerca di una configurazione di decodificatore" più indietro in questa pagina.
5.  Creare un nuovo dispositivo di decodificatore.

Supponendo che l'handle del dispositivo sia valido, il processo di decodifica funziona nel modo seguente:

1.  Ottenere una superficie disponibile che non è attualmente in uso. (Inizialmente tutte le superfici sono disponibili).
2.  Eseguire una query sull'esempio multimediale per l'interfaccia [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Chiamare [**IMFTrackedSample:: Seallocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) e fornire un puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , implementata dal decodificatore. Quando il renderer video rilascia l'esempio, verrà richiamato il callback del decodificatore.
4.  Chiamare [**IDirectXVideoDecoder:: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
5.  Eseguire le operazioni seguenti una o più volte:
    1.  Chiamare [**IDirectXVideoDecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) per ottenere un buffer del decodificatore DXVA.
    2.  Riempire il buffer.
    3.  Chiamare [**IDirectXVideoDecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
    4.  Chiamare [**IDirectXVideoDecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) per eseguire le operazioni di decodifica sul frame.

DXVA 2,0 usa le stesse strutture di dati di DXVA 1,0 per le operazioni di decodifica. Per il set originale di profili DXVA (per H. 261, H. 263 e MPEG-2), queste strutture di dati sono descritte nella [specifica DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

All'interno di ogni [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)coppia di chiamate di / [**esecuzione**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) BeginFrame, è possibile chiamare più volte [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) , ma solo una volta per ogni tipo di buffer DXVA. Se viene chiamato due volte con lo stesso tipo di buffer, i dati vengono sovrascritti.

Usare il callback del metodo [**Seallocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (passaggio 3) per tenere traccia degli esempi attualmente disponibili e in uso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
