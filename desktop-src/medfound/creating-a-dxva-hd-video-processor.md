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
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="c6966-103">Creazione di un processore video DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="c6966-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="c6966-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) usa due interfacce primarie:</span><span class="sxs-lookup"><span data-stu-id="c6966-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="c6966-105">[**IDXVAHD \_ Dispositivo**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span><span class="sxs-lookup"><span data-stu-id="c6966-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="c6966-106">Rappresenta il dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="c6966-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="c6966-107">Usare questa interfaccia per eseguire una query sulle funzionalità del dispositivo e creare il processore video.</span><span class="sxs-lookup"><span data-stu-id="c6966-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="c6966-108">[**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span><span class="sxs-lookup"><span data-stu-id="c6966-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="c6966-109">Rappresenta un set di funzionalità di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="c6966-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="c6966-110">Usare questa interfaccia per eseguire il blit di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="c6966-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="c6966-111">Nel codice seguente vengono presupposte le seguenti variabili globali:</span><span class="sxs-lookup"><span data-stu-id="c6966-111">In the code that follows, the following global variables are assumed:</span></span>


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



<span data-ttu-id="c6966-112">Per creare un processore video DXVA-HD:</span><span class="sxs-lookup"><span data-stu-id="c6966-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="c6966-113">Compilare una struttura [**DXVAHD \_ Content \_ desc**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) con una descrizione del contenuto video.</span><span class="sxs-lookup"><span data-stu-id="c6966-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="c6966-114">Il driver utilizza queste informazioni come un suggerimento per ottimizzare le funzionalità del processore video.</span><span class="sxs-lookup"><span data-stu-id="c6966-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="c6966-115">La struttura non contiene una descrizione del formato completo.</span><span class="sxs-lookup"><span data-stu-id="c6966-115">The structure does not contain a complete format description.</span></span>
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

    

2.  <span data-ttu-id="c6966-116">Chiamare [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) per creare il dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="c6966-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="c6966-117">Questa funzione restituisce un puntatore all'interfaccia [**del \_ dispositivo IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .</span><span class="sxs-lookup"><span data-stu-id="c6966-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="c6966-118">Chiamare [**IDXVAHD \_ Device:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span><span class="sxs-lookup"><span data-stu-id="c6966-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="c6966-119">Questo metodo compila una struttura [**\_ VPDEVCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) con le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6966-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="c6966-120">Se sono necessarie funzionalità di elaborazione video specifiche, ad esempio le chiavi luma o il filtro delle immagini, verificarne la disponibilità usando questa struttura.</span><span class="sxs-lookup"><span data-stu-id="c6966-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="c6966-121">Verificare se il dispositivo DXVA-HD supporta i formati video di input necessari.</span><span class="sxs-lookup"><span data-stu-id="c6966-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="c6966-122">L'argomento relativo al [controllo dei formati DXVA-HD supportati](checking-supported-dxva-hd-formats.md) descrive questo passaggio in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="c6966-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="c6966-123">Verificare se il dispositivo DXVA-HD supporta il formato di output necessario.</span><span class="sxs-lookup"><span data-stu-id="c6966-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="c6966-124">La sezione [controllo dei formati DXVA-HD supportati](checking-supported-dxva-hd-formats.md) descrive questo passaggio in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="c6966-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="c6966-125">Allocare una matrice di strutture [**\_ VPCAPS di DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) .</span><span class="sxs-lookup"><span data-stu-id="c6966-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="c6966-126">Il numero di elementi della matrice che deve essere allocato viene fornito dal membro **VideoProcessorCount** della [**struttura \_ VPDEVCAPS di DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) , ottenuto nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="c6966-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="c6966-127">Ogni struttura [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) rappresenta un processore video distinto.</span><span class="sxs-lookup"><span data-stu-id="c6966-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="c6966-128">È possibile scorrere in ciclo questa matrice per individuare le funzionalità di ogni processore video.</span><span class="sxs-lookup"><span data-stu-id="c6966-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="c6966-129">La struttura include informazioni sulle funzionalità di conversione della frequenza di deinterlacciamento, telecine e frame del processore video.</span><span class="sxs-lookup"><span data-stu-id="c6966-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="c6966-130">Selezionare un processore video da creare.</span><span class="sxs-lookup"><span data-stu-id="c6966-130">Select a video processor to create.</span></span> <span data-ttu-id="c6966-131">Il membro **VPGuid** della struttura [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contiene un GUID che identifica in modo univoco il processore video.</span><span class="sxs-lookup"><span data-stu-id="c6966-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="c6966-132">Passare questo GUID al metodo [**\_ Device:: CreateVideoProcessor di IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="c6966-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="c6966-133">Il metodo restituisce un [**puntatore \_ VideoProcessor IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="c6966-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="c6966-134">Facoltativamente, chiamare [**IDXVAHD \_ Device:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) per creare una matrice di superfici video di input.</span><span class="sxs-lookup"><span data-stu-id="c6966-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="c6966-135">Nell'esempio di codice seguente viene illustrata la sequenza completa dei passaggi:</span><span class="sxs-lookup"><span data-stu-id="c6966-135">The following code example shows the complete sequence of steps:</span></span>


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



<span data-ttu-id="c6966-136">La funzione CreateVPDevice Mostra in questo esempio crea il processore video (passaggi 5-7):</span><span class="sxs-lookup"><span data-stu-id="c6966-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c6966-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6966-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6966-138">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="c6966-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



