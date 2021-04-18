---
title: Lettura di flussi con pixel non quadrati
description: Lettura di flussi con pixel non quadrati
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows Media Format SDK, lettura di flussi video
- Windows Media Format SDK, flussi video
- Windows Media Format SDK, pixel non quadrati
- Windows Media Format SDK, pixel (non quadrato)
- Formato di sistemi avanzati (ASF), lettura di flussi video
- ASF (Advanced Systems Format), lettura di flussi video
- Formati di sistemi avanzati (ASF), flussi video
- ASF (Advanced Systems Format), flussi video
- Formato di sistemi avanzati (ASF), pixel non quadrati
- ASF (formato avanzato dei sistemi), pixel non quadrati
- Formato di sistemi avanzati (ASF), pixel (non quadrato)
- ASF (formato avanzato dei sistemi), pixel (non quadrato)
- lettura di flussi video
- flussi video, lettura
- flussi video, pixel non quadrati
- pixel non quadrati
- pixel (non quadrato)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106299001"
---
# <a name="reading-streams-with-non-square-pixels"></a><span data-ttu-id="6c296-120">Lettura di flussi con pixel non quadrati</span><span class="sxs-lookup"><span data-stu-id="6c296-120">Reading Streams with Non-Square Pixels</span></span>

<span data-ttu-id="6c296-121">Le applicazioni Reader che devono gestire correttamente i pixel non quadrati devono esaminare sia gli attributi a livello di flusso nell'intestazione ASF che le estensioni dell'unità dati in ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="6c296-121">Reader applications that need to correctly handle non-square pixels should examine both the stream-level attributes in the ASF header and the data unit extensions on each sample.</span></span> <span data-ttu-id="6c296-122">Esistono due casi in cui è necessario modificare il rettangolo di output per compensare i pixel non quadrati.</span><span class="sxs-lookup"><span data-stu-id="6c296-122">There are two cases when the output rectangle must be adjusted to compensate for non-square pixels.</span></span>

<span data-ttu-id="6c296-123">Quando il contenuto di origine è stato acquisito da un dispositivo, ad esempio una fotocamera DV (video digitale) con pixel non quadrati nel CCD, un'applicazione Reader deve modificare il relativo rettangolo di output video in modo che l'immagine venga visualizzata correttamente in un monitor del computer con pixel quadrati.</span><span class="sxs-lookup"><span data-stu-id="6c296-123">When the source content has been captured from a device such as a DV (digital video) camera with non-square pixels in its CCD, a reader application must adjust its video output rectangle so that the image displays correctly on a computer monitor with square pixels.</span></span>

<span data-ttu-id="6c296-124">Quando l'applicazione Reader genera un video che verrà riprodotto in una televisione NTSC, ad esempio tramite una connessione S-video out sulla scheda video, è necessario modificare il rettangolo video in modo che l'immagine venga visualizzata correttamente sui pixel non quadrati della televisione.</span><span class="sxs-lookup"><span data-stu-id="6c296-124">When your reader application outputs video that will be played back on an NTSC television, for example through an S-Video out connection on the video card, you must adjust the video rectangle so that the image displays correctly on the television's non-square pixels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c296-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c296-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c296-126">**Per leggere e scrivere flussi video con pixel non quadrati**</span><span class="sxs-lookup"><span data-stu-id="6c296-126">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




