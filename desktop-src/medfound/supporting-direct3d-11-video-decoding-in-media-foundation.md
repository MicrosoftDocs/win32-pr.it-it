---
description: Questo argomento descrive come supportare Microsoft Direct3D 11 in un Microsoft Media Foundation decodificatore.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Supporto della decodifica video Direct3D 11 in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95a1d1bc1dd9987fe59fe807e56aa9af1ea4ad597b72c077906483d623e11e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972885"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Supporto della decodifica video Direct3D 11 in Media Foundation

Questo argomento descrive come supportare Microsoft Direct3D 11 in un Microsoft Media Foundation decodificatore. In particolare, descrive la comunicazione tra il decodificatore e il renderer video. In questo argomento non viene descritto come implementare le operazioni di decodifica.

-   [Overview](#overview)
-   [Aprire un handle di dispositivo](#open-a-device-handle)
-   [Trovare una configurazione del decodificatore](#find-a-decoder-configuration)
-   [Fallback alla decodifica software](#fallback-to-software-decoding)
-   [Allocazione di buffer non compressi](#allocating-uncompressed-buffers)
-   [Decodifica](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Nella parte restante di questo argomento vengono usati i termini seguenti:

-   **Decodificatore software**. Il decodificatore software è Media Foundation transform (MFT) che riceve campioni video compressi e restituisce fotogrammi video non compressi.
-   **Dispositivo decodificatore**. Il dispositivo decodificatore è l'acceleratore video e viene implementato dal driver di grafica. Il dispositivo decodificatore esegue operazioni di decodifica accelerata.
-   **Pipeline**. La pipeline ospita il decodificatore software e recapita buffer da e verso il decodificatore software. A seconda dell'applicazione, la pipeline potrebbe [](source-reader.md)essere [la sessione](media-session.md)multimediale, il lettore di origine o il codice dell'applicazione che chiama direttamente in MFT.

Per eseguire la decodifica usando Direct3D 11, il decodificatore software deve avere un puntatore a un dispositivo Direct3D 11. Il dispositivo Direct3D 11 viene creato esternamente al decodificatore software. In uno scenario [di sessione](media-session.md) multimediale, il renderer video crea il dispositivo Direct3D 11. In uno scenario [di lettura origine,](source-reader.md) in genere l'applicazione crea il dispositivo Direct3D 11.

Gestione dispositivi DXGI viene usato per condividere Direct3D 11 tra componenti. Gestione dispositivi DXGI espone [**l'interfaccia IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) La pipeline imposta il **puntatore IMFDXGIDeviceManager** sul decodificatore software inviando il messaggio [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md)

Il diagramma seguente illustra la relazione tra il decodificatore software, Direct3D 11 e la pipeline.

![diagramma che mostra il decodificatore software e il gestore di dispositivi dxgi.](images/d3d11video01.png)

Ecco i passaggi di base che un decodificatore software deve eseguire per supportare Direct3D 11 in Media Foundation:

1.  Aprire un handle per il dispositivo Direct3D 11.
2.  Trovare una configurazione del decodificatore.
3.  Allocare buffer non compressi.
4.  Decodificare i fotogrammi.

Questi passaggi sono descritti in modo più dettagliato nella parte restante di questo argomento.

## <a name="open-a-device-handle"></a>Aprire un handle di dispositivo

Il decodificatore MFT usa gestione dispositivi DXGI per ottenere un handle per il dispositivo Direct3D 11. Per aprire l'handle del dispositivo, seguire questa procedura:

1.  Il decodificatore MFT deve esporre [l'attributo MF \_ SA \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) con valore **TRUE.**
2.  Il caricatore della topologia esegue una query su questo attributo chiamando [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Il valore **TRUE** indica che MFT supporta Direct3D 11.
3.  Il caricatore della topologia chiama [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md) Il *parametro ulParam* è un [**puntatore IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) alla gestione dispositivi DXGI. Eseguire una query su questo puntatore [**per l'interfaccia IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)
4.  Chiamare [**IMFDXGIDeviceManager::OpenDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) per ottenere un handle per il dispositivo Direct3D 11.
5.  Per ottenere un puntatore al dispositivo Direct3D 11, chiamare [**IMFDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Passare l'handle del dispositivo e il **valore IID \_ ID3D11Device**. Il metodo restituisce un puntatore [**all'interfaccia ID3D11Device.**](/windows/win32/api/d3d11/nn-d3d11-id3d11device)
6.  Per ottenere un puntatore all'acceleratore video, chiamare di [**nuovo IMFDXGIDeviceManager::GetVideoService.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) Questa volta, passare l'handle del dispositivo e il **valore IID \_ ID3D11VideoDevice**. Il metodo restituisce un puntatore [**all'interfaccia ID3D11VideoDevice.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice)
7.  Chiamare [**ID3D11Device::GetImmediateContext**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) per ottenere un [**puntatore ID3D11DeviceContext.**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext)
8.  Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) per ottenere un [**puntatore ID3D11VideoContext.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext)
9.  È consigliabile usare la protezione multi-thread nel contesto di dispositivo per evitare problemi di deadlock che a volte possono verificarsi quando si chiama [**ID3D11VideoContext::GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) o [**ID3D11VideoContext::ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer). Per impostare la protezione multithread, chiamare prima [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) per ottenere un [**puntatore ID3D10Multithread.**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) Chiamare quindi [**ID3D10Multithread::SetMultithreadProtected**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected), passando **true** per *bMTProtect*.

## <a name="find-a-decoder-configuration"></a>Trovare una configurazione del decodificatore

Per eseguire la decodifica, il decodificatore software deve trovare una configurazione compatibile supportata dal dispositivo decodificatore, incluso un formato di destinazione di rendering. Questo passaggio si verifica [**all'interno del metodo IMFTransform::SetInputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) come indicato di seguito.

1.  Convalidare il tipo di supporto di input. Se il tipo viene rifiutato, ignorare i passaggi rimanenti e restituire un codice di errore.
2.  Chiamare [**ID3D11VideoDevice::GetVideoDecoderProfileCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) per ottenere il numero di profili supportati.
3.  Chiamare [**ID3D11VideoDevice::GetVideoDecoderProfile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) per enumerare i profili e ottenere i GUID del profilo.
4.  Cercare un GUID del profilo che corrisponda al formato video e alle funzionalità del decodificatore software. Ad esempio, un decodificatore MPEG-2 cerca **D3D11 \_ DECODER \_ PROFILE \_ MPEG2 \_ MOCOMP,****D3D11 \_ DECODER \_ PROFILE \_ MPEG2 \_ IDCT** e **D3D11 \_ DECODER PROFILE \_ \_ MPEG2 \_ VLD**.
5.  Se viene trovato un GUID del decodificatore appropriato, controllare il formato di output chiamando il [**metodo ID3D11VideoDevice::CheckVideoDecoderFormat.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) Passare il GUID del decodificatore e un **valore DXGI \_ FORMAT** che specifica il formato della destinazione di rendering.
6.  Trovare quindi una configurazione appropriata per il decodificatore.
    1.  Chiamare [**ID3D11VideoDevice::GetVideoDecoderConfigCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) per ottenere il numero di configurazioni del decodificatore. Passare lo stesso GUID del dispositivo decodificatore, insieme a una struttura [**D3D11 \_ VIDEO \_ DECODER \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) che descrive il formato di destinazione di rendering proposto.
    2.  Chiamare [**ID3D11VideoDevice::GetVideoDecoderConfig**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) per enumerare le configurazioni del decodificatore.

Nel metodo [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) restituire un formato video non compresso in base al formato di destinazione di rendering proposto.

Nel metodo [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) controllare il tipo di supporto rispetto al formato di destinazione di rendering.

## <a name="fallback-to-software-decoding"></a>Fallback alla decodifica software

L'MFT potrebbe non essere in grado di trovare una configurazione. Ad esempio, il driver di grafica potrebbe non supportare le funzionalità giuste. In tal caso, il MFT deve eseguire il fall back alla decodifica software, come indicato di seguito.

1.  I [**metodi SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) [**e SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) devono entrambi restituire **MF E \_ \_ UNSUPPORTED \_ D3D \_ TYPE**.
2.  In risposta, il caricatore della topologia invierà il messaggio [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) con il **valore NULL** per il *parametro ulParam.*
3.  MFT rilascia il puntatore [**all'interfaccia IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)
4.  Il caricatore della topologia rinegozia il tipo di supporto.

A questo punto, MFT può usare la decodifica software.

## <a name="allocating-uncompressed-buffers"></a>Allocazione di buffer non compressi

Il decodificatore è responsabile dell'allocazione di trame Direct3D 11 da usare come buffer video non compressi. L'attributo [MF \_ SA MINIMUM OUTPUT SAMPLE \_ \_ \_ \_ COUNT](mf-sa-minimum-output-sample-count.md) negli attributi del flusso di output (vedere [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) viene usato per determinare il numero di superfici che il decodificatore deve allocare per il renderer video da usare per la deinterlacing. Un decodificatore deve usare questo valore che lo delimita per alcuni limiti ragionevoli, ad esempio 3-32. Per il contenuto progressivo, vedere [MF \_ SA MINIMUM OUTPUT SAMPLE COUNT \_ \_ \_ \_ \_ PROGRESSIVE](mf-sa-minimum-output-sample-count-progressive.md).

Nel metodo [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) impostare il flag **MFT \_ OUTPUT STREAM \_ PROVIDES \_ \_ SAMPLES** nella struttura [**MFT OUTPUT STREAM \_ \_ \_ INFO.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) Questo flag notifica alla sessione multimediale che MFT alloca i propri campioni di output. Per allocare gli esempi di output, MFT esegue la procedura seguente:

1.  Creare una matrice di trame 2D chiamando [**ID3D11Device::CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d). Nella struttura [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) impostare **ArraySize** sul numero di superfici necessarie per il decodificatore. ad esempio:
    -   Superfici per i fotogrammi di riferimento.
    -   Superfici per la deinterlacing (tre superfici).
    -   Superfici necessarie al decodificatore per la memorizzazione nel buffer.

    I flag di associazione (**BindFlags**) devono includere il flag **D3D11 \_ BIND \_ DECODER** ed eventuali flag di associazione impostati tramite l'attributo [BINDFLAGS di MF \_ SA \_ D3D11 \_](mf-sa-d3d11-bindflags.md) negli attributi del flusso di output.
2.  Per ogni superficie nella matrice di trame, chiamare [**ID3D11VideoDevice::CreateVideoDecoderOutputView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) per creare una visualizzazione di output del decodificatore video. Durante la decodifica, queste visualizzazioni di output verranno passate al metodo [**ID3D11VideoContext::D ecoderBeginFrame.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)
3.  Per ogni superficie nella matrice di trame, creare un esempio multimediale come segue:
    1.  Creare un buffer multimediale DXGI chiamando la [**funzione MFCreateDXGISurfaceBuffer.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) Passare il [**puntatore ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) e l'offset per ogni elemento nella matrice di trame. La funzione restituisce un [**puntatore IMFMediaBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
    2.  Creare un esempio di supporto vuoto chiamando la [**funzione MFCreateVideoSampleFromSurface.**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) Impostare il *parametro pUnkSurface* su **NULL.** La funzione restituisce un [**puntatore IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
    3.  Chiamare [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) per aggiungere il buffer multimediale all'esempio.

È consigliabile eliminare tutte le trame create contemporaneamente, invece di eliminare solo alcune e continuare a usare il promemoria.

## <a name="decoding"></a>Decodifica

Per creare il dispositivo decodificatore, chiamare [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder). Il metodo restituisce un puntatore [**all'interfaccia ID3D11VideoDecoder.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) La decodifica deve avvenire all'interno [**del metodo IMFTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) In ogni frame chiamare [**IMFDXGIDeviceManager::TestDevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) per testare la disponibilità del DXGI. Se il dispositivo è stato modificato, il decodificatore software deve ricreare il dispositivo decodificatore, come indicato di seguito:

1.  Chiudere l'handle del dispositivo chiamando [**IMFDXGIDeviceManager::CloseDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle).
2.  Rilasciare tutte le risorse associate al dispositivo Direct3D 11 precedente, incluse le interfacce [**ID3D11VideoDecoder,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) [**ID3D11VideoContext,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)e [**ID3D11VideoDecoderOutputView.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview)
3.  Aprire un nuovo handle di dispositivo.
4.  Negoziare una nuova configurazione del decodificatore, come descritto in precedenza in [Trovare una configurazione del decodificatore](#find-a-decoder-configuration). Questo passaggio è necessario perché le funzionalità del dispositivo potrebbero essere state modificate.
5.  Creare un nuovo dispositivo decodificatore.

Supponendo che l'handle del dispositivo sia valido, il processo di decodifica funziona come segue:

1.  Ottenere una superficie disponibile che non è attualmente in uso. Inizialmente, tutte le superfici sono disponibili.
2.  Eseguire una query sull'esempio multimediale per [**l'interfaccia IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)
3.  Chiamare [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) e fornire un puntatore [**all'interfaccia IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) Il decodificatore software deve implementare questa interfaccia. Quando il renderer video rilascia l'esempio, viene richiamato il callback. Usare questo callback per tenere traccia degli esempi attualmente disponibili e degli esempi in uso.
4.  Chiamare [**ID3D11VideoContext::D ecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe). Passare i puntatori [**all'interfaccia ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) per il dispositivo decodificatore e all'interfaccia [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) per la visualizzazione di output.
5.  Eseguire le operazioni seguenti una o più volte:
    1.  Chiamare [**ID3D11VideoContext::GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) per ottenere un buffer.
    2.  Riempire il buffer.
    3.  Chiamare [**ID3D11VideoContext::ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer).
    4.  Chiamare [**ID3D11VideoContext::SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers). Questo metodo indica al dispositivo decodificatore di eseguire le operazioni di decodifica sul frame.
6.  Chiamare [**ID3D11VideoContext::D ecoderEndFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) per segnalare la fine della decodifica per il frame corrente.

Direct3D 11 usa le stesse strutture di dati di DXVA 2.0 per le operazioni di decodifica. Per il set originale di profili DXVA (per H.261, H.263 e MPEG-2), queste strutture di dati sono descritte nella [specifica DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

All'interno di ogni coppia di chiamate [**DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) e [**SubmitDecoderBuffer,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) è possibile chiamare [**GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) più volte, ma solo una volta per ogni tipo di buffer. Se si usa lo stesso tipo di buffer due volte senza chiamare **SubmitDecoderBuffer**, i dati verranno sovrascritti nel buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API video Direct3D 11](direct3d-11-video-apis.md)
</dt> <dt>

[Accelerazione video DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
