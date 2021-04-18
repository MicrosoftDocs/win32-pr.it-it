---
title: Ottenere le migliori prestazioni di ricerca video
description: Ottenere le migliori prestazioni di ricerca video
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK, migliori prestazioni di ricerca video
- Advanced Systems Format (ASF), migliori prestazioni di ricerca video
- ASF (Advanced Systems Format), migliori prestazioni di ricerca video
- ASF (Advanced Systems Format), prestazioni di ricerca video
- ASF (Advanced Systems Format), prestazioni di ricerca video
- ASF (Advanced Systems Format), prestazioni
- ASF (formato avanzato dei sistemi), prestazioni
- ricerca video
- prestazioni, ricerca video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298511"
---
# <a name="getting-the-best-video-seeking-performance"></a><span data-ttu-id="5f6ce-112">Ottenere le migliori prestazioni di ricerca video</span><span class="sxs-lookup"><span data-stu-id="5f6ce-112">Getting the Best Video Seeking Performance</span></span>

<span data-ttu-id="5f6ce-113">La ricerca di contenuto in un file è un'operazione molto comune che potenzialmente rappresenta un problema di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5f6ce-113">Seeking to content in a file is a very common operation that is potentially a performance issue.</span></span> <span data-ttu-id="5f6ce-114">Il video codificato con il codec Windows Media Video 9 è costituito principalmente da frame Delta, che registrano solo le modifiche in relazione al frame precedente.</span><span class="sxs-lookup"><span data-stu-id="5f6ce-114">Video encoded with the Windows Media Video 9 codec is made up primarily of delta frames, which only record the changes in relation to the previous frame.</span></span> <span data-ttu-id="5f6ce-115">La ricostruzione di frame Delta richiede tempo, in particolare se i fotogrammi chiave sono lontani.</span><span class="sxs-lookup"><span data-stu-id="5f6ce-115">Reconstructing delta frames takes time, particularly if the key frames are far apart.</span></span> <span data-ttu-id="5f6ce-116">Per ulteriori informazioni sulla configurazione di fotogrammi chiave per una ricerca efficiente, vedere [configurazione dei flussi video per la ricerca delle prestazioni](configuring-video-streams-for-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="5f6ce-116">For more information about configuring key frames for efficient seeking, see [Configuring Video Streams for Seeking Performance](configuring-video-streams-for-seeking-performance.md).</span></span>

<span data-ttu-id="5f6ce-117">Oltre alla configurazione corretta, è possibile migliorare le prestazioni di ricerca usando l'indicizzazione dei frame per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="5f6ce-117">In addition to proper configuration, you can improve seeking performance by using frame indexing for the video stream.</span></span> <span data-ttu-id="5f6ce-118">La ricerca di un numero di frame è in genere più veloce rispetto alla ricerca di un'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="5f6ce-118">Seeking to a frame number is typically faster than seeking to a presentation time.</span></span>

<span data-ttu-id="5f6ce-119">Se si cerca in un file con più flussi, è necessario selezionare solo i flussi necessari.</span><span class="sxs-lookup"><span data-stu-id="5f6ce-119">If seeking in a file with multiple streams, you should select only the streams that are needed.</span></span> <span data-ttu-id="5f6ce-120">Ogni flusso configurato per la lettura influirà sulle prestazioni della ricerca, perché tutti i flussi selezionati sono sincronizzati quando si cerca un punto in un file.</span><span class="sxs-lookup"><span data-stu-id="5f6ce-120">Each stream configured for reading will affect the performance of seeking, because all selected streams are synchronized when you seek to a point in a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f6ce-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f6ce-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f6ce-122">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="5f6ce-122">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="5f6ce-123">**Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono**</span><span class="sxs-lookup"><span data-stu-id="5f6ce-123">**To Seek By Frame Number Using the Asynchronous Reader**</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="5f6ce-124">**Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="5f6ce-124">**To Seek By Frame Number Using the Synchronous Reader**</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="5f6ce-125">**Per eseguire ricerche in base al tempo tramite il Reader asincrono**</span><span class="sxs-lookup"><span data-stu-id="5f6ce-125">**To Seek By Time Using the Asynchronous Reader**</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="5f6ce-126">**Per eseguire ricerche in base al tempo tramite il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="5f6ce-126">**To Seek By Time Using the Synchronous Reader**</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




