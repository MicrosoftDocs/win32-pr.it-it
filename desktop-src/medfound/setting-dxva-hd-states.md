---
description: Impostazione degli stati DXVA-HD
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Impostazione degli stati DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092699"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="ea39f-103">Impostazione degli stati DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ea39f-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="ea39f-104">Durante l'elaborazione video, il dispositivo Microsoft DirectX Video Acceleration High Definition (DXVA-HD) mantiene uno stato permanente da un fotogramma a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="ea39f-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="ea39f-105">Ogni stato ha un valore predefinito documentato.</span><span class="sxs-lookup"><span data-stu-id="ea39f-105">Each state has a documented default.</span></span> <span data-ttu-id="ea39f-106">Dopo aver configurato il dispositivo, impostare gli stati da modificare rispetto alle impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="ea39f-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="ea39f-107">Prima di elaborare ogni frame, aggiornare gli stati che devono cambiare.</span><span class="sxs-lookup"><span data-stu-id="ea39f-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="ea39f-108">Questa progettazione è diversa da DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="ea39f-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="ea39f-109">In DXVA-VP l'applicazione deve specificare tutti i parametri VP con ogni frame.</span><span class="sxs-lookup"><span data-stu-id="ea39f-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="ea39f-110">Gli stati del dispositivo rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="ea39f-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="ea39f-111">*Gli stati* di flusso applicano ogni flusso di input separatamente.</span><span class="sxs-lookup"><span data-stu-id="ea39f-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="ea39f-112">È possibile applicare impostazioni diverse a ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="ea39f-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="ea39f-113">*Gli stati blit* si applicano a livello globale all'intero blit di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="ea39f-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="ea39f-114">Vengono definiti gli stati del flusso seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea39f-114">The following stream states are defined.</span></span>



| <span data-ttu-id="ea39f-115">Stato del flusso</span><span class="sxs-lookup"><span data-stu-id="ea39f-115">Stream State</span></span>                                   | <span data-ttu-id="ea39f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea39f-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea39f-117">**DXVAHD \_ STREAM \_ STATE \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ea39f-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="ea39f-118">Formato video di input.</span><span class="sxs-lookup"><span data-stu-id="ea39f-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="ea39f-119">**FORMATO FRAME STATO FLUSSO DXVAHD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ea39f-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="ea39f-120">Interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="ea39f-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="ea39f-121">**SPAZIO COLORE DI \_ \_ \_ INPUT \_ \_ DELLO STATO DEL FLUSSO DXVAHD**</span><span class="sxs-lookup"><span data-stu-id="ea39f-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="ea39f-122">Spazio colore di input.</span><span class="sxs-lookup"><span data-stu-id="ea39f-122">Input color space.</span></span> <span data-ttu-id="ea39f-123">Questo stato specifica l'intervallo di colori RGB e la matrice di trasferimento YCbCr per il flusso di input.</span><span class="sxs-lookup"><span data-stu-id="ea39f-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="ea39f-124">**FREQUENZA DI OUTPUT DELLO \_ STATO \_ DEL FLUSSO \_ \_ DXVAHD**</span><span class="sxs-lookup"><span data-stu-id="ea39f-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="ea39f-125">Frequenza dei fotogrammi di output.</span><span class="sxs-lookup"><span data-stu-id="ea39f-125">Output frame rate.</span></span> <span data-ttu-id="ea39f-126">Questo stato controlla la conversione della frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="ea39f-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="ea39f-127">**DXVAHD \_ STREAM \_ STATE \_ SOURCE \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="ea39f-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="ea39f-128">Rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="ea39f-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="ea39f-129">**DXVAHD \_ STREAM \_ STATE \_ DESTINATION \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="ea39f-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="ea39f-130">Rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea39f-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="ea39f-131">**DXVAHD \_ STREAM \_ STATE \_ ALPHA**</span><span class="sxs-lookup"><span data-stu-id="ea39f-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="ea39f-132">Alfa planare.</span><span class="sxs-lookup"><span data-stu-id="ea39f-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="ea39f-133">**TAVOLOZZA DELLO STATO DEL FLUSSO DXVAHD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ea39f-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="ea39f-134">Tavolozza.</span><span class="sxs-lookup"><span data-stu-id="ea39f-134">Color palette.</span></span> <span data-ttu-id="ea39f-135">Questo stato si applica solo ai formati di input con svasato.</span><span class="sxs-lookup"><span data-stu-id="ea39f-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="ea39f-136">**CHIAVE LUMA DELLO \_ STATO DEL FLUSSO \_ \_ DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="ea39f-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="ea39f-137">Tasto Luma.</span><span class="sxs-lookup"><span data-stu-id="ea39f-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="ea39f-138">**PROPORZIONI DELLO STATO DEL FLUSSO DXVAHD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ea39f-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="ea39f-139">Proporzioni pixel.</span><span class="sxs-lookup"><span data-stu-id="ea39f-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="ea39f-140">**DXVAHD \_ STREAM \_ STATE \_ FILTER \_ Xxxx**</span><span class="sxs-lookup"><span data-stu-id="ea39f-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="ea39f-141">Impostazioni del filtro delle immagini.</span><span class="sxs-lookup"><span data-stu-id="ea39f-141">Image filter settings.</span></span> <span data-ttu-id="ea39f-142">Il driver può supportare luminosità, contrasto e altri filtri di immagine.</span><span class="sxs-lookup"><span data-stu-id="ea39f-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="ea39f-143">Sono definiti gli stati di blit seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea39f-143">The following blit states are defined:</span></span>



| <span data-ttu-id="ea39f-144">Stato blit</span><span class="sxs-lookup"><span data-stu-id="ea39f-144">Blit State</span></span>                                   | <span data-ttu-id="ea39f-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea39f-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ea39f-146">**DXVAHD \_ BLT \_ STATE \_ TARGET \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="ea39f-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="ea39f-147">Rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea39f-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="ea39f-148">**COLORE DI SFONDO DELLO STATO BLT DXVAHD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ea39f-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="ea39f-149">Colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="ea39f-149">Background color.</span></span>                                                            |
| <span data-ttu-id="ea39f-150">**SPAZIO COLORE DI OUTPUT DELLO STATO BLT DXVAHD \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ea39f-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="ea39f-151">Spazio colore di output.</span><span class="sxs-lookup"><span data-stu-id="ea39f-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="ea39f-152">**DXVAHD \_ BLT \_ STATE \_ ALPHA \_ FILL**</span><span class="sxs-lookup"><span data-stu-id="ea39f-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="ea39f-153">Modalità di riempimento alfa.</span><span class="sxs-lookup"><span data-stu-id="ea39f-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="ea39f-154">**DXVAHD \_ BLT \_ STATE \_ CONSTRICTION**</span><span class="sxs-lookup"><span data-stu-id="ea39f-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="ea39f-155">Costrizione.</span><span class="sxs-lookup"><span data-stu-id="ea39f-155">Constriction.</span></span> <span data-ttu-id="ea39f-156">Questo stato controlla se il dispositivo sottocampiona l'output.</span><span class="sxs-lookup"><span data-stu-id="ea39f-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="ea39f-157">Per impostare uno stato del flusso, chiamare il [**metodo IDXVAHD \_ VideoProcessor::SetVideoProcessStreamState.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate)</span><span class="sxs-lookup"><span data-stu-id="ea39f-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="ea39f-158">Per impostare uno stato blit, chiamare il [**metodo IDXVAHD \_ VideoProcessor::SetVideoProcessBltState.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate)</span><span class="sxs-lookup"><span data-stu-id="ea39f-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="ea39f-159">In entrambi questi metodi, un valore di enumerazione specifica lo stato da impostare.</span><span class="sxs-lookup"><span data-stu-id="ea39f-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="ea39f-160">I dati sullo stato vengono dati usando una struttura di dati specifica dello stato, di cui l'applicazione esegue il cast in un **tipo void. \***</span><span class="sxs-lookup"><span data-stu-id="ea39f-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="ea39f-161">L'esempio di codice seguente imposta il formato di input e il rettangolo di destinazione per il flusso 0 e imposta il colore di sfondo su nero.</span><span class="sxs-lookup"><span data-stu-id="ea39f-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ea39f-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea39f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea39f-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ea39f-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



