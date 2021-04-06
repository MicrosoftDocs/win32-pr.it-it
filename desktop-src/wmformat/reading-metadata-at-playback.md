---
title: Lettura dei metadati durante la riproduzione
description: Lettura dei metadati durante la riproduzione
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- Windows Media Format SDK, lettura dei metadati
- Windows Media Format SDK, Reader asincroni
- Windows Media Format SDK, lettori sincroni
- ASF (Advanced Systems Format), lettura dei metadati
- ASF (Advanced Systems Format), lettura dei metadati
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- Reader asincroni, lettura dei metadati
- lettori sincroni, lettura dei metadati
- metadati, lettura alla riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a2515dd62092d02a45b0261fe2b501e0833a31
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046426"
---
# <a name="reading-metadata-at-playback"></a><span data-ttu-id="891b3-115">Lettura dei metadati durante la riproduzione</span><span class="sxs-lookup"><span data-stu-id="891b3-115">Reading Metadata at Playback</span></span>

<span data-ttu-id="891b3-116">Sia l'oggetto Reader asincrono che l'oggetto Reader sincrono possono leggere i metadati dall'intestazione di un file ASF caricato.</span><span class="sxs-lookup"><span data-stu-id="891b3-116">Both the asynchronous reader object and the synchronous reader object can read the metadata from the header of a loaded ASF file.</span></span> <span data-ttu-id="891b3-117">Durante la lettura dei file, gli attributi dei metadati sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="891b3-117">When reading files, the metadata attributes are all read-only.</span></span> <span data-ttu-id="891b3-118">È possibile eseguire query su entrambi gli oggetti Reader per le interfacce [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) e [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="891b3-118">Both reader objects can be queried for the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interfaces.</span></span>

<span data-ttu-id="891b3-119">Per ulteriori informazioni sull'accesso ai metadati, vedere [utilizzo dei metadati](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="891b3-119">For more information about accessing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="891b3-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="891b3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="891b3-121">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="891b3-121">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




