---
description: L'elaborazione video di DXVA incapsula le funzioni dell'hardware grafico dedicato all'elaborazione di immagini video non compresse. I servizi di elaborazione video includono la deinterlacciamento e la combinazione di video.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Elaborazione video DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524545"
---
# <a name="dxva-video-processing"></a>Elaborazione video DXVA

L'elaborazione video di DXVA incapsula le funzioni dell'hardware grafico dedicato all'elaborazione di immagini video non compresse. I servizi di elaborazione video includono la deinterlacciamento e la combinazione di video.

In questo argomento sono incluse le sezioni seguenti:

-   [Overview](#overview)
-   [Creazione di un dispositivo di elaborazione video](#creating-a-video-processing-device)
    -   [Ottenere il puntatore IDirectXVideoProcessorService](#get-the-idirectxvideoprocessorservice-pointer)
    -   [Enumerare i dispositivi di elaborazione video](#enumerate-the-video-processing-devices)
    -   [Enumerare i formati di Render-Target](#enumerate-render-target-formats)
    -   [Eseguire query sulle funzionalità del dispositivo](#query-the-device-capabilities)
    -   [Creare il dispositivo](#create-the-device)
-   [Blit processo video](#video-process-blit)
    -   [Parametri blit](#blit-parameters)
    -   [Esempi di input](#input-samples)
-   [Composizione immagine](#image-composition)
    -   [Esempio 1: Letterbox](#example-1-letterboxing)
    -   [Esempio 2: estensione delle immagini del sottoflusso](#example-2-stretching-substream-images)
    -   [Esempio 3: mancata corrispondenza tra le altezze di flusso](#example-3-mismatched-stream-heights)
    -   [Esempio 4: rettangolo di destinazione più piccolo della superficie di destinazione](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [Esempio 5: rettangoli di origine](#example-5-source-rectangles)
    -   [Esempio 6: intersezione di rettangoli di destinazione](#example-6-intersecting-destination-rectangles)
    -   [Esempio 7: allungamento e ritaglio di video](#example-7-stretching-and-cropping-video)
-   [Ordine di esempio di input](#input-sample-order)
    -   [Esempio 1](#example-1-letterboxing)
    -   [Esempio 2](#example-2-stretching-substream-images)
    -   [Esempio 3](#example-3-mismatched-stream-heights)
    -   [Esempio 4](#example-4-target-rectangle-smaller-than-destination-surface)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

L'hardware grafico può utilizzare l'unità di elaborazione grafica (GPU) per elaborare immagini video non compresse. Un dispositivo di *elaborazione video* è un componente software che incapsula queste funzioni. Le applicazioni possono utilizzare un dispositivo di elaborazione video per eseguire funzioni quali:

-   Deinterlacciamento e telecine inverso
-   Combinazione di sottoflussi video nell'immagine video principale
-   Regolazione del colore (ProcAmp) e filtro delle immagini
-   Ridimensionamento delle immagini
-   Conversione dello spazio colore
-   Fusione alfa

Il diagramma seguente illustra le fasi della pipeline di elaborazione video. Il diagramma non ha lo scopo di mostrare un'implementazione effettiva. Ad esempio, il driver di grafica potrebbe combinare varie fasi in un'unica operazione. Tutte queste operazioni possono essere eseguite in una singola chiamata al dispositivo di elaborazione video. Alcune fasi illustrate di seguito, ad esempio il filtro rumore e i dettagli, potrebbero non essere supportate dal driver.

![diagramma che mostra le fasi dell'elaborazione video di DXVA.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

L'input per la pipeline di elaborazione video include sempre un flusso video *primario* , che contiene i dati dell'immagine principale. Il flusso video primario determina la frequenza dei fotogrammi per il video di output. Ogni frame del video di output viene calcolato in relazione ai dati di input dal flusso video primario. I pixel nel flusso primario sono sempre opachi, senza dati alfa per pixel. Il flusso video primario può essere progressivo o interlacciato.

Facoltativamente, la pipeline di elaborazione video può ricevere fino a 15 sottoflussi video. Un sottoflusso contiene dati di immagine ausiliari, ad esempio didascalie chiuse o immagini secondarie di DVD. Queste immagini vengono visualizzate sul flusso video primario e in genere non sono destinate a essere visualizzate da soli. Le immagini di flussi secondari possono contenere dati alfa per pixel e sono sempre frame progressivi. Il dispositivo di elaborazione video Alpha-combina le immagini del sottoflusso con il frame deinterlacciato corrente dal flusso video primario.

Nella parte restante di questo argomento, il termine *immagine* viene usato per i dati di input in un dispositivo di elaborazione video. Un'immagine può essere costituita da un frame progressivo, da un singolo campo o da due campi con interfoliazione. L'output è sempre un frame deinterlacciato.

Un driver video può implementare più di un dispositivo di elaborazione video per fornire diversi set di funzionalità di elaborazione video. I dispositivi sono identificati dal GUID. I GUID seguenti sono predefiniti:

-   **DXVA2 \_ VideoProcBobDevice**. Questo dispositivo esegue il deinterlacciamento Bob.
-   **DXVA2 \_ VideoProcProgressiveDevice**. Questo dispositivo viene usato se il video contiene solo frame progressivi, senza frame interlacciati. (Alcuni contenuti video contengono una combinazione di frame progressivi e interlacciati. Il dispositivo progressivo non può essere usato per questo tipo di contenuto video misto, perché è necessario un passaggio di deinterlacciamento per i frame interlacciati.

Ogni driver di grafica che supporta l'elaborazione video DXVA deve implementare almeno questi due dispositivi. Il driver di grafica può anche fornire altri dispositivi, che sono identificati da GUID specifici del driver. Un driver, ad esempio, potrebbe implementare un algoritmo di deinterlacciamento proprietario che produce un output di qualità superiore rispetto a quello di Bob deinterlacciamento. Alcuni algoritmi di deinterlacciamento possono richiedere immagini di riferimento in avanti o indietro dal flusso primario. In tal caso, il chiamante deve fornire queste immagini al driver nella sequenza corretta, come descritto più avanti in questa sezione.

Viene inoltre fornito un dispositivo software di riferimento. Il dispositivo software è ottimizzato per la qualità anziché per la velocità e potrebbe non essere adatto per l'elaborazione video in tempo reale. Il dispositivo software di riferimento usa il valore GUID DXVA2 \_ VideoProcSoftwareDevice.

## <a name="creating-a-video-processing-device"></a>Creazione di un dispositivo di elaborazione video

Prima di usare l'elaborazione video DXVA, l'applicazione deve creare un dispositivo di elaborazione video. Ecco una breve descrizione dei passaggi, illustrati più dettagliatamente nella parte restante di questa sezione:

1.  Ottenere un puntatore all'interfaccia [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .
2.  Creare una descrizione del formato video per il flusso video primario. Usare questa descrizione per ottenere un elenco dei dispositivi di elaborazione video che supportano il formato video. I dispositivi sono identificati dal GUID.
3.  Per un dispositivo specifico, ottenere un elenco di formati di destinazione di rendering supportati dal dispositivo. I formati vengono restituiti come un elenco di valori **D3DFORMAT** . Se si prevede di combinare sottoflussi, ottenere anche un elenco dei formati sottoflussi supportati.
4.  Eseguire una query sulle funzionalità di ogni dispositivo.
5.  Creare il dispositivo di elaborazione video.

In alcuni casi è possibile omettere alcuni di questi passaggi. Ad esempio, anziché ottenere l'elenco dei formati di destinazione di rendering, è possibile provare semplicemente a creare il dispositivo di elaborazione video con il formato preferito e verificare se l'operazione ha esito positivo. Un formato comune, ad esempio D3DFMT \_ X8R8G8B8, è probabile che abbia esito positivo.

Nella parte restante di questa sezione vengono descritti in dettaglio questi passaggi.

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a>Ottenere il puntatore IDirectXVideoProcessorService

L'interfaccia [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) è ottenuta dal dispositivo Direct3D. Esistono due modi per ottenere un puntatore a questa interfaccia:

-   Da un dispositivo Direct3D.
-   Dal [Gestione dispositivi Direct3D](direct3d-device-manager.md).

Se è presente un puntatore a un dispositivo Direct3D, è possibile ottenere un puntatore [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) chiamando la funzione [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) . Passare un puntatore all'interfaccia **IDirect3DDevice9** del dispositivo e specificare **IID \_ IDirectXVideoProcessorService** per il parametro *riid* , come illustrato nel codice seguente:


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



n alcuni casi, un oggetto crea il dispositivo Direct3D e lo condivide con altri oggetti tramite il [Gestione dispositivi Direct3D](direct3d-device-manager.md). In questa situazione, è possibile chiamare [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) in gestione dispositivi per ottenere il puntatore [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , come illustrato nel codice seguente:


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a>Enumerare i dispositivi di elaborazione video

Per ottenere un elenco di dispositivi di elaborazione video, compilare una struttura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) con il formato del flusso video primario e passare la struttura al metodo [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) . Il metodo restituisce una matrice di GUID, uno per ogni dispositivo di elaborazione video che può essere usato con questo formato video.

Si consideri un'applicazione che esegue il rendering di un flusso video in formato YUY2 usando la definizione BT. 709 del colore YUV, con una frequenza dei fotogrammi di 29,97 fotogrammi al secondo. Si supponga che il contenuto video sia costituito interamente da frame progressivi. Il frammento di codice seguente mostra come compilare la descrizione del formato e ottenere i GUID del dispositivo:


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



Il codice per questo esempio è tratto dall'esempio [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) SDK.

La matrice *pGuids* in questo esempio viene allocata dal metodo [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , quindi l'applicazione deve liberare la matrice chiamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree). I passaggi rimanenti possono essere eseguiti usando uno dei GUID del dispositivo restituiti da questo metodo.

### <a name="enumerate-render-target-formats"></a>Enumerare i formati di Render-Target

Per ottenere l'elenco dei formati di destinazione di rendering supportati dal dispositivo, passare il GUID del dispositivo e la struttura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) al metodo [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , come illustrato nel codice seguente:


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



Il metodo restituisce una matrice di valori **D3DFORMAT** . In questo esempio, in cui il tipo di input è YUY2, un tipico elenco di formati potrebbe essere D3DFMT \_ X8R8G8B8 (RGB a 32 bit) e D3DMFT \_ YUY2 (il formato di input). Tuttavia, l'elenco esatto dipenderà dal driver.

L'elenco dei formati disponibili per i flussi sottoflussi può variare a seconda del formato di destinazione di rendering e del formato di input. Per ottenere l'elenco dei formati di sottoflusso, passare il GUID del dispositivo, la struttura del formato e il formato di destinazione di rendering al metodo [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , come illustrato nel codice seguente:


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



Questo metodo restituisce un'altra matrice di valori **D3DFORMAT** . I formati di sottoflusso tipici sono AYUV e AI44.

### <a name="query-the-device-capabilities"></a>Eseguire query sulle funzionalità del dispositivo

Per ottenere le funzionalità di un particolare dispositivo, passare il GUID del dispositivo, la struttura del formato e un formato di destinazione di rendering al metodo [**IDirectXVideoProcessorService:: GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) . Il metodo compila una struttura della struttura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con le funzionalità del dispositivo.


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a>Creare il dispositivo

Per creare il dispositivo di elaborazione video, chiamare [**IDirectXVideoProcessorService:: CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor). L'input per questo metodo è il GUID del dispositivo, la descrizione del formato, il formato della destinazione di rendering e il numero massimo di flussi sottoflussi che si prevede di combinare. Il metodo restituisce un puntatore all'interfaccia [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , che rappresenta il dispositivo di elaborazione video.


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a>Blit processo video

L'operazione di elaborazione video principale è l' *elaborazione video blit*. Un *blit* è qualsiasi operazione che combina due o più bitmap in una singola bitmap. Un blit di elaborazione video combina le immagini di input per creare un frame di output. Per eseguire un blit di elaborazione video, chiamare [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Questo metodo passa un set di esempi video al dispositivo di elaborazione video. In risposta, il dispositivo di elaborazione video elabora le immagini di input e genera un frame di output. L'elaborazione può includere la deinterlacciamento, la conversione dello spazio colore e la combinazione di sottoflussi. L'output viene scritto in una superficie di destinazione fornita dal chiamante.

Il metodo [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) accetta i parametri seguenti:

-   *pRT* punta a una superficie di destinazione di rendering **IDirect3DSurface9** che riceverà il frame video elaborato.
-   *pBltParams* punta a una struttura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) che specifica i parametri per blit.
-   *pSamples* è l'indirizzo di una matrice di strutture [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Queste strutture contengono gli esempi di input per blit.
-   *NumSamples valore* fornisce la dimensione della matrice *pSamples* .
-   Il parametro *riservato* è riservato e deve essere impostato su **null**.

Nella matrice *pSamples* il chiamante deve fornire gli esempi di input seguenti:

-   Immagine corrente dal flusso video primario.
-   Immagini di riferimento avanti e indietro, se richieste dall'algoritmo di deinterlacciamento.
-   Zero o più immagini di flussi secondari, fino a un massimo di 15 flussi secondari.

Il driver prevede che la matrice sia in un ordine specifico, come descritto nell' [ordine di esempio di input](#input-sample-order).

### <a name="blit-parameters"></a>Parametri blit

La struttura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contiene parametri generali per blit. I parametri più importanti vengono archiviati nei seguenti membri della struttura:

-   **TargetFrame** è l'ora di presentazione del frame di output. Per contenuti progressivi, questo tempo deve essere uguale all'ora di inizio per il frame corrente dal flusso video primario. Questa volta viene specificato nel membro **iniziale** della struttura [**\_ VideoSample di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) per tale esempio di input.

    Per il contenuto interlacciato, un frame con due campi con interfoliazione produce due fotogrammi di output deinterlacciati. Nel primo frame di output, l'ora di presentazione deve corrispondere all'ora di inizio dell'immagine corrente nel flusso video principale, proprio come il contenuto progressivo. Sul secondo frame di output, l'ora di inizio deve essere uguale al punto medio tra l'ora di inizio dell'immagine corrente nel flusso video primario e l'ora di inizio dell'immagine successiva nel flusso. Se, ad esempio, il video di input è 25 fotogrammi al secondo (50 campi al secondo), i frame di output avranno i timestamp indicati nella tabella seguente. I timestamp vengono visualizzati in unità di 100 nanosecondi.

    

    | Immagine input | **TargetFrame** (1) | **TargetFrame** (2) |
    |---------------|---------------------|---------------------|
    | 0             | 0                   | 200000              |
    | 400000        | 0                   | 600000              |
    | 800000        | 800000              | 1000000             |
    | 1,2 milioni       | 1,2 milioni             | 1,4 milioni             |

    

     

    Se il contenuto interlacciato è costituito da campi singoli anziché da campi con interfoliazione, i tempi di output corrispondono sempre ai tempi di input, come per il contenuto progressivo.

-   **TargetRect** definisce un'area rettangolare all'interno dell'area di destinazione. Blit scriverà l'output in questa area. In particolare, ogni pixel all'interno di **targetRect** verrà modificato e nessun pixel al di fuori di **targetRect** verrà modificato. Il rettangolo di destinazione definisce il rettangolo di delimitazione per tutti i flussi video di input. La posizione dei singoli flussi all'interno di tale rettangolo viene controllata tramite il parametro *pSamples* di [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).
-   **BackgroundColor** restituisce il colore dello sfondo quando non viene visualizzata alcuna immagine video. Quando, ad esempio, viene visualizzata un'immagine video di 16 x 9 in un'area di 4 x 3 (letterbox), le aree letterbox vengono visualizzate con il colore di sfondo. Il colore di sfondo si applica solo all'interno del rettangolo di destinazione (**targetRect**). Qualsiasi pixel al di fuori di **targetRect** non viene modificato.
-   **DestFormat** descrive lo spazio di colore per il video di output, ad esempio se viene usato il colore ITU-R BT. 709 o BT. 601. Queste informazioni possono influire sul modo in cui viene visualizzata l'immagine. Per ulteriori informazioni, vedere [informazioni sui colori estese](extended-color-information.md).

Altri parametri sono descritti nella pagina di riferimento per la [**struttura \_ VideoProcessBltParams di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .

### <a name="input-samples"></a>Esempi di input

Il parametro *pSamples* di [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) punta a una matrice di strutture [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Ognuna di queste strutture contiene informazioni su un esempio di input e un puntatore alla superficie Direct3D che contiene l'esempio. Ogni esempio è uno dei seguenti:

-   Immagine corrente dal flusso primario.
-   Immagine di riferimento avanti o indietro dal flusso primario, usata per la deinterlacciamento.
-   Immagine del flusso di flussi.

L'ordine esatto in cui gli esempi devono essere visualizzati nella matrice è descritto più avanti nella sezione [ordine di esempio di input](#input-sample-order).

È possibile fornire fino a 15 immagini di flussi secondari, sebbene la maggior parte delle applicazioni video necessiti di un solo sottoflusso, al massimo. Il numero di flussi substream può variare con ogni chiamata a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Le immagini di flussi secondari sono indicate impostando il membro **SampleFormat. SampleFormat** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) uguale a DXVA2 \_ SampleSubStream. Per il flusso video primario, questo membro descrive l'interlacciamento del video di input. Per ulteriori informazioni, vedere [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) Enumeration.

Per il flusso video primario, i membri **iniziale** e **finale** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) forniscono le ore di inizio e di fine dell'esempio di input. Per le immagini di flussi secondari, impostare questi valori su zero, perché l'ora di presentazione viene sempre calcolata dal flusso primario. L'applicazione è responsabile del rilevamento del momento in cui ogni immagine di flusso substream deve essere presentata e inviata a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) al momento giusto.

Due rettangoli definiscono la modalità di posizionamento del video di origine per ogni flusso:

-   Il membro **SrcRect** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) specifica il *rettangolo di origine*, un'area rettangolare dell'immagine di origine che verrà visualizzata nel frame di output composito. Per ritagliare l'immagine, impostarla su un valore inferiore alle dimensioni del frame. In caso contrario, impostarlo uguale alle dimensioni del frame.
-   Il membro **DstRect** della stessa struttura specifica il *rettangolo di destinazione*, un'area rettangolare della superficie di destinazione in cui verrà visualizzato il frame del video.

Il driver Blits i pixel dal rettangolo di origine al rettangolo di destinazione. I due rettangoli possono avere dimensioni o proporzioni diverse; il driver scalerà l'immagine in base alle esigenze. Ogni flusso di input può inoltre utilizzare un fattore di scala diverso. Di fatto, la scalabilità potrebbe essere necessaria per produrre le proporzioni corrette nel frame di output. Il driver non prende in considerazione le proporzioni dei pixel dell'origine, pertanto se l'immagine di origine utilizza pixel non quadrati, spetta all'applicazione calcolare il rettangolo di destinazione corretto.

I formati dei sottoflussi preferiti sono AYUV e AI44. Quest'ultimo è un formato pallet con 16 colori. Le voci della tavolozza sono specificate nel membro **PAL** della struttura [**\_ VideoSample di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Se il formato del video di origine è espresso originariamente come tipo di supporto Media Foundation, le voci della tavolozza vengono archiviate nell'attributo della [**\_ \_ tavolozza MF mt**](mf-mt-palette-attribute.md) . Per i formati non pallet, deselezionare la matrice su zero.

## <a name="image-composition"></a>Composizione immagine

Ogni operazione blit è definita dai tre rettangoli seguenti:

-   Il rettangolo di *destinazione* (**targetRect**) definisce l'area all'interno della superficie di destinazione in cui verrà visualizzato l'output. L'immagine di output viene ritagliata in questo rettangolo.
-   Il rettangolo di *destinazione* per ogni flusso (**DstRect**) definisce dove viene visualizzato il flusso di input nell'immagine composita.
-   Il rettangolo di *origine* per ogni flusso (**SrcRect**) definisce quale parte dell'immagine di origine viene visualizzata.

I rettangoli di destinazione e di destinazione vengono specificati in relazione alla superficie di destinazione. Il rettangolo di origine viene specificato in relazione all'immagine di origine. Tutti i rettangoli sono specificati in pixel.

![diagramma che mostra i rettangoli di origine, di destinazione e di destinazione](images/dxva-vp-rects.gif)

Il dispositivo di elaborazione video Alpha fonde le immagini di input, usando una delle seguenti origini di dati Alpha:

-   Dati alfa per pixel da sottoflussi.
-   Valore alfa planare per ogni flusso video, specificato nel membro **PlanarAlpha** della struttura [**\_ VideoSample di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .
-   Valore alfa planare dell'immagine composita, specificata nel membro **Alpha** della struttura VideoProcessBltParams di [**DXVA2 \_**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) . Questo valore viene usato per fondere l'intera immagine composita con il colore di sfondo.

Questa sezione fornisce una serie di esempi che illustrano il modo in cui il dispositivo di elaborazione video crea l'immagine di output.

### <a name="example-1-letterboxing"></a>Esempio 1: Letterbox

Questo esempio illustra come creare una letterbox per l'immagine di origine, impostando il rettangolo di destinazione su un valore inferiore al rettangolo di destinazione. Il flusso video primario in questo esempio è un'immagine 720 × 480 ed è destinato a essere visualizzato in corrispondenza di un 16:9 proporzioni. La superficie di destinazione è 640 × 480 pixel (4:3 proporzioni). Per ottenere le proporzioni corrette, il rettangolo di destinazione deve essere 640 × 360. Per semplicità, in questo esempio non è incluso un sottoflusso. Nel diagramma seguente vengono illustrati i rettangoli di origine e di destinazione.

![diagramma che mostra le letterbox.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

Il diagramma precedente Mostra i rettangoli seguenti:

-   Rettangolo di destinazione: {0, 0, 640, 480}
-   Video principale:

    -   Rettangolo di origine: {0, 0, 720, 480}
    -   Rettangolo di destinazione: {0, 60, 640, 420}

Il driver Deinterlaccia il video, compatta il frame deinterlacciato a 640 × 360 e blit il frame nel rettangolo di destinazione. Il rettangolo di destinazione è più grande del rettangolo di destinazione, pertanto il driver utilizzerà il colore di sfondo per riempire le barre orizzontali sopra e sotto il frame. Il colore di sfondo viene specificato nella [**struttura \_ VideoProcessBltParams di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .

### <a name="example-2-stretching-substream-images"></a>Esempio 2: estensione delle immagini del sottoflusso

Le immagini di flussi secondari possono estendersi oltre l'immagine principale del video. Nel video DVD, ad esempio, il flusso video primario può avere una proporzioni 4:3 mentre il sottoflusso è 16:9. In questo esempio, entrambi i flussi video hanno le stesse dimensioni di origine (720 × 480), ma il sottoflusso deve essere visualizzato in base a un rapporto 16:9. Per ottenere queste proporzioni, l'immagine del sottoflusso viene allungata orizzontalmente. I rettangoli di origine e di destinazione sono illustrati nel diagramma seguente.

![diagramma che mostra l'estensione dell'immagine del flusso secondari.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

Il diagramma precedente Mostra i rettangoli seguenti:

-   Rettangolo di destinazione: {0, 0, 854, 480}
-   Video principale:

    -   Rettangolo di origine: {0, 0, 720, 480}
    -   Rettangolo di destinazione: {0, 107, 474, 480}

-   Substream
    -   Rettangolo di origine: {0, 0, 720, 480}
    -   Rettangolo di destinazione: {0, 0, 854, 480}

Questi valori conservano l'altezza dell'immagine e scalano entrambe le immagini orizzontalmente. Nelle aree in cui sono visualizzate entrambe le immagini, sono con Blend alfa. Se l'immagine del sottoflusso exends oltre il video prima, il sottoflusso è alfa blended con il colore di sfondo. Questo account di fusione alfa per i colori modificati sul lato destro del diagramma.

### <a name="example-3-mismatched-stream-heights"></a>Esempio 3: mancata corrispondenza tra le altezze di flusso

Nell'esempio precedente, il sottoflusso e il flusso primario sono della stessa altezza. I flussi possono anche avere altezze non corrispondenti, come illustrato in questo esempio. Le aree all'interno del rettangolo di destinazione in cui non viene visualizzato alcun video vengono disegnate utilizzando il colore di sfondo, in questo esempio il nero. I rettangoli di origine e di destinazione sono illustrati nel diagramma seguente.

![diagramma che mostra le altezze di flusso non corrispondenti,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

Il diagramma precedente Mostra i rettangoli seguenti:

-   Rettangolo di destinazione: {0, 0, 150, 85}
-   Video principale:
    -   Rettangolo di origine: {0, 0, 150, 50}
    -   Rettangolo di destinazione: {0, 17, 150, 67}
-   Substream
    -   Rettangolo di origine: {0, 0, 100, 85}
    -   Rettangolo di destinazione: {25, 0, 125, 85}

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a>Esempio 4: rettangolo di destinazione più piccolo della superficie di destinazione

In questo esempio viene illustrato un caso in cui il rettangolo di destinazione è più piccolo della superficie di destinazione.

![diagramma che mostra un blit a un rettangolo di destinazione.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

Il diagramma precedente Mostra i rettangoli seguenti:

-   Superficie di destinazione: {0, 0, 300, 200}
-   Rettangolo di destinazione: {0, 0, 150, 85}
-   Video principale:
    -   Rettangolo di origine: {0, 0, 150, 50}
    -   Rettangolo di destinazione: {0, 17, 150, 67}
-   Substream
    -   Rettangolo di origine: {0, 0, 100, 85}
    -   Rettangolo di destinazione: {25, 0, 125, 85}

I pixel all'esterno del rettangolo di destinazione non vengono modificati, pertanto il colore di sfondo viene visualizzato solo all'interno del rettangolo di destinazione. L'area tratteggiata indica parti della superficie di destinazione che non sono interessate dal blit.

### <a name="example-5-source-rectangles"></a>Esempio 5: rettangoli di origine

Se si specifica un rettangolo di origine inferiore a quello dell'immagine di origine, il driver blit solo quella parte dell'immagine. In questo esempio, i rettangoli di origine specificano il quadrante inferiore destro del flusso video primario e il quadrante inferiore sinistro del sottoflusso, indicato dai contrassegni hash nel diagramma. I rettangoli di destinazione hanno le stesse dimensioni dei rettangoli di origine, quindi il video non viene allungato. I rettangoli di origine e di destinazione sono illustrati nel diagramma seguente.

![diagramma che mostra un blit da due rettangoli di origine.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

Il diagramma precedente Mostra i rettangoli seguenti:

-   Rettangolo di destinazione: {0, 0, 720, 576}
-   Video principale:
    -   Dimensioni superficie di origine: {0, 0, 720, 480}
    -   Rettangolo di origine: {360, 240, 720, 480}
    -   Rettangolo di destinazione: {0, 0, 360, 240}
-   Substream
    -   Dimensioni superficie di origine: {0, 0, 640, 576}
    -   Rettangolo di origine: {0, 288, 320, 576}
    -   Rettangolo di destinazione: {400, 0, 720, 288}

### <a name="example-6-intersecting-destination-rectangles"></a>Esempio 6: intersezione di rettangoli di destinazione

Questo esempio è simile a quello precedente, ma i rettangoli di destinazione si intersecano. Le dimensioni della superficie sono identiche a quelle dell'esempio precedente, ma i rettangoli di origine e di destinazione non lo sono. Anche in questo caso, il video viene ritagliato ma non allungato. I rettangoli di origine e di destinazione sono illustrati nel diagramma seguente.

![diagramma che mostra i rettangoli di destinazione intersecanti.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

Il diagramma precedente Mostra i rettangoli seguenti:

-   Rettangolo di destinazione: {0, 0, 720, 576}
-   Video principale:
    -   Dimensioni superficie di origine: {0, 0, 720, 480}
    -   Rettangolo di origine: {260, 92, 720, 480}
    -   Rettangolo di destinazione: {0, 0, 460, 388}
-   Substream
    -   Dimensioni superficie di origine: {0, 0, 640, 576}
    -   Rettangolo di origine: {0, 0, 460, 388}
    -   Rettangolo di destinazione: {260, 188, 720, 576}

### <a name="example-7-stretching-and-cropping-video"></a>Esempio 7: allungamento e ritaglio di video

In questo esempio il video è allungato e ritagliato. Un'area 180 × 120 da ogni flusso viene estesa per coprire un'area 360 × 240 nel rettangolo di destinazione.

![diagramma che mostra l'estensione e il ritaglio.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

Il diagramma precedente Mostra i rettangoli seguenti:

-   Rettangolo di destinazione: {0, 0, 720, 480}
-   Video principale:
    -   Dimensioni superficie di origine: {0, 0, 360, 240}
    -   Rettangolo di origine: {180, 120, 360, 240}
    -   Rettangolo di destinazione: {0, 0, 360, 240}
-   Substream
    -   Dimensioni superficie di origine: {0, 0, 360, 240}
    -   Rettangolo di origine: {0, 0, 180, 120}
    -   Rettangolo di destinazione: {360, 240, 720, 480}

## <a name="input-sample-order"></a>Ordine di esempio di input

Il parametro *pSamples* del metodo [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) è un puntatore a una matrice di esempi di input. Gli esempi dal flusso video primario vengono visualizzati per primi, seguiti da immagini substream nell'ordine Z. Gli esempi devono essere inseriti nella matrice nell'ordine seguente:

-   Gli esempi per il flusso video primario vengono visualizzati per primi nella matrice, in ordine temporale. A seconda della modalità di deinterlacciamento, il driver potrebbe richiedere uno o più esempi di riferimento dal flusso video primario. I membri **NumForwardRefSamples** e **NumBackwardRefSamples** della struttura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) specificano il numero di campioni di riferimento avanti e indietro necessari. Il chiamante deve fornire questi esempi di riferimento anche se il contenuto video è progressivo e non richiede la deinterlacciamento. Questa situazione può verificarsi quando si assegnano frame progressivi a un dispositivo di deinterlacciamento, ad esempio quando l'origine contiene una combinazione di frame sia interlacciati che progressivi.
-   Dopo gli esempi per il flusso video primario, la matrice può contenere fino a 15 campioni di sottoflusso, disposti in ordine Z, dal basso verso l'alto. I flussi secondari sono sempre progressivi e non richiedono immagini di riferimento.

In qualsiasi momento, il flusso video primario può passare da contenuto interlacciato a quello progressivo e il numero di flussi subesistenti può cambiare.

Il membro **SampleFormat. SampleFormat** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indica il tipo di immagine. Per le immagini di flussi secondari, impostare questo valore su DXVA2 \_ SampleSubStream. Per le immagini progressive, il valore è DXVA2 \_ SampleProgressiveFrame. Per le immagini interlacciate, il valore dipende dal layout del campo.

Se il driver richiede esempi di riferimento avanti e indietro, il numero completo di campioni potrebbe non essere disponibile all'inizio della sequenza video. In tal caso, includere le relative voci nella matrice *pSamples* , ma contrassegnare i campioni mancanti con il tipo DXVA2 \_ SampleUnknown.

I membri **iniziale** e **finale** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) forniscono la posizione temporale di ogni campione. Questi valori vengono usati solo per gli esempi dal flusso video primario. Per le immagini di flussi secondari, impostare entrambi i membri su zero.

Gli esempi seguenti possono essere utili per chiarire tali requisiti.

### <a name="example-1"></a>Esempio 1

Il caso più semplice si verifica quando non sono presenti sottoflussi e l'algoritmo di deinterlacciamento non richiede esempi di riferimento (**NumForwardRefSamples** e **NumBackwardRefSamples** sono entrambi zero). Il deinterlacciamento Bob è un esempio di tale algoritmo. In questo caso, la matrice *pSamples* deve contenere una singola superficie di input, come illustrato nella tabella seguente.



| Indice           | Tipo di superficie        | Posizione temporale |
|-----------------|---------------------|-------------------|
| *pSamples* \[ 0\] | Immagine interlacciata. | *T*               |



 

Si presuppone che il valore time *T* sia l'ora di inizio del fotogramma video corrente.

### <a name="example-2"></a>Esempio 2

In questo esempio, l'applicazione combina due sottoflussi con il flusso primario. L'algoritmo di deinterlacciamento non richiede esempi di riferimento. Nella tabella seguente viene illustrato il modo in cui questi esempi vengono disposti nella matrice *pSamples* .



| Indice           | Tipo di superficie       | Posizione temporale | Ordine Z |
|-----------------|--------------------|-------------------|---------|
| *pSamples* \[ 0\] | Immagine interlacciata | *T*               | 0       |
| *pSamples* \[ 1\] | Substream          | 0                 | 1       |
| *pSamples* \[ 2\] | Substream          | 0                 | 2       |



 

### <a name="example-3"></a>Esempio 3

Si supponga ora che l'algoritmo di deinterlacciamento richieda un esempio di riferimento all'indietro e un esempio di riferimento in avanti. Vengono inoltre fornite due immagini di flussi secondari, per un totale di cinque superfici. L'ordinamento corretto è illustrato nella tabella seguente.



| Indice           | Tipo di superficie                   | Posizione temporale | Ordine Z        |
|-----------------|--------------------------------|-------------------|----------------|
| *pSamples* \[ 0\] | Immagine interlacciata (riferimento) | *T* − 1            | Non applicabile |
| *pSamples* \[ 1\] | Immagine interlacciata             | *T*               | 0              |
| *pSamples* \[ 2\] | Immagine interlacciata (riferimento) | *T* + 1            | Non applicabile |
| *pSamples* \[ 3\] | Substream                      | 0                 | 1              |
| *pSamples* \[ 4\] | Substream                      | 0                 | 2              |



 

L'ora *t* − 1 è l'ora di inizio del frame prima del frame corrente e *T* + 1 è l'ora di inizio del frame seguente.

Se il flusso video passa al contenuto progressivo, usando la stessa modalità di deinterlacciamento, l'applicazione deve fornire lo stesso numero di campioni, come illustrato nella tabella seguente.



| Indice           | Tipo di superficie                    | Posizione temporale | Ordine Z        |
|-----------------|---------------------------------|-------------------|----------------|
| *pSamples* \[ 0\] | Immagine progressiva (riferimento) | *T* − 1            | Non applicabile |
| *pSamples* \[ 1\] | Immagine progressiva             | *T*               | 0              |
| *pSamples* \[ 2\] | Immagine progressiva (riferimento) | *T* + 1            | Non applicabile |
| *pSamples* \[ 3\] | Substream                       | 0                 | 1              |
| *pSamples* \[ 4\] | Substream                       | 0                 | 2              |



 

### <a name="example-4"></a>Esempio 4

All'inizio di una sequenza video, gli esempi di riferimento avanti e indietro potrebbero non essere disponibili. Quando si verifica questa situazione, le voci degli esempi mancanti sono incluse nella matrice *pSamples* , con il tipo di esempio DXVA2 \_ SampleUnknown.

Supponendo che la modalità di deinterlacciamento necessiti di un esempio di riferimento a ritroso e in avanti, le prime tre chiamate a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) avrebbero le sequenze di input visualizzate nelle tre tabelle seguenti.



| Indice           | Tipo di superficie                   | Posizione temporale |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Sconosciuto                        | 0                 |
| *pSamples* \[ 1\] | Sconosciuto                        | 0                 |
| *pSamples* \[ 2\] | Immagine interlacciata (riferimento) | *T* + 1            |



 



| Indice           | Tipo di superficie                   | Posizione temporale |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Sconosciuto                        | 0                 |
| *pSamples* \[ 1\] | Immagine interlacciata             | *T*               |
| *pSamples* \[ 2\] | Immagine interlacciata (riferimento) | *T* + 1            |



 



| Indice           | Tipo di superficie                   | Posizione temporale |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Immagine interlacciata             | *T* − 1            |
| *pSamples* \[ 1\] | Immagine interlacciata             | *T*               |
| *pSamples* \[ 2\] | Immagine interlacciata (riferimento) | *T* + 1            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[\_Esempio DXVA2 VideoProc](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
