---
description: Informazioni sui video digitali in DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Informazioni sui video digitali in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569259"
---
# <a name="about-digital-video-in-directshow"></a><span data-ttu-id="d4a47-103">Informazioni sui video digitali in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d4a47-103">About Digital Video in DirectShow</span></span>

<span data-ttu-id="d4a47-104">Il video digitale (DV) può essere acquisito da una videocamera DV, archiviato in un file nel computer dell'utente o archiviato su nastro utilizzando un videoregistratore (video tape registrar).</span><span class="sxs-lookup"><span data-stu-id="d4a47-104">Digital video (DV) can be captured from a DV camera, stored in a file on the user's computer, or stored on tape using a video tape recorder (VTR).</span></span> <span data-ttu-id="d4a47-105">Pertanto, le operazioni che un'applicazione può eseguire su un flusso DV includono:</span><span class="sxs-lookup"><span data-stu-id="d4a47-105">Thus, the operations that an application might perform on a DV stream include:</span></span>

-   <span data-ttu-id="d4a47-106">Acquisisci video live da una videocamera DV.</span><span class="sxs-lookup"><span data-stu-id="d4a47-106">Capture live video from a DV camera.</span></span>
-   <span data-ttu-id="d4a47-107">Trasmettere i dati DV dal nastro VTR al computer.</span><span class="sxs-lookup"><span data-stu-id="d4a47-107">Transmit DV data from VTR tape to the computer.</span></span>
-   <span data-ttu-id="d4a47-108">Trasmettere i dati DV dal computer al VTR.</span><span class="sxs-lookup"><span data-stu-id="d4a47-108">Transmit DV data from the computer to the VTR.</span></span>
-   <span data-ttu-id="d4a47-109">Leggere i dati DV da un file.</span><span class="sxs-lookup"><span data-stu-id="d4a47-109">Read DV data from a file.</span></span>
-   <span data-ttu-id="d4a47-110">Scrive i dati DV in un file.</span><span class="sxs-lookup"><span data-stu-id="d4a47-110">Write DV data to a file.</span></span>
-   <span data-ttu-id="d4a47-111">Eseguire il rendering dell'audio e del video in un flusso DV.</span><span class="sxs-lookup"><span data-stu-id="d4a47-111">Render the audio and video in a DV stream.</span></span>

<span data-ttu-id="d4a47-112">DirectShow fornisce i filtri DV seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4a47-112">DirectShow provides the following DV filters:</span></span>

-   <span data-ttu-id="d4a47-113">[Driver Msdv](msdv-driver.md).</span><span class="sxs-lookup"><span data-stu-id="d4a47-113">[MSDV Driver](msdv-driver.md).</span></span> <span data-ttu-id="d4a47-114">Il driver MSDV controlla un dispositivo DV, ad esempio una videocamera.</span><span class="sxs-lookup"><span data-stu-id="d4a47-114">The MSDV driver controls a DV device, such as a camcorder.</span></span> <span data-ttu-id="d4a47-115">Il dispositivo può avere una sottounità della fotocamera e un'unità secondaria VTR; MSDV controlla entrambe le sottounità.</span><span class="sxs-lookup"><span data-stu-id="d4a47-115">The device may have a camera subunit and a VTR subunit; MSDV controls both subunits.</span></span> <span data-ttu-id="d4a47-116">Il driver MSDV viene visualizzato come filtro DirectShow per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d4a47-116">The MSDV driver appears to applications as a DirectShow filter.</span></span>
-   <span data-ttu-id="d4a47-117">Filtro [barra di divisione DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d4a47-117">[DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="d4a47-118">I frame DV contengono audio e video nello stesso frame.</span><span class="sxs-lookup"><span data-stu-id="d4a47-118">DV frames contain audio and video in the same frame.</span></span> <span data-ttu-id="d4a47-119">Il filtro Splitter DV estrae i dati audio e li restituisce come uno o due flussi audio.</span><span class="sxs-lookup"><span data-stu-id="d4a47-119">The DV Splitter filter extracts the audio data and outputs it as one or two audio streams.</span></span> <span data-ttu-id="d4a47-120">Restituisce i dati originali come flusso video DV separato.</span><span class="sxs-lookup"><span data-stu-id="d4a47-120">It outputs the original data as a separate DV video stream.</span></span>
-   <span data-ttu-id="d4a47-121">Filtro [decodificatore video DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d4a47-121">[DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span> <span data-ttu-id="d4a47-122">Decodifica il video DV in un video non compresso.</span><span class="sxs-lookup"><span data-stu-id="d4a47-122">Decodes DV video into uncompressed video.</span></span>
-   <span data-ttu-id="d4a47-123">Filtro [codificatore video DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d4a47-123">[DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span> <span data-ttu-id="d4a47-124">Codifica il video non compresso in un video con codifica DV.</span><span class="sxs-lookup"><span data-stu-id="d4a47-124">Encodes uncompressed video to DV-encoded video.</span></span>
-   <span data-ttu-id="d4a47-125">[Muxer DV](dv-muxer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d4a47-125">[DV Muxer](dv-muxer-filter.md).</span></span> <span data-ttu-id="d4a47-126">Combina un flusso video DV con uno o due flussi audio, per creare un singolo flusso DV con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="d4a47-126">Combines a DV video stream with one or two audio streams, to create a single interleaved DV stream.</span></span>

<span data-ttu-id="d4a47-127">La barra di divisione DV e il decodificatore video DV interagiscono.</span><span class="sxs-lookup"><span data-stu-id="d4a47-127">The DV Splitter and DV Video Decoder work together.</span></span> <span data-ttu-id="d4a47-128">Il separatore acquisisce il flusso con interfoliazione e genera flussi video audio e DV distinti.</span><span class="sxs-lookup"><span data-stu-id="d4a47-128">The splitter takes the interleaved stream and outputs separate audio and DV video streams.</span></span> <span data-ttu-id="d4a47-129">Il decodificatore converte il video DV in un video non compresso.</span><span class="sxs-lookup"><span data-stu-id="d4a47-129">The decoder converts the DV video to uncompressed video.</span></span> <span data-ttu-id="d4a47-130">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="d4a47-130">The following image illustrates this process.</span></span>

![Splitter DV e decoder DV](images/dv-filters1.png)

<span data-ttu-id="d4a47-132">Il codificatore video DV e il muxer DV invertino il processo: il codificatore converte il video non compresso in video DV e Mux combina audio e video DV per creare un singolo flusso Interleaved, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="d4a47-132">The DV Video Encoder and the DV Muxer reverse the process: The encoder converts uncompressed video to DV video, and the mux combines audio and DV video to create a single interleaved stream, as shown in the following diagram.</span></span>

![codificatore DV e muxer DV](images/dv-filters2.png)

## <a name="related-topics"></a><span data-ttu-id="d4a47-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4a47-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4a47-135">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d4a47-135">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



