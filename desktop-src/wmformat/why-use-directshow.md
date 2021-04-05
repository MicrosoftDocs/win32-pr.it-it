---
title: Perché usare DirectShow
description: Perché usare DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, hardware
- Windows Media Format SDK, Windows Driver Model (WDM)
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), hardware
- ASF (formato avanzato dei sistemi), hardware
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- DirectShow, informazioni
- DirectShow, hardware
- DirectShow, Windows Driver Model (WDM)
- Windows Driver Model (WDM)
- WDM (Windows Driver Model)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710372"
---
# <a name="why-use-directshow"></a><span data-ttu-id="f6177-117">Perché usare DirectShow?</span><span class="sxs-lookup"><span data-stu-id="f6177-117">Why Use DirectShow?</span></span>

<span data-ttu-id="f6177-118">Esistono due motivi principali per cui un'applicazione può usare direttamente DirectShow anziché Windows Media Format SDK: per praticità dell'architettura di streaming DirectShow e per l'accesso all'hardware.</span><span class="sxs-lookup"><span data-stu-id="f6177-118">There are two main reasons why an application might use DirectShow rather than the Windows Media Format SDK directly: for the convenience of the DirectShow streaming architecture, and for access to hardware.</span></span>

## <a name="convenience"></a><span data-ttu-id="f6177-119">Praticità</span><span class="sxs-lookup"><span data-stu-id="f6177-119">Convenience</span></span>

<span data-ttu-id="f6177-120">Con l'architettura di streaming DirectShow, sono necessarie solo alcune chiamate al metodo per riprodurre file Windows Media Audio o Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="f6177-120">With DirectShow streaming architecture, it takes only a few method calls to play Windows Media Audio or Windows Media Video files.</span></span> <span data-ttu-id="f6177-121">Anche la creazione di file è semplificata.</span><span class="sxs-lookup"><span data-stu-id="f6177-121">Creating files is also simplified.</span></span> <span data-ttu-id="f6177-122">È sufficiente specificare un profilo usando l'interfaccia **IConfigAsfWriter** sul filtro e DirectShow carica automaticamente i componenti necessari per il rendering o la scrittura dei flussi e fornisce i meccanismi per il trasferimento e la sincronizzazione del flusso dei dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="f6177-122">You simply specify a profile using the **IConfigAsfWriter** interface on the filter, and DirectShow automatically loads the required components for rendering or writing the streams, and provides the mechanisms for transferring and synchronizing the flow of media data.</span></span> <span data-ttu-id="f6177-123">DirectShow è particolarmente utile per la conversione di contenuto da formati diversi in formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f6177-123">DirectShow is especially useful when converting content from varied formats into Windows Media Format.</span></span> <span data-ttu-id="f6177-124">È possibile creare grafici di filtro DirectShow che decodificano una vasta gamma di tipi di file e di compressione e quindi inviano i flussi decodificati al filtro del [writer ASF WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f6177-124">You can create DirectShow filter graphs that decode a wide variety of file and compression types, and then feed the decoded streams into the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span> <span data-ttu-id="f6177-125">Per confronto, l'esempio UncompAVItoWMV in questo SDK funziona solo con file AVI non compressi.</span><span class="sxs-lookup"><span data-stu-id="f6177-125">By comparison, the UncompAVItoWMV sample in this SDK works only with uncompressed AVI files.</span></span> <span data-ttu-id="f6177-126">I flussi di testo e i flussi di dati arbitrari possono anche essere creati e/o sottoposti a rendering tramite DirectShow, ma ciò potrebbe richiedere la creazione di filtri DirectShow personalizzati per l'elaborazione di tali flussi.</span><span class="sxs-lookup"><span data-stu-id="f6177-126">Text streams and arbitrary data streams can also be created and/or rendered through DirectShow, but this might require you to create custom DirectShow filters for processing those streams.</span></span>

## <a name="access-to-hardware"></a><span data-ttu-id="f6177-127">Accesso all'hardware</span><span class="sxs-lookup"><span data-stu-id="f6177-127">Access to Hardware</span></span>

<span data-ttu-id="f6177-128">DirectShow è l'unico modo per il codice dell'applicazione per accedere a dispositivi hardware basati su Windows Driver Model (WDM), ad esempio fotocamere DV 1394, sintonizzatori TV e webcam USB.</span><span class="sxs-lookup"><span data-stu-id="f6177-128">DirectShow is the only way for application code to access Windows Driver Model (WDM)–based hardware devices such as 1394 DV cameras, TV tuners, and USB webcams.</span></span> <span data-ttu-id="f6177-129">Se l'applicazione deve acquisire i dati direttamente da un dispositivo hardware basato su WDM e transcodificarli in formato Windows Media e Windows Media Encoder SDK non è adatto alle proprie esigenze, DirectShow è l'unica alternativa.</span><span class="sxs-lookup"><span data-stu-id="f6177-129">If your application must capture data directly from a WDM-based hardware device and transcode it to Windows Media Format, and the Windows Media Encoder SDK does not suit your needs, then DirectShow is the only alternative.</span></span> <span data-ttu-id="f6177-130">DirectShow può essere usato anche per accedere a dispositivi legacy basati su video per Windows.</span><span class="sxs-lookup"><span data-stu-id="f6177-130">DirectShow can also be used to access legacy devices based on Video for Windows.</span></span>

 

 




