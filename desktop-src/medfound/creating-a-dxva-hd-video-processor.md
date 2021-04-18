---
description: .
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Creazione di un processore video DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee524681cad43a8e140421e8e6eff30d44cabcc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305470"
---
# <a name="creating-a-dxva-hd-video-processor"></a>Creazione di un processore video DXVA-HD

Microsoft DirectX Video Acceleration High Definition (DXVA-HD) usa due interfacce primarie:

-   [**IDXVAHD \_ Dispositivo**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device). Rappresenta il dispositivo DXVA-HD. Usare questa interfaccia per eseguire una query sulle funzionalità del dispositivo e creare il processore video.
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor). Rappresenta un set di funzionalità di elaborazione video. Usare questa interfaccia per eseguire il blit di elaborazione video.

Nel codice seguente vengono presupposte le seguenti variabili globali:


```C++
IDirect3D9Ex            *g_pD3D = NULL;     
IDirect3DDevice9Ex      *g_pD3DDevice = NULL;   // Direct3D device.
IDXVAHD_Device          *g_pDXVAHD = NULL;      // DXVA-HD device.
IDXVAHD_VideoProcessor  *g_pDXVAVP = NULL;      // DXVA-HD video processor.
IDirect3DSurface9       *g_pSurface = NULL;     // Video surface.
        
const D3DFORMAT     RENDER_TARGET_FORMAT = D3DFMT_X8R8G8B8;
const D3DFORMAT     VIDEO_FORMAT         = D3DFMT_X8R8G8B8; 
const UINT          VIDEO_FPS            = 60;
const UINT          VIDEO_WIDTH          = 640;
const UINT          VIDEO_HEIGHT         = 480;
```



Per creare un processore video DXVA-HD:

1.  Compilare una struttura [**DXVAHD \_ Content \_ desc**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) con una descrizione del contenuto video. Il driver utilizza queste informazioni come un suggerimento per ottimizzare le funzionalità del processore video. La struttura non contiene una descrizione del formato completo.
    ```C++
        DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

        DXVAHD_CONTENT_DESC desc;

        desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
        desc.InputFrameRate = fps;
        desc.InputWidth = VIDEO_WIDTH;
        desc.InputHeight = VIDEO_HEIGHT;
        desc.OutputFrameRate = fps;
        desc.OutputWidth = VIDEO_WIDTH;
        desc.OutputHeight = VIDEO_HEIGHT;
    ```

    

2.  Chiamare [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) per creare il dispositivo DXVA-HD. Questa funzione restituisce un puntatore all'interfaccia [**del \_ dispositivo IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  Chiamare [**IDXVAHD \_ Device:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps). Questo metodo compila una struttura [**\_ VPDEVCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) con le funzionalità del dispositivo. Se sono necessarie funzionalità di elaborazione video specifiche, ad esempio le chiavi luma o il filtro delle immagini, verificarne la disponibilità usando questa struttura.
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  Verificare se il dispositivo DXVA-HD supporta i formati video di input necessari. L'argomento relativo al [controllo dei formati DXVA-HD supportati](checking-supported-dxva-hd-formats.md) descrive questo passaggio in modo più dettagliato.
5.  Verificare se il dispositivo DXVA-HD supporta il formato di output necessario. La sezione [controllo dei formati DXVA-HD supportati](checking-supported-dxva-hd-formats.md) descrive questo passaggio in modo più dettagliato.
6.  Allocare una matrice di strutture [**\_ VPCAPS di DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) . Il numero di elementi della matrice che deve essere allocato viene fornito dal membro **VideoProcessorCount** della [**struttura \_ VPDEVCAPS di DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) , ottenuto nel passaggio 3.
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  Ogni struttura [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) rappresenta un processore video distinto. È possibile scorrere in ciclo questa matrice per individuare le funzionalità di ogni processore video. La struttura include informazioni sulle funzionalità di conversione della frequenza di deinterlacciamento, telecine e frame del processore video.
8.  Selezionare un processore video da creare. Il membro **VPGuid** della struttura [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contiene un GUID che identifica in modo univoco il processore video. Passare questo GUID al metodo [**\_ Device:: CreateVideoProcessor di IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) . Il metodo restituisce un [**puntatore \_ VideoProcessor IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  Facoltativamente, chiamare [**IDXVAHD \_ Device:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) per creare una matrice di superfici video di input.

Nell'esempio di codice seguente viene illustrata la sequenza completa dei passaggi:


```C++
// Initializes the DXVA-HD video processor.

// NOTE: The following example makes some simplifying assumptions:
//
// 1. There is a single input stream.
// 2. The input frame rate matches the output frame rate.
// 3. No advanced DXVA-HD features are needed, such as luma keying or IVTC.
// 4. The application uses a single input video surface.

HRESULT InitializeDXVAHD()
{
    if (g_pD3DDevice == NULL)
    {
        return E_FAIL;
    }

    HRESULT hr = S_OK;

    IDXVAHD_Device          *pDXVAHD = NULL;
    IDXVAHD_VideoProcessor  *pDXVAVP = NULL;
    IDirect3DSurface9       *pSurf = NULL;

    DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

    DXVAHD_CONTENT_DESC desc;

    desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
    desc.InputFrameRate = fps;
    desc.InputWidth = VIDEO_WIDTH;
    desc.InputHeight = VIDEO_HEIGHT;
    desc.OutputFrameRate = fps;
    desc.OutputWidth = VIDEO_WIDTH;
    desc.OutputHeight = VIDEO_HEIGHT;

#ifdef USE_SOFTWARE_PLUGIN    
    HMODULE hSWPlugin = LoadLibrary(L"C:\\dxvahdsw.dll");

    PDXVAHDSW_Plugin pSWPlugin = (PDXVAHDSW_Plugin)GetProcAddress(hSWPlugin, "DXVAHDSW_Plugin");

    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc,DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        pSWPlugin, &pDXVAHD);
#else
    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        NULL, &pDXVAHD);
#endif
    if (FAILED(hr))
    {
        goto done;
    }

    DXVAHD_VPDEVCAPS caps;

    hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Check whether the device supports the input and output formats.

    hr = CheckInputFormatSupport(pDXVAHD, caps, VIDEO_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CheckOutputFormatSupport(pDXVAHD, caps, RENDER_TARGET_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the VP device.
    hr = CreateVPDevice(pDXVAHD, caps, &pDXVAVP);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );

    if (FAILED(hr))
    {
        goto done;
    }


    g_pDXVAHD = pDXVAHD;
    g_pDXVAHD->AddRef();

    g_pDXVAVP = pDXVAVP;
    g_pDXVAVP->AddRef();

    g_pSurface = pSurf;
    g_pSurface->AddRef();

done:
    SafeRelease(&pDXVAHD);
    SafeRelease(&pDXVAVP);
    SafeRelease(&pSurf);
    return hr;
}
```



La funzione CreateVPDevice Mostra in questo esempio crea il processore video (passaggi 5-7):


```C++
// Creates a DXVA-HD video processor.

HRESULT CreateVPDevice(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    IDXVAHD_VideoProcessor  **ppDXVAVP
    )
{
    // Create the array of video processor caps. 
    
    DXVAHD_VPCAPS *pVPCaps = 
        new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

    if (pVPCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
        caps.VideoProcessorCount, pVPCaps);

    // At this point, an application could loop through the array and examine
    // the capabilities. For purposes of this example, however, we simply
    // create the first video processor in the list.

    if (SUCCEEDED(hr))
    {
        // The VPGuid member contains the GUID that identifies the video 
        // processor.

        hr = pDXVAHD->CreateVideoProcessor(&pVPCaps[0].VPGuid, ppDXVAVP);
    }

    delete [] pVPCaps;
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



