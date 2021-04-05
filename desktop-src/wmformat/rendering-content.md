---
title: Rendering del contenuto
description: Rendering del contenuto
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows Media Format SDK, rendering del contenuto
- Formato avanzato dei sistemi (ASF), rendering del contenuto
- ASF (Advanced Systems Format), rendering del contenuto
- ASF (Advanced Systems Format), rendering del contenuto
- ASF (formato avanzato dei sistemi), rendering del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856849"
---
# <a name="rendering-content"></a><span data-ttu-id="a6500-108">Rendering del contenuto</span><span class="sxs-lookup"><span data-stu-id="a6500-108">Rendering Content</span></span>

<span data-ttu-id="a6500-109">Windows Media Format SDK non fornisce routine per il rendering del contenuto fornito dall'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="a6500-109">The Windows Media Format SDK does not provide any routines for rendering content delivered by the reader object.</span></span> <span data-ttu-id="a6500-110">Se si scrivono applicazioni per riprodurre il contenuto nei file ASF, è necessario implementare le routine di rendering personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a6500-110">If you write applications to play back the content in ASF files, you must implement your own rendering routines.</span></span>

<span data-ttu-id="a6500-111">È necessario prestare attenzione quando si esegue il rendering del contenuto per assicurarsi che venga eseguito il rendering degli esempi in ordine di presentazione e che gli esempi di flussi diversi vengano sincronizzati durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="a6500-111">You must be careful when rendering content to ensure that samples are rendered in order of presentation time and that samples from different streams are synchronized when rendering.</span></span> <span data-ttu-id="a6500-112">Il metodo utilizzato per garantire la sincronizzazione dei flussi dipenderà dalla tecnica di rendering utilizzata per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a6500-112">The method you employ to ensure stream synchronization will depend upon the rendering technique you use for your application.</span></span> <span data-ttu-id="a6500-113">In generale, se si dispone di flussi audio e video, è necessario eseguire la sincronizzazione con il flusso audio, perché l'incoerenza nel flusso audio è più evidente rispetto ad alcuni frame rilasciati in un flusso video.</span><span class="sxs-lookup"><span data-stu-id="a6500-113">In general, if you have audio and video streams, you should synchronize to the audio stream, because inconsistency in the audio stream is more noticeable than a few dropped frames in a video stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6500-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6500-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6500-115">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="a6500-115">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="a6500-116">**Per recuperare esempi di supporti con il Reader asincrono**</span><span class="sxs-lookup"><span data-stu-id="a6500-116">**To Retrieve Media Samples with the Asynchronous Reader**</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="a6500-117">**Per recuperare esempi di supporti con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="a6500-117">**To Retrieve Media Samples with the Synchronous Reader**</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




