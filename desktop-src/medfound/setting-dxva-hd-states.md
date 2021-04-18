---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Impostazione di DXVA-stati HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308999"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="06040-103">Impostazione di DXVA-stati HD</span><span class="sxs-lookup"><span data-stu-id="06040-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="06040-104">Durante l'elaborazione video, il dispositivo Microsoft DirectX Video Acceleration High Definition (DXVA-HD) mantiene uno stato persistente da un fotogramma a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="06040-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="06040-105">Ogni stato ha un valore predefinito documentato.</span><span class="sxs-lookup"><span data-stu-id="06040-105">Each state has a documented default.</span></span> <span data-ttu-id="06040-106">Dopo aver configurato il dispositivo, impostare gli Stati che si desidera modificare rispetto alle impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="06040-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="06040-107">Prima di elaborare ogni frame, aggiornare gli Stati che devono essere modificati.</span><span class="sxs-lookup"><span data-stu-id="06040-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="06040-108">Questa progettazione è diversa da DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="06040-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="06040-109">In DXVA-VP, l'applicazione deve specificare tutti i parametri VP con ciascun frame.</span><span class="sxs-lookup"><span data-stu-id="06040-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="06040-110">Gli Stati del dispositivo rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="06040-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="06040-111">Gli Stati del *flusso* applicano ogni flusso di input separatamente.</span><span class="sxs-lookup"><span data-stu-id="06040-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="06040-112">È possibile applicare impostazioni diverse a ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="06040-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="06040-113">Gli stati *blit* si applicano globalmente all'intera blit di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="06040-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="06040-114">Vengono definiti gli Stati di flusso seguenti.</span><span class="sxs-lookup"><span data-stu-id="06040-114">The following stream states are defined.</span></span>



| <span data-ttu-id="06040-115">Stato del flusso</span><span class="sxs-lookup"><span data-stu-id="06040-115">Stream State</span></span>                                   | <span data-ttu-id="06040-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06040-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06040-117">**\_ \_ D3DFORMAT stato flusso \_ DXVAHD**</span><span class="sxs-lookup"><span data-stu-id="06040-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="06040-118">Formato video di input.</span><span class="sxs-lookup"><span data-stu-id="06040-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="06040-119">**\_ \_ formato frame dello stato del flusso DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06040-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="06040-120">Interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="06040-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="06040-121">**\_ \_ \_ \_ spazio colore input stato flusso \_ DXVAHD**</span><span class="sxs-lookup"><span data-stu-id="06040-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="06040-122">Spazio colore di input.</span><span class="sxs-lookup"><span data-stu-id="06040-122">Input color space.</span></span> <span data-ttu-id="06040-123">Questo stato specifica l'intervallo di colori RGB e la matrice di trasferimento YCbCr per il flusso di input.</span><span class="sxs-lookup"><span data-stu-id="06040-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="06040-124">**\_frequenza di \_ output dello stato del flusso \_ DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="06040-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="06040-125">Frequenza del frame di output.</span><span class="sxs-lookup"><span data-stu-id="06040-125">Output frame rate.</span></span> <span data-ttu-id="06040-126">Questo stato controlla la conversione della frequenza del frame.</span><span class="sxs-lookup"><span data-stu-id="06040-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="06040-127">**\_ \_ \_ Rect origine stato flusso \_ DXVAHD**</span><span class="sxs-lookup"><span data-stu-id="06040-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="06040-128">Rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="06040-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="06040-129">**\_ \_ \_ Rect destinazione stato flusso \_ DXVAHD**</span><span class="sxs-lookup"><span data-stu-id="06040-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="06040-130">Rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="06040-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="06040-131">**\_ \_ alfa stato flusso \_ DXVAHD**</span><span class="sxs-lookup"><span data-stu-id="06040-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="06040-132">Alfa planare.</span><span class="sxs-lookup"><span data-stu-id="06040-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="06040-133">**\_ \_ tavolozza dello stato del flusso DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="06040-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="06040-134">Tavolozza dei colori.</span><span class="sxs-lookup"><span data-stu-id="06040-134">Color palette.</span></span> <span data-ttu-id="06040-135">Questo stato è valido solo per i formati di input pallettizzati.</span><span class="sxs-lookup"><span data-stu-id="06040-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="06040-136">**\_ \_ chiave Luma dello stato del flusso DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06040-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="06040-137">Chiave Luma.</span><span class="sxs-lookup"><span data-stu-id="06040-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="06040-138">**proporzioni \_ \_ dello stato del flusso DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06040-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="06040-139">Proporzioni pixel.</span><span class="sxs-lookup"><span data-stu-id="06040-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="06040-140">**\_ \_ Filtro stato flusso \_ DXVAHD \_ xxxx**</span><span class="sxs-lookup"><span data-stu-id="06040-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="06040-141">Impostazioni filtro immagine.</span><span class="sxs-lookup"><span data-stu-id="06040-141">Image filter settings.</span></span> <span data-ttu-id="06040-142">Il driver può supportare la luminosità, il contrasto e altri filtri immagine.</span><span class="sxs-lookup"><span data-stu-id="06040-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="06040-143">Sono definiti gli Stati blit seguenti:</span><span class="sxs-lookup"><span data-stu-id="06040-143">The following blit states are defined:</span></span>



| <span data-ttu-id="06040-144">Stato blit</span><span class="sxs-lookup"><span data-stu-id="06040-144">Blit State</span></span>                                   | <span data-ttu-id="06040-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06040-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="06040-146">**DXVAHD \_ \_ destinazione stato \_ BLT \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="06040-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="06040-147">Rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="06040-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="06040-148">**\_colore di \_ \_ sfondo stato BLT DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="06040-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="06040-149">Colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="06040-149">Background color.</span></span>                                                            |
| <span data-ttu-id="06040-150">**\_ \_ \_ spazio colore di output dello stato \_ di DXVAHD BLT \_**</span><span class="sxs-lookup"><span data-stu-id="06040-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="06040-151">Spazio colore di output.</span><span class="sxs-lookup"><span data-stu-id="06040-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="06040-152">**\_ \_ \_ riempimento alfa stato DXVAHD \_ BLT**</span><span class="sxs-lookup"><span data-stu-id="06040-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="06040-153">Modalità di riempimento alfa.</span><span class="sxs-lookup"><span data-stu-id="06040-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="06040-154">**\_ \_ limitazione dello stato del BLT DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="06040-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="06040-155">Limitazioni.</span><span class="sxs-lookup"><span data-stu-id="06040-155">Constriction.</span></span> <span data-ttu-id="06040-156">Questo stato controlla se il dispositivo downsampling delle l'output.</span><span class="sxs-lookup"><span data-stu-id="06040-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="06040-157">Per impostare lo stato di un flusso, chiamare il metodo [**IDXVAHD \_ VideoProcessor:: SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) .</span><span class="sxs-lookup"><span data-stu-id="06040-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="06040-158">Per impostare uno stato blit, chiamare il metodo [**IDXVAHD \_ VideoProcessor:: SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) .</span><span class="sxs-lookup"><span data-stu-id="06040-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="06040-159">In entrambi i metodi, un valore di enumerazione specifica lo stato da impostare.</span><span class="sxs-lookup"><span data-stu-id="06040-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="06040-160">I dati relativi allo stato vengono forniti utilizzando una struttura di dati specifica dello stato, a cui l'applicazione esegue il cast a un tipo **void \*** .</span><span class="sxs-lookup"><span data-stu-id="06040-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="06040-161">Nell'esempio di codice seguente vengono impostati il formato di input e il rettangolo di destinazione per il flusso 0 e il colore di sfondo viene impostato su nero.</span><span class="sxs-lookup"><span data-stu-id="06040-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="06040-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06040-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06040-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="06040-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



