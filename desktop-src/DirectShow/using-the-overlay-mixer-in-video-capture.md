---
description: Uso del mixer overlay in acquisizione video
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Uso del mixer overlay in acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057831"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a><span data-ttu-id="38984-103">Uso del mixer overlay in acquisizione video</span><span class="sxs-lookup"><span data-stu-id="38984-103">Using the Overlay Mixer in Video Capture</span></span>

<span data-ttu-id="38984-104">Sono disponibili alcuni tipi di video in cui il filtro [renderer video](video-renderer-filter.md) non può essere visualizzato da solo.</span><span class="sxs-lookup"><span data-stu-id="38984-104">There are certain kinds of video that the [Video Renderer](video-renderer-filter.md) filter cannot display by itself.</span></span> <span data-ttu-id="38984-105">In queste situazioni, il renderer video deve funzionare con il filtro [Overlay Mixer](overlay-mixer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="38984-105">In these situations, the Video Renderer must work with the [Overlay Mixer](overlay-mixer-filter.md) filter.</span></span> <span data-ttu-id="38984-106">Il mixer overlay gestisce il rendering, mentre il renderer video gestisce la finestra video.</span><span class="sxs-lookup"><span data-stu-id="38984-106">The Overlay Mixer manages the rendering, while the Video Renderer manages the video window.</span></span> <span data-ttu-id="38984-107">Il mixer overlay è necessario nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="38984-107">The Overlay Mixer is needed in the following situations:</span></span>

-   <span data-ttu-id="38984-108">PIN della porta video (VP).</span><span class="sxs-lookup"><span data-stu-id="38984-108">Video port (VP) pins.</span></span> <span data-ttu-id="38984-109">Se il dispositivo di acquisizione usa una porta video, il mixer della sovrimpressione gestisce la sovrimpressione hardware.</span><span class="sxs-lookup"><span data-stu-id="38984-109">If the capture device uses a video port, the Overlay Mixer manages the hardware overlay.</span></span>
-   <span data-ttu-id="38984-110">Video interlacciato.</span><span class="sxs-lookup"><span data-stu-id="38984-110">Interlaced video.</span></span> <span data-ttu-id="38984-111">Per i video interlacciati, il decodificatore richiede un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , che non è supportato dal renderer video.</span><span class="sxs-lookup"><span data-stu-id="38984-111">For interlaced video, the decoder requires a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format, which the Video Renderer does not support.</span></span>
-   <span data-ttu-id="38984-112">Didascalie chiuse.</span><span class="sxs-lookup"><span data-stu-id="38984-112">Closed captions.</span></span> <span data-ttu-id="38984-113">Il testo della didascalia viene sottoposto a rendering come bitmap a 8 bit per pixel, sovrapposte al video dal mixer sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="38984-113">The caption text is rendered as 8-bits-per-pixel bitmaps, which the Overlay Mixer overlays onto the video.</span></span>

<span data-ttu-id="38984-114">Il metodo **RenderStream** del generatore di grafici di acquisizione inserisce il mixer della sovrimpressione ogni volta che è necessario.</span><span class="sxs-lookup"><span data-stu-id="38984-114">The Capture Graph Builder's **RenderStream** method inserts the Overlay Mixer whenever needed.</span></span> <span data-ttu-id="38984-115">Se si compila il grafo senza usare il generatore di grafici di acquisizione, tuttavia, è necessario verificare la presenza di queste situazioni e inserire il mixer sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="38984-115">If you are building the graph without using the Capture Graph Builder, however, you must check for each of these situations and insert the Overlay Mixer yourself.</span></span>

-   <span data-ttu-id="38984-116">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="38984-116">\[!Important\]</span></span>  
    > <span data-ttu-id="38984-117">Se il dispositivo ha un pin VP, è necessario connettere il mixer overlay anche se non è necessaria la funzionalità di anteprima nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38984-117">If the device has a VP pin, you must connect the Overlay Mixer even if you do not need preview functionality in your application.</span></span> <span data-ttu-id="38984-118">Con una porta video, il dispositivo di acquisizione Invia sempre i dati video alla sovrapposizione hardware, quindi il mixer overlay è sempre necessario.</span><span class="sxs-lookup"><span data-stu-id="38984-118">With a video port, the capture device always sends the video data to the hardware overlay, so the Overlay Mixer is always needed.</span></span>

     

<span data-ttu-id="38984-119">I filtri renderer video mixing (VMR-7 e VMR-9) supportano entrambi i video interlacciati e possono combinare bitmap didascalie chiuse nel video principale.</span><span class="sxs-lookup"><span data-stu-id="38984-119">The Video Mixing Renderer filters (VMR-7 and VMR-9) both support interlaced video, and are able to mix closed caption bitmaps onto the primary video.</span></span> <span data-ttu-id="38984-120">Se si usa VMR per questi scenari, non è necessario usare il mixer overlay.</span><span class="sxs-lookup"><span data-stu-id="38984-120">If you are using the VMR for those scenarios, then you do not need to use the Overlay Mixer.</span></span> <span data-ttu-id="38984-121">VMR-9 non supporta le connessioni pin VP.</span><span class="sxs-lookup"><span data-stu-id="38984-121">The VMR-9 does not support VP pin connections.</span></span> <span data-ttu-id="38984-122">VMR-7 supporta le connessioni pin VP tramite il filtro gestione porta video.</span><span class="sxs-lookup"><span data-stu-id="38984-122">The VMR-7 supports VP pin connections through the Video Port Manager filter.</span></span> <span data-ttu-id="38984-123">Tuttavia, è possibile che alcuni driver non funzionino correttamente con il gestore della porta video.</span><span class="sxs-lookup"><span data-stu-id="38984-123">However, you may find that some drivers do not work correctly with the Video Port Manager.</span></span> <span data-ttu-id="38984-124">Per questo motivo, il mixer overlay è ancora consigliato per i pin VP.</span><span class="sxs-lookup"><span data-stu-id="38984-124">For that reason, the Overlay Mixer is still recommended for VP pins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38984-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38984-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38984-126">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="38984-126">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="38984-127">PIN della porta video</span><span class="sxs-lookup"><span data-stu-id="38984-127">Video Port Pins</span></span>](video-port-pins.md)
</dt> <dt>

[<span data-ttu-id="38984-128">Tipo di formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="38984-128">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
</dt> </dl>

 

 



