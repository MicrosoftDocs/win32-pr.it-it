---
title: Implementazione di un plug-in video DSP
description: Implementazione di un plug-in video DSP
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Plug-in di Windows Media Player, video DSP
- plug-in, video DSP
- plug-in di elaborazione dei segnali digitali, implementazione del codice
- Plug-in DSP, implementazione del codice
- plug-in di elaborazione dei segnali digitali, modifica del codice di esempio
- Plug-in DSP, modifica del codice di esempio
- plug-in per l'elaborazione di segnali digitali, implementazione video
- Plug-in DSP, implementazione video
- plug-in di video DSP, implementazione del codice
- plug-in di video DSP, modifica del codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330436"
---
# <a name="implementing-a-video-dsp-plug-in"></a><span data-ttu-id="83c63-113">Implementazione di un plug-in video DSP</span><span class="sxs-lookup"><span data-stu-id="83c63-113">Implementing a Video DSP Plug-in</span></span>

<span data-ttu-id="83c63-114">Gli adapter per la visualizzazione video del computer supportano un set di formati video.</span><span class="sxs-lookup"><span data-stu-id="83c63-114">Computer video display adapters support a set of video formats.</span></span> <span data-ttu-id="83c63-115">I codec video digitali supportano anche un set di formati video.</span><span class="sxs-lookup"><span data-stu-id="83c63-115">Digital video codecs also support a set of video formats.</span></span> <span data-ttu-id="83c63-116">Quando si tenta di riprodurre un file video specifico, Windows Media Player deve scegliere un formato da usare per il rendering.</span><span class="sxs-lookup"><span data-stu-id="83c63-116">When attempting to play a particular video file, Windows Media Player must choose a format to use for rendering.</span></span> <span data-ttu-id="83c63-117">Il lettore tenta di trovare la migliore corrispondenza tra i formati supportati dal codec video e i formati supportati dalla scheda video video, ovvero quello che produce la qualità più elevata.</span><span class="sxs-lookup"><span data-stu-id="83c63-117">The Player attempts to find the best match between the formats supported by the video codec and the formats supported by the video display adapter—that is, the one that yields the highest quality.</span></span>

<span data-ttu-id="83c63-118">Per creare un plug-in di Windows Media Player DSP che elabora il video, è necessario innanzitutto decidere quali formati video si desidera vengano elaborati dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="83c63-118">To create a Windows Media Player DSP plug-in that processes video, you'll first need to decide which video formats you'd like your plug-in to process.</span></span> <span data-ttu-id="83c63-119">Il plug-in video DSP di esempio funziona con i formati video seguenti:</span><span class="sxs-lookup"><span data-stu-id="83c63-119">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="83c63-120">NV12</span><span class="sxs-lookup"><span data-stu-id="83c63-120">NV12</span></span>
-   <span data-ttu-id="83c63-121">YV12</span><span class="sxs-lookup"><span data-stu-id="83c63-121">YV12</span></span>
-   <span data-ttu-id="83c63-122">YUY2</span><span class="sxs-lookup"><span data-stu-id="83c63-122">YUY2</span></span>
-   <span data-ttu-id="83c63-123">UYVY</span><span class="sxs-lookup"><span data-stu-id="83c63-123">UYVY</span></span>
-   <span data-ttu-id="83c63-124">RGB32</span><span class="sxs-lookup"><span data-stu-id="83c63-124">RGB32</span></span>
-   <span data-ttu-id="83c63-125">RGB24</span><span class="sxs-lookup"><span data-stu-id="83c63-125">RGB24</span></span>
-   <span data-ttu-id="83c63-126">RGB555</span><span class="sxs-lookup"><span data-stu-id="83c63-126">RGB555</span></span>
-   <span data-ttu-id="83c63-127">RGB565</span><span class="sxs-lookup"><span data-stu-id="83c63-127">RGB565</span></span>

<span data-ttu-id="83c63-128">I formati scelti per l'elaborazione dipende dall'utente.</span><span class="sxs-lookup"><span data-stu-id="83c63-128">Which formats you choose to process is up to you.</span></span> <span data-ttu-id="83c63-129">È possibile rimuovere i formati dal plug-in di esempio in modo che non siano più supportati ed è possibile aggiungere codice per elaborare formati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="83c63-129">You can remove formats from the sample plug-in so that they aren't supported any longer and you can add code to process additional formats.</span></span>

<span data-ttu-id="83c63-130">Le sezioni seguenti forniscono informazioni aggiuntive che è necessario tenere presente prima di creare il plug-in video DSP per Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="83c63-130">The following sections provide additional information you should know before creating your own video DSP plug-in for Windows Media Player:</span></span>

-   [<span data-ttu-id="83c63-131">Negoziazione del formato video nel plug-in DSP video di esempio</span><span class="sxs-lookup"><span data-stu-id="83c63-131">Video Format Negotiation in the Sample Video DSP Plug-in</span></span>](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="83c63-132">DoProcessOutput nel plug-in di video DSP di esempio</span><span class="sxs-lookup"><span data-stu-id="83c63-132">DoProcessOutput in the Sample Video DSP Plug-in</span></span>](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="83c63-133">Elaborazione del video</span><span class="sxs-lookup"><span data-stu-id="83c63-133">Processing the Video</span></span>](processing-the-video.md)

## <a name="related-topics"></a><span data-ttu-id="83c63-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83c63-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83c63-135">**Implementazione del codice DSP**</span><span class="sxs-lookup"><span data-stu-id="83c63-135">**Implementing Your DSP Code**</span></span>](implementing-your-dsp-code.md)
</dt> </dl>

 

 




