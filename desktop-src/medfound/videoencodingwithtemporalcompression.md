---
description: Codifica video con compressione temporale
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codifica video con compressione temporale (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310162"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a><span data-ttu-id="3a1a9-103">Codifica video con compressione temporale (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="3a1a9-103">Video Encoding with Temporal Compression (Microsoft Media Foundation)</span></span>

<span data-ttu-id="3a1a9-104">Per ottenere i rapporti di compressione più elevati possibili, i codec Windows Media Video usano la *compressione temporale*.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-104">To achieve the highest compression ratios possible, the Windows Media Video codecs use *temporal compression*.</span></span> <span data-ttu-id="3a1a9-105">La compressione temporale è una tecnica che consente di ridurre le dimensioni dei video compressi senza codificare ogni fotogramma come immagine completa.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-105">Temporal compression is a technique of reducing compressed video size by not encoding each frame as a complete image.</span></span> <span data-ttu-id="3a1a9-106">I frame codificati completamente (come un'immagine statica) sono denominati *fotogrammi chiave*.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-106">The frames that are encoded completely (like a static image) are called *key frames*.</span></span> <span data-ttu-id="3a1a9-107">Tutti gli altri frame del video sono rappresentati da dati che specificano la modifica dall'ultimo frame.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-107">All other frames in the video are represented by data specifying the change since the last frame.</span></span> <span data-ttu-id="3a1a9-108">Questi frame sono detti *frame Delta*.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-108">These frames are called *delta frames*.</span></span>

<span data-ttu-id="3a1a9-109">La quantità di compressione che è possibile ottenere tramite la compressione temporale dipende dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-109">The amount of compression that can be achieved using temporal compression depends upon the content.</span></span> <span data-ttu-id="3a1a9-110">Se il video è statico, senza molto movimento o altre modifiche nell'immagine, è possibile creare molti frame Delta per ogni fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-110">If the video is static, without a lot of motion or other changes in image, many delta frames can be created for each key frame.</span></span> <span data-ttu-id="3a1a9-111">Maggiore è il numero di frame Delta utilizzati, minore è il flusso video codificato.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-111">The more delta frames that are used, the smaller the encoded video stream.</span></span> <span data-ttu-id="3a1a9-112">Tuttavia, se il video è dinamico, con una grande quantità di movimento o colori mutevoli, il vantaggio di usare la compressione temporale è inferiore.</span><span class="sxs-lookup"><span data-stu-id="3a1a9-112">However, if the video is dynamic, with lots of motion or changing colors, the benefit of using temporal compression is smaller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a1a9-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a1a9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a1a9-114">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="3a1a9-114">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



