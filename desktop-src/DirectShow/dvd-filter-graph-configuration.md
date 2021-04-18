---
description: Configurazione del grafico del filtro DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configurazione del grafico del filtro DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522402"
---
# <a name="dvd-filter-graph-configuration"></a><span data-ttu-id="3508c-103">Configurazione del grafico del filtro DVD</span><span class="sxs-lookup"><span data-stu-id="3508c-103">DVD Filter Graph Configuration</span></span>

<span data-ttu-id="3508c-104">In questa sezione vengono descritte le varie configurazioni del grafico filtro per la riproduzione DVD in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3508c-104">This section describes the various filter graph configurations for DVD playback in DirectShow.</span></span> <span data-ttu-id="3508c-105">Questi diagrammi vengono forniti principalmente per riferimento.</span><span class="sxs-lookup"><span data-stu-id="3508c-105">These diagrams are provided mainly for reference.</span></span> <span data-ttu-id="3508c-106">Il navigatore DVD compila il grafo, quindi in generale non è necessario comprendere i dettagli della configurazione del grafo.</span><span class="sxs-lookup"><span data-stu-id="3508c-106">The DVD Navigator builds the graph, so in general it is not necessary to understand the details of how the graph is configured.</span></span> <span data-ttu-id="3508c-107">Per altre informazioni, vedere [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="3508c-107">For more information, see [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span></span>

<span data-ttu-id="3508c-108">Nella figura seguente viene illustrato un grafico del filtro DVD con un decodificatore software.</span><span class="sxs-lookup"><span data-stu-id="3508c-108">The following illustration shows a DVD filter graph with a software decoder.</span></span>

![grafico filtro DVD per Windows XP](images/dvd-graph-xp.png)

<span data-ttu-id="3508c-110">Quando è presente un decodificatore hardware, questo viene in genere connesso direttamente alla scheda video tramite una porta video.</span><span class="sxs-lookup"><span data-stu-id="3508c-110">When a hardware decoder is present, it is typically connected directly to the video card by a video port.</span></span> <span data-ttu-id="3508c-111">In questo modo, i bit video decodificati possono essere inviati direttamente al buffer frame sulla scheda grafica senza passare alla memoria host.</span><span class="sxs-lookup"><span data-stu-id="3508c-111">This enables the decoded video bits to be sent directly to the frame buffer on the graphics card without passing into host memory.</span></span> <span data-ttu-id="3508c-112">Per gestire questa connessione diretta nelle versioni precedenti di Windows, DirectShow supporta le estensioni VPE (DirectDraw video Port Extensions) tramite un'interfaccia sul [filtro del mixer sovrapposto](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3508c-112">To manage this direct connection on earlier versions of Windows, DirectShow supports DirectDraw Video Port Extensions (VPE) through an interface on the [Overlay Mixer Filter](overlay-mixer-filter.md).</span></span>

> [!Note]  
> <span data-ttu-id="3508c-113">Il mixer overlay è ora deprecato.</span><span class="sxs-lookup"><span data-stu-id="3508c-113">The Overlay Mixer is now deprecated.</span></span>

 

<span data-ttu-id="3508c-114">In Windows XP e versioni successive, un decodificatore hardware può connettersi al filtro di [gestione porta video](video-port-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="3508c-114">In Windows XP and later, a hardware decoder can connect to the [Video Port Manager](video-port-manager.md) filter.</span></span>

![Graph DVD per Windows XP con un decoder hardware](images/dvd-hwgraph-xp.png)

<span data-ttu-id="3508c-116">In tutti questi grafici, il navigatore DVD è il filtro di origine; esegue diverse attività:</span><span class="sxs-lookup"><span data-stu-id="3508c-116">In all these graphs, the DVD Navigator is the source filter; it performs several tasks:</span></span>

-   <span data-ttu-id="3508c-117">Legge i dati di navigazione e video dal disco.</span><span class="sxs-lookup"><span data-stu-id="3508c-117">Reads the navigation and video data from the disc.</span></span>
-   <span data-ttu-id="3508c-118">Esegue il demultiplexing dei dati video, audio e subpicture in flussi distinti.</span><span class="sxs-lookup"><span data-stu-id="3508c-118">Demultiplexes the video, audio, and subpicture data into separate streams.</span></span>
-   <span data-ttu-id="3508c-119">Pompa i flussi nel grafico per un'ulteriore elaborazione e un eventuale rendering.</span><span class="sxs-lookup"><span data-stu-id="3508c-119">Pumps the streams into the graph for further processing and eventual rendering.</span></span>
-   <span data-ttu-id="3508c-120">Informa l'applicazione di eventi correlati a DVD.</span><span class="sxs-lookup"><span data-stu-id="3508c-120">Informs your application of DVD-related events.</span></span>

<span data-ttu-id="3508c-121">Nel flusso audio, il navigatore DVD si connette a valle a un decoder audio, che si connette al [filtro renderer DirectSound](directsound-renderer-filter.md), il renderer audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="3508c-121">On the audio stream, the DVD Navigator connects downstream to an audio decoder, which connects to the [DirectSound Renderer Filter](directsound-renderer-filter.md), the default audio renderer.</span></span> <span data-ttu-id="3508c-122">Nei flussi video e subpicture, i filtri downstream sono il decodificatore video di terze parti e il renderer di mixaggio video (o il [mixer overlay](overlay-mixer-filter.md)e il [renderer video](video-renderer-filter.md) nelle applicazioni di livello inferiore).</span><span class="sxs-lookup"><span data-stu-id="3508c-122">On the video and subpicture streams, the downstream filters are the third-party video decoder, and the Video Mixing Renderer (or the [Overlay Mixer](overlay-mixer-filter.md), and the [Video Renderer](video-renderer-filter.md) on downlevel applications).</span></span> <span data-ttu-id="3508c-123">Se l'applicazione gestirà i dati della riga 21 con didascalia chiusa, è necessario aggiungere il filtro del decodificatore 2 della riga 21 al grafico.</span><span class="sxs-lookup"><span data-stu-id="3508c-123">If your application will handle line 21 closed-captioned data, you must add the DirectShow Line 21 Decoder 2 filter to the graph.</span></span> <span data-ttu-id="3508c-124">Si tratta di una singola chiamata al metodo. il filtro verrà connesso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3508c-124">This involves a single method call; the filter will be connected automatically.</span></span>

<span data-ttu-id="3508c-125">L'applicazione comunica con e controlla il navigatore DVD tramite le interfacce personalizzate esposte da DVD Navigator: [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), ovvero i metodi "set" e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), ovvero i metodi "Get".</span><span class="sxs-lookup"><span data-stu-id="3508c-125">Your application communicates with and controls the DVD Navigator through the custom interfaces that the DVD Navigator exposes: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)—the "set" methods—and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)—the "get" methods.</span></span> <span data-ttu-id="3508c-126">Deve inoltre comunicare con Filter Graph Manager (tramite [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) per arrestare, avviare e controllare altrimenti il grafo.</span><span class="sxs-lookup"><span data-stu-id="3508c-126">It also must communicate with the filter graph manager (through [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) to stop, start, and otherwise control the graph.</span></span> <span data-ttu-id="3508c-127">Potrebbe anche essere necessario controllare altri filtri singoli, ad esempio il filtro del mixer sovrapposto per passare da un schermo a schermo intero a un altro.</span><span class="sxs-lookup"><span data-stu-id="3508c-127">You might also need to control other individual filters, such as the Overlay Mixer filter for switching between windowed and full-screen display.</span></span> <span data-ttu-id="3508c-128">Per ulteriori informazioni, vedere [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span><span class="sxs-lookup"><span data-stu-id="3508c-128">For more information, see [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span></span> <span data-ttu-id="3508c-129">La configurazione esatta del grafo varia a seconda del tipo di decodificatore MPEG-2 installato, se è necessario gestire la riga 21 dati con didascalia chiusa e altri fattori.</span><span class="sxs-lookup"><span data-stu-id="3508c-129">The exact configuration of the graph will vary depending on what type of MPEG-2 decoder you have installed, whether you need to handle line 21 closed-captioned data, and other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3508c-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3508c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3508c-131">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="3508c-131">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



