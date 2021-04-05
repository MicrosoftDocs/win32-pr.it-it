---
title: Flussi arbitrari
description: Flussi arbitrari
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media Format SDK, flussi arbitrari
- ASF (Advanced Systems Format), flussi arbitrari
- ASF (formato avanzato dei sistemi), flussi arbitrari
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- flussi arbitrari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707870"
---
# <a name="arbitrary-streams"></a><span data-ttu-id="f75f7-110">Flussi arbitrari</span><span class="sxs-lookup"><span data-stu-id="f75f7-110">Arbitrary Streams</span></span>

<span data-ttu-id="f75f7-111">Oltre ai flussi audio e video e ai flussi di immagini, un file ASF può contenere i flussi che contengono una varietà di dati.</span><span class="sxs-lookup"><span data-stu-id="f75f7-111">In addition to audio and video streams and image streams, an ASF file can accommodate streams containing a variety of data.</span></span> <span data-ttu-id="f75f7-112">Gli oggetti di Windows Media Format SDK forniscono supporto per flussi di script, flussi di trasferimento di file, flussi Web e flussi di dati arbitrari.</span><span class="sxs-lookup"><span data-stu-id="f75f7-112">The objects of the Windows Media Format SDK provide support for script streams, file transfer streams, Web streams, and arbitrary data streams.</span></span> <span data-ttu-id="f75f7-113">Tutti questi tipi di flusso sono arbitrari, ovvero non viene eseguita alcuna convalida dei dati da parte dell'oggetto di lettura.</span><span class="sxs-lookup"><span data-stu-id="f75f7-113">All of these stream types are arbitrary, meaning that no data validation is performed by the reading object.</span></span> <span data-ttu-id="f75f7-114">Quando si includono flussi di questi tipi nei file, assicurarsi che l'applicazione di lettura esegua la convalida o il controllo dei dati per garantire che il contenuto non sia stato danneggiato o intenzionalmente modificato da terze parti dannose.</span><span class="sxs-lookup"><span data-stu-id="f75f7-114">When you include streams of these types in your files, be sure that the reading application performs validation or data checking to ensure that your content has not been corrupted or intentionally mangled by a malicious third party.</span></span>

<span data-ttu-id="f75f7-115">Sebbene gli oggetti di questo SDK non verifichino o convalidano i dati in flussi arbitrari, diversi tipi di flussi arbitrari sono supportati in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="f75f7-115">Although the objects of this SDK do not verify or validate data in arbitrary streams, several types of arbitrary streams are natively supported.</span></span> <span data-ttu-id="f75f7-116">Nella tabella seguente sono elencati i tipi di flusso arbitrari predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f75f7-116">The following table lists the predefined arbitrary stream types.</span></span> <span data-ttu-id="f75f7-117">Sono supportati anche i flussi di script, ma vengono descritti separatamente nella sezione [comandi script](script-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="f75f7-117">Script streams are also supported, but are discussed separately in the [Script Commands](script-commands.md) section.</span></span> <span data-ttu-id="f75f7-118">Per ulteriori informazioni sulla creazione di tipi personalizzati, vedere [flussi di dati arbitrari personalizzati](custom-arbitrary-data-streams.md).</span><span class="sxs-lookup"><span data-stu-id="f75f7-118">For more information about creating custom types, see [Custom Arbitrary Data Streams](custom-arbitrary-data-streams.md).</span></span>



| <span data-ttu-id="f75f7-119">Tipo arbitrario</span><span class="sxs-lookup"><span data-stu-id="f75f7-119">Arbitrary type</span></span>                   | <span data-ttu-id="f75f7-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f75f7-120">Description</span></span>                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="f75f7-121">Flussi di testo</span><span class="sxs-lookup"><span data-stu-id="f75f7-121">Text Streams</span></span>](text-streams.md) | <span data-ttu-id="f75f7-122">Contengono stringhe di testo.</span><span class="sxs-lookup"><span data-stu-id="f75f7-122">Contain text strings.</span></span>                                             |
| [<span data-ttu-id="f75f7-123">Flussi di file</span><span class="sxs-lookup"><span data-stu-id="f75f7-123">File Streams</span></span>](file-streams.md) | <span data-ttu-id="f75f7-124">Contenere uno o più file di dati.</span><span class="sxs-lookup"><span data-stu-id="f75f7-124">Contain one or more data files.</span></span>                                   |
| [<span data-ttu-id="f75f7-125">Flussi Web</span><span class="sxs-lookup"><span data-stu-id="f75f7-125">Web Streams</span></span>](web-streams.md)   | <span data-ttu-id="f75f7-126">Contiene file di dati equivalenti alla versione memorizzata nella cache di pagine Web.</span><span class="sxs-lookup"><span data-stu-id="f75f7-126">Contain data files equivalent to the cached version of Web pages.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f75f7-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f75f7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f75f7-128">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="f75f7-128">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="f75f7-129">**Flussi audio e video**</span><span class="sxs-lookup"><span data-stu-id="f75f7-129">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="f75f7-130">**Configurazione di tipi di flusso arbitrari**</span><span class="sxs-lookup"><span data-stu-id="f75f7-130">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




