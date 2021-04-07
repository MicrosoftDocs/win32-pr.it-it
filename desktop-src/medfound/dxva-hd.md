---
description: Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749255"
---
# <a name="dxva-hd"></a><span data-ttu-id="225a3-103">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="225a3-103">DXVA-HD</span></span>

<span data-ttu-id="225a3-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="225a3-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <span data-ttu-id="225a3-105">DXVA-HD usa la GPU per eseguire funzioni quali deinterlacciamento, composizione e conversione dello spazio colore.</span><span class="sxs-lookup"><span data-stu-id="225a3-105">DXVA-HD uses the GPU to perform functions such as deinterlacing, compositing, and color-space conversion.</span></span>

<span data-ttu-id="225a3-106">DXVA-HD è simile all' [elaborazione video DXVA](dxva-video-processing.md) (DXVA-VP), ma offre funzionalità avanzate e un modello di elaborazione più semplice.</span><span class="sxs-lookup"><span data-stu-id="225a3-106">DXVA-HD is similar to [DXVA Video Processing](dxva-video-processing.md) (DXVA-VP), but offers enhanced features and a simpler processing model.</span></span> <span data-ttu-id="225a3-107">Grazie a un modello di composizione più flessibile, DXVA-HD è progettato per supportare la nuova generazione di formati ottici HD e standard broadcast.</span><span class="sxs-lookup"><span data-stu-id="225a3-107">By providing a more flexible composition model, DXVA-HD is designed to support the next generation of HD optical formats and broadcast standards.</span></span>

<span data-ttu-id="225a3-108">L'API DXVA-HD richiede un driver di visualizzazione WDDM che supporta l'interfaccia DDI (Device Driver Interface) DXVA-HD o un processore software plug-in.</span><span class="sxs-lookup"><span data-stu-id="225a3-108">The DXVA-HD API requires either a WDDM display driver that supports the DXVA-HD device driver interface (DDI), or a plug-in software processor.</span></span>

-   [<span data-ttu-id="225a3-109">Miglioramenti rispetto a DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="225a3-109">Improvements over DXVA-VP</span></span>](#improvements-over-dxva-vp)
-   [<span data-ttu-id="225a3-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="225a3-110">Related topics</span></span>](#related-topics)

## <a name="improvements-over-dxva-vp"></a><span data-ttu-id="225a3-111">Miglioramenti rispetto a DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="225a3-111">Improvements over DXVA-VP</span></span>

<span data-ttu-id="225a3-112">DXVA-HD espande il set di funzionalità fornite da DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="225a3-112">DXVA-HD expands the set of features provided by DXVA-VP.</span></span> <span data-ttu-id="225a3-113">I miglioramenti includono:</span><span class="sxs-lookup"><span data-stu-id="225a3-113">Enhancements include:</span></span>

-   <span data-ttu-id="225a3-114">Combinazione di RGB e YUV.</span><span class="sxs-lookup"><span data-stu-id="225a3-114">RGB and YUV mixing.</span></span> <span data-ttu-id="225a3-115">Qualsiasi flusso può essere RGB o YUV.</span><span class="sxs-lookup"><span data-stu-id="225a3-115">Any stream can be either RGB or YUV.</span></span> <span data-ttu-id="225a3-116">Non esiste più una distinzione tra il flusso primario e i sottoflussi.</span><span class="sxs-lookup"><span data-stu-id="225a3-116">There is no longer a distinction between the primary stream and the substreams.</span></span>
-   <span data-ttu-id="225a3-117">Deinterlacciamento di più flussi.</span><span class="sxs-lookup"><span data-stu-id="225a3-117">Deinterlacing of multiple streams.</span></span> <span data-ttu-id="225a3-118">Qualsiasi flusso può essere progressivo o interlacciato.</span><span class="sxs-lookup"><span data-stu-id="225a3-118">Any stream can be either progressive or interlaced.</span></span> <span data-ttu-id="225a3-119">Inoltre, la cadenza e la frequenza dei fotogrammi possono variare da un flusso di input a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="225a3-119">Moreover, the cadence and frame rate can can vary from one input stream to the next.</span></span>
-   <span data-ttu-id="225a3-120">Colori di sfondo RGB.</span><span class="sxs-lookup"><span data-stu-id="225a3-120">RGB background colors.</span></span> <span data-ttu-id="225a3-121">In precedenza erano supportati solo i colori di sfondo YUV.</span><span class="sxs-lookup"><span data-stu-id="225a3-121">Previously, only YUV background colors were supported.</span></span>
-   <span data-ttu-id="225a3-122">Chiavi Luma.</span><span class="sxs-lookup"><span data-stu-id="225a3-122">Luma keying.</span></span> <span data-ttu-id="225a3-123">Quando è abilitata la chiave Luma, i valori Luma che rientrano in un intervallo designato diventano trasparenti.</span><span class="sxs-lookup"><span data-stu-id="225a3-123">When luma keying is enabled, luma values that fall within a designated range become transparent.</span></span>
-   <span data-ttu-id="225a3-124">Spostamento dinamico tra modalità di deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="225a3-124">Dynamic switching between deinterlace modes.</span></span>

<span data-ttu-id="225a3-125">DXVA-HD definisce anche alcune funzionalità avanzate che i driver possono supportare.</span><span class="sxs-lookup"><span data-stu-id="225a3-125">DXVA-HD also defines some advanced features that drivers can support.</span></span> <span data-ttu-id="225a3-126">Tuttavia, le applicazioni non devono presupporre che tutti i driver supportino queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="225a3-126">However, applications should not assume that all drivers will support these features.</span></span> <span data-ttu-id="225a3-127">Le funzionalità avanzate includono:</span><span class="sxs-lookup"><span data-stu-id="225a3-127">The advanced features include:</span></span>

-   <span data-ttu-id="225a3-128">Telecine inversa (ad esempio, da 60i a 24p).</span><span class="sxs-lookup"><span data-stu-id="225a3-128">Inverse telecine (for example, 60i to 24p).</span></span>
-   <span data-ttu-id="225a3-129">Conversione della frequenza dei fotogrammi (ad esempio, 24p in 120P).</span><span class="sxs-lookup"><span data-stu-id="225a3-129">Frame-rate conversion (for example, 24p to 120p).</span></span>
-   <span data-ttu-id="225a3-130">Modalità di riempimento alfa.</span><span class="sxs-lookup"><span data-stu-id="225a3-130">Alpha-fill modes.</span></span>
-   <span data-ttu-id="225a3-131">Riduzione del rumore e filtro di miglioramento del perimetro.</span><span class="sxs-lookup"><span data-stu-id="225a3-131">Noise reduction and edge enhancement filtering.</span></span>
-   <span data-ttu-id="225a3-132">Ridimensionamento non lineare Anamorfo.</span><span class="sxs-lookup"><span data-stu-id="225a3-132">Anamorphic non-linear scaling.</span></span>
-   <span data-ttu-id="225a3-133">Extended YCbCr (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="225a3-133">Extended YCbCr (xvYCC).</span></span>

<span data-ttu-id="225a3-134">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="225a3-134">This section contains the following topics.</span></span>

-   [<span data-ttu-id="225a3-135">Creazione di un processore video DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="225a3-135">Creating a DXVA-HD Video Processor</span></span>](creating-a-dxva-hd-video-processor.md)
-   [<span data-ttu-id="225a3-136">Controllo dei formati DXVA-HD supportati</span><span class="sxs-lookup"><span data-stu-id="225a3-136">Checking Supported DXVA-HD Formats</span></span>](checking-supported-dxva-hd-formats.md)
-   [<span data-ttu-id="225a3-137">Creazione di superfici video DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="225a3-137">Creating DXVA-HD Video Surfaces</span></span>](creating-dxva-hd-video-surfaces.md)
-   [<span data-ttu-id="225a3-138">Impostazione di DXVA-stati HD</span><span class="sxs-lookup"><span data-stu-id="225a3-138">Setting DXVA-HD States</span></span>](setting-dxva-hd-states.md)
-   [<span data-ttu-id="225a3-139">Esecuzione di DXVA-HD blit</span><span class="sxs-lookup"><span data-stu-id="225a3-139">Performing the DXVA-HD Blit</span></span>](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a><span data-ttu-id="225a3-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="225a3-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="225a3-141">Accelerazione video DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="225a3-141">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="225a3-142">Esempio di DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="225a3-142">DXVA-HD Sample</span></span>](dxva-hd-sample.md)
</dt> </dl>

 

 



