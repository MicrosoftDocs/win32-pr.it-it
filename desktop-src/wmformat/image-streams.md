---
title: Flussi di immagini
description: Flussi di immagini
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Media Format SDK, flussi di immagini
- Formati di sistemi avanzati (ASF), flussi di immagini
- ASF (formato avanzato dei sistemi), flussi di immagini
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- flussi di immagini, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331607"
---
# <a name="image-streams"></a><span data-ttu-id="2a9ef-110">Flussi di immagini</span><span class="sxs-lookup"><span data-stu-id="2a9ef-110">Image Streams</span></span>

<span data-ttu-id="2a9ef-111">Un flusso di immagini è un tipo speciale di flusso che contiene ancora le immagini assegnate ai tempi di presentazione.</span><span class="sxs-lookup"><span data-stu-id="2a9ef-111">An image stream is a special type of stream that contains still images assigned to presentation times.</span></span> <span data-ttu-id="2a9ef-112">Un'applicazione può visualizzare le immagini in un flusso di immagini come desiderato, ma l'implementazione tipica consiste nel visualizzare ogni immagine fino a quando non viene recapitata l'immagine successiva, ad esempio una presentazione.</span><span class="sxs-lookup"><span data-stu-id="2a9ef-112">An application can display the pictures in an image stream as desired, but the typical implementation is to display each picture until the next picture is delivered, like a slide show.</span></span> <span data-ttu-id="2a9ef-113">In genere, un flusso di immagini è codificato in un file con un flusso audio per produrre una semplice presentazione di immagini sincronizzate con musica o sintesi vocale.</span><span class="sxs-lookup"><span data-stu-id="2a9ef-113">Usually, an image stream is encoded in a file with an audio stream to produce a simple presentation of images synchronized with music or speech.</span></span>

<span data-ttu-id="2a9ef-114">I flussi di immagini sono simili ai flussi video in quanto vengono creati da campioni non compressi compressi come parte del processo di scrittura di file, ma sono simili anche a flussi arbitrari perché è necessario assegnare una velocità in bit e una finestra del buffer appropriata per il contenuto senza basarsi sulle proprietà assegnate dal codec.</span><span class="sxs-lookup"><span data-stu-id="2a9ef-114">Image streams are like video streams in that they are created from uncompressed samples that are compressed as part of the file writing process, but they are also like arbitrary streams because you must assign a bit rate and buffer window appropriate to the content without relying on codec-assigned properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a9ef-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a9ef-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a9ef-116">**Flussi arbitrari**</span><span class="sxs-lookup"><span data-stu-id="2a9ef-116">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="2a9ef-117">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="2a9ef-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="2a9ef-118">**Flussi audio e video**</span><span class="sxs-lookup"><span data-stu-id="2a9ef-118">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="2a9ef-119">**Scrittura di flussi di immagini**</span><span class="sxs-lookup"><span data-stu-id="2a9ef-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




