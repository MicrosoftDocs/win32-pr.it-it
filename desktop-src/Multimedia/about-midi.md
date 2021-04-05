---
title: Informazioni su MIDI
description: Informazioni su MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Multimedia di Windows, Musical Instrument Digital Interface (MIDI)
- Multimedia, Musical Instrument Digital Interface (MIDI)
- audio multimediale, MIDI (Musical Instrument Digital Interface)
- audio, Musical Instrument Digital Interface (MIDI)
- MIDI (Musical Instrument Digital Interface), informazioni
- MIDI (Musical Instrument Digital Interface), informazioni
- MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (strumento musicale digitale), MCI (Media Control Interface)
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), servizi MIDI
- MIDI (Musical Instrument Digital Interface), servizi MIDI
- Interfaccia di controllo multimediale (MCI), Musical Instrument Digital Interface (MIDI)
- MCI (Media Control Interface), Musical Instrument Digital Interface (MIDI)
- buffer di flusso, informazioni
- Servizi MIDI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708926"
---
# <a name="about-midi"></a><span data-ttu-id="26c62-119">Informazioni su MIDI</span><span class="sxs-lookup"><span data-stu-id="26c62-119">About MIDI</span></span>

<span data-ttu-id="26c62-120">Il Application Programming Interface Microsoft Win32 (API) fornisce i metodi seguenti per l'utilizzo dei dati MIDI da parte delle applicazioni:</span><span class="sxs-lookup"><span data-stu-id="26c62-120">The Microsoft Win32 application programming interface (API) provides the following methods for applications to work with MIDI data:</span></span>

-   <span data-ttu-id="26c62-121">L'interfaccia di controllo multimediale (MCI).</span><span class="sxs-lookup"><span data-stu-id="26c62-121">The Media Control Interface (MCI).</span></span> <span data-ttu-id="26c62-122">Sebbene il modo più semplice per riprodurre un file MIDI consiste nell'usare la classe della finestra MCIWnd, è anche possibile usare i comandi MCI per creare un'interfaccia personalizzata per un dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="26c62-122">Although the simplest way to play a MIDI file is to use the MCIWnd window class, you can also use MCI commands to create a customized interface to a MIDI device.</span></span> <span data-ttu-id="26c62-123">Per ulteriori informazioni sulla classe della finestra MCIWnd, vedere [classe della finestra MCIWnd](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="26c62-123">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span> <span data-ttu-id="26c62-124">Per ulteriori informazioni su MCI, vedere [MCI](mci.md)o [MCI (Media Control Interface)](media-control-interface--mci.md).</span><span class="sxs-lookup"><span data-stu-id="26c62-124">For more information about MCI, see [MCI](mci.md), or [Media Control Interface (MCI)](media-control-interface--mci.md).</span></span>
-   <span data-ttu-id="26c62-125">[Buffer di flusso](stream-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="26c62-125">[Stream Buffers](stream-buffers.md).</span></span> <span data-ttu-id="26c62-126">Questo formato consente a un'applicazione di modificare buffer di dati MIDI timestamp per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="26c62-126">This format allows an application to manipulate buffers of time-stamped MIDI data for playback.</span></span> <span data-ttu-id="26c62-127">I buffer di flusso sono utili per le applicazioni che richiedono un controllo più preciso sull'output rispetto alle offerte MCI.</span><span class="sxs-lookup"><span data-stu-id="26c62-127">Stream buffers are useful to applications that require more precise control over output than MCI offers.</span></span>
-   <span data-ttu-id="26c62-128">[Servizi MIDI](midi-services.md).</span><span class="sxs-lookup"><span data-stu-id="26c62-128">[MIDI Services](midi-services.md).</span></span> <span data-ttu-id="26c62-129">Le applicazioni che richiedono il controllo più preciso dei dati MIDI utilizzano in genere questi servizi di basso livello.</span><span class="sxs-lookup"><span data-stu-id="26c62-129">Applications that need the most precise control of MIDI data typically use these low-level services.</span></span>

<span data-ttu-id="26c62-130">Negli argomenti seguenti vengono descritti ognuno di questi metodi e viene fornita una panoramica del mapper di MIDI.</span><span class="sxs-lookup"><span data-stu-id="26c62-130">The following topics discuss each of these methods and provides an overview of the MIDI Mapper.</span></span>

-   [<span data-ttu-id="26c62-131">Mapper MIDI</span><span class="sxs-lookup"><span data-stu-id="26c62-131">The MIDI Mapper</span></span>](the-midi-mapper.md)
-   [<span data-ttu-id="26c62-132">Interfaccia di controllo multimediale (MCI)</span><span class="sxs-lookup"><span data-stu-id="26c62-132">Media Control Interface (MCI)</span></span>](media-control-interface--mci.md)
-   [<span data-ttu-id="26c62-133">Buffer di flusso</span><span class="sxs-lookup"><span data-stu-id="26c62-133">Stream Buffers</span></span>](stream-buffers.md)
-   [<span data-ttu-id="26c62-134">Servizi MIDI</span><span class="sxs-lookup"><span data-stu-id="26c62-134">MIDI Services</span></span>](midi-services.md)
-   [<span data-ttu-id="26c62-135">Riproduzione di file MIDI</span><span class="sxs-lookup"><span data-stu-id="26c62-135">Playing MIDI Files</span></span>](playing-midi-files.md)
-   [<span data-ttu-id="26c62-136">Registrazione audio MIDI</span><span class="sxs-lookup"><span data-stu-id="26c62-136">Recording MIDI Audio</span></span>](recording-midi-audio.md)
-   [<span data-ttu-id="26c62-137">Elaborazione di dati MIDI da due origini MIDI</span><span class="sxs-lookup"><span data-stu-id="26c62-137">Processing MIDI Data from Two MIDI Sources</span></span>](processing-midi-data-from-two-midi-sources.md)
-   [<span data-ttu-id="26c62-138">Creazione di file MIDI</span><span class="sxs-lookup"><span data-stu-id="26c62-138">Creating MIDI Files</span></span>](creating-midi-files.md)

 

 




