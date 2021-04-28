---
description: Creazione di un processore video DXVA-HD
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Creazione di un processore video DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89c5a361335f83296eec538a5a6a710b9e19604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102599"
---
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="70a02-103">Creazione di un processore video DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="70a02-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="70a02-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) usa due interfacce principali:</span><span class="sxs-lookup"><span data-stu-id="70a02-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="70a02-105">[**IDXVAHD \_ Dispositivo**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span><span class="sxs-lookup"><span data-stu-id="70a02-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="70a02-106">Rappresenta il dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="70a02-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="70a02-107">Usare questa interfaccia per eseguire query sulle funzionalità del dispositivo e creare il processore video.</span><span class="sxs-lookup"><span data-stu-id="70a02-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="70a02-108">[**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span><span class="sxs-lookup"><span data-stu-id="70a02-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="70a02-109">Rappresenta un set di funzionalità di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="70a02-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="70a02-110">Usare questa interfaccia per eseguire il blit di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="70a02-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="70a02-111">Nel codice seguente vengono utilizzate le variabili globali seguenti:</span><span class="sxs-lookup"><span data-stu-id="70a02-111">In the code that follows, the following global variables are assumed:</span></span>


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



<span data-ttu-id="70a02-112">Per creare un processore video DXVA-HD:</span><span class="sxs-lookup"><span data-stu-id="70a02-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="70a02-113">Compilare una [**struttura DXVAHD \_ CONTENT \_ DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) con una descrizione del contenuto video.</span><span class="sxs-lookup"><span data-stu-id="70a02-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="70a02-114">Il driver usa queste informazioni come suggerimento per ottimizzare le funzionalità del processore video.</span><span class="sxs-lookup"><span data-stu-id="70a02-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="70a02-115">La struttura non contiene una descrizione del formato completa.</span><span class="sxs-lookup"><span data-stu-id="70a02-115">The structure does not contain a complete format description.</span></span>
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

    

2.  <span data-ttu-id="70a02-116">Chiamare [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) per creare il dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="70a02-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="70a02-117">Questa funzione restituisce un puntatore all'interfaccia del dispositivo [**IDXVAHD. \_**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)</span><span class="sxs-lookup"><span data-stu-id="70a02-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="70a02-118">Chiamare [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span><span class="sxs-lookup"><span data-stu-id="70a02-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="70a02-119">Questo metodo compila una struttura [**\_ VPDEVCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) con le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70a02-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="70a02-120">Se sono necessarie funzionalità di elaborazione video specifiche, ad esempio la chiave luma o il filtro delle immagini, verificarne la disponibilità usando questa struttura.</span><span class="sxs-lookup"><span data-stu-id="70a02-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="70a02-121">Controllare se il dispositivo DXVA-HD supporta i formati video di input necessari.</span><span class="sxs-lookup"><span data-stu-id="70a02-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="70a02-122">[L'argomento Controllo dei formati DXVA-HD](checking-supported-dxva-hd-formats.md) supportati descrive questo passaggio in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="70a02-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="70a02-123">Controllare se il dispositivo DXVA-HD supporta il formato di output necessario.</span><span class="sxs-lookup"><span data-stu-id="70a02-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="70a02-124">La sezione [Controllo dei formati DXVA-HD](checking-supported-dxva-hd-formats.md) supportati descrive questo passaggio in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="70a02-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="70a02-125">Allocare una matrice [**di strutture \_ VPCAPS DXVAHD.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps)</span><span class="sxs-lookup"><span data-stu-id="70a02-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="70a02-126">Il numero di elementi della matrice che devono essere allocati è dato dal membro **VideoProcessorCount** della struttura [**\_ VPDEVCAPS DXVAHD,**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) ottenuto nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="70a02-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="70a02-127">Ogni [**struttura \_ VPCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) rappresenta un processore video distinto.</span><span class="sxs-lookup"><span data-stu-id="70a02-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="70a02-128">È possibile scorrere questa matrice per individuare le funzionalità di ogni processore video.</span><span class="sxs-lookup"><span data-stu-id="70a02-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="70a02-129">La struttura include informazioni sulle funzionalità di deinterlacing, telecine e conversione della frequenza fotogrammi del processore video.</span><span class="sxs-lookup"><span data-stu-id="70a02-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="70a02-130">Selezionare un processore video da creare.</span><span class="sxs-lookup"><span data-stu-id="70a02-130">Select a video processor to create.</span></span> <span data-ttu-id="70a02-131">Il **membro VPGuid** della struttura [**\_ VPCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contiene un GUID che identifica in modo univoco il processore video.</span><span class="sxs-lookup"><span data-stu-id="70a02-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="70a02-132">Passare questo GUID al [**metodo IDXVAHD \_ Device::CreateVideoProcessor.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor)</span><span class="sxs-lookup"><span data-stu-id="70a02-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="70a02-133">Il metodo restituisce un [**puntatore IDXVAHD \_ VideoProcessor.**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)</span><span class="sxs-lookup"><span data-stu-id="70a02-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="70a02-134">Facoltativamente, chiamare [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) per creare una matrice di superfici video di input.</span><span class="sxs-lookup"><span data-stu-id="70a02-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="70a02-135">L'esempio di codice seguente illustra la sequenza completa di passaggi:</span><span class="sxs-lookup"><span data-stu-id="70a02-135">The following code example shows the complete sequence of steps:</span></span>


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



<span data-ttu-id="70a02-136">La funzione CreateVPDevice illustrata in questo esempio crea il processore video (passaggi da 5 a 7):</span><span class="sxs-lookup"><span data-stu-id="70a02-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="70a02-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70a02-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70a02-138">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="70a02-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



