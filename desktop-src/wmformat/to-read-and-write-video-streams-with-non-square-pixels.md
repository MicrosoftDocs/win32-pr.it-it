---
title: Per leggere e scrivere flussi video con pixel non quadrati
description: Per leggere e scrivere flussi video con pixel non quadrati
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- Windows Media Format SDK, lettura di flussi video
- Windows Media Format SDK, scrittura di flussi video
- Windows Media Format SDK, flussi video
- Windows Media Format SDK, pixel non quadrati
- Windows Media Format SDK, pixel (non quadrato)
- Formato di sistemi avanzati (ASF), lettura di flussi video
- ASF (Advanced Systems Format), lettura di flussi video
- Formato di sistemi avanzati (ASF), scrittura di flussi video
- ASF (Advanced Systems Format), scrittura di flussi video
- Formati di sistemi avanzati (ASF), flussi video
- ASF (Advanced Systems Format), flussi video
- Formato di sistemi avanzati (ASF), pixel non quadrati
- ASF (formato avanzato dei sistemi), pixel non quadrati
- Formato di sistemi avanzati (ASF), pixel (non quadrato)
- ASF (formato avanzato dei sistemi), pixel (non quadrato)
- lettura di flussi video
- scrittura di flussi video
- flussi video, lettura
- flussi video, scrittura
- flussi video, pixel non quadrati
- pixel non quadrati
- pixel (non quadrato)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6b3e3ba67ba42dfc144e7f95ddd042dea0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329772"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a><span data-ttu-id="a85d7-125">Per leggere e scrivere flussi video con pixel non quadrati</span><span class="sxs-lookup"><span data-stu-id="a85d7-125">To Read and Write Video Streams with Non-Square Pixels</span></span>

<span data-ttu-id="a85d7-126">I monitor computer hanno pixel quadrati, ma altri tipi di schermate video, inclusi i televisori NTSC, presentano pixel rettangolari o non quadrati.</span><span class="sxs-lookup"><span data-stu-id="a85d7-126">Computer monitors have square pixels, but other types of video screens, including NTSC televisions, have rectangular or non-square pixels.</span></span> <span data-ttu-id="a85d7-127">Inoltre, alcuni dispositivi di input, ad esempio le fotocamere digitali video (DV), hanno addebitato due dispositivi con pixel non quadrati.</span><span class="sxs-lookup"><span data-stu-id="a85d7-127">Also, some input devices, such as Digital Video (DV) cameras, have charged couple devices with non-square pixels.</span></span> <span data-ttu-id="a85d7-128">Quando si scrivono file basati su dati di origine di pixel non quadrati o destinati a essere visualizzati in dispositivi con pixel non quadrati, le informazioni sulle proporzioni dei pixel devono essere incluse nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="a85d7-128">When you are writing files that are either based on non-square pixel source data or else intended for display on devices with non-square pixels, the pixel aspect ratio information must be included in the ASF file.</span></span> <span data-ttu-id="a85d7-129">Le applicazioni Reader devono esaminare tali informazioni e usarle per regolare le proporzioni del rettangolo video in modo necessario.</span><span class="sxs-lookup"><span data-stu-id="a85d7-129">Reader applications must examine that information and use it to adjust the aspect ratio of the video rectangle as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a85d7-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a85d7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a85d7-131">**Argomenti avanzati**</span><span class="sxs-lookup"><span data-stu-id="a85d7-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="a85d7-132">**Lettura di flussi con pixel non quadrati**</span><span class="sxs-lookup"><span data-stu-id="a85d7-132">**Reading Streams with Non-Square Pixels**</span></span>](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[<span data-ttu-id="a85d7-133">**Scrittura di flussi con pixel non quadrati**</span><span class="sxs-lookup"><span data-stu-id="a85d7-133">**Writing Streams with Non-Square Pixels**</span></span>](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




