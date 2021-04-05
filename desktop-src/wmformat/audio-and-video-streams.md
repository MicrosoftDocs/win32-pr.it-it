---
title: Flussi audio e video
description: Flussi audio e video
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media Format SDK, flussi audio
- Formati di sistemi avanzati (ASF), flussi audio
- ASF (formato avanzato dei sistemi), flussi audio
- Windows Media Format SDK, flussi video
- Formati di sistemi avanzati (ASF), flussi video
- ASF (Advanced Systems Format), flussi video
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- flussi audio, informazioni
- flussi video, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044645"
---
# <a name="audio-and-video-streams"></a><span data-ttu-id="6dfd6-114">Flussi audio e video</span><span class="sxs-lookup"><span data-stu-id="6dfd6-114">Audio and Video Streams</span></span>

<span data-ttu-id="6dfd6-115">I tipi più comuni di flussi usati nei file creati usando Windows Media Format SDK sono flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-115">The most common types of streams used in files created by using the Windows Media Format SDK are audio and video streams.</span></span> <span data-ttu-id="6dfd6-116">Le rappresentazioni digitali dei dati audio e video sono complesse e utilizzano grandi quantità di memoria.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-116">Digital representations of audio and video data are complex and take up large amounts of memory.</span></span> <span data-ttu-id="6dfd6-117">Nella maggior parte dei casi, audio e video vengono compressi prima di essere aggiunti a un file ASF.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-117">Under most circumstances, both audio and video are compressed before being added to an ASF file.</span></span> <span data-ttu-id="6dfd6-118">La compressione viene eseguita usando un compressore/decompressore (codec).</span><span class="sxs-lookup"><span data-stu-id="6dfd6-118">Compression is accomplished using a compressor/decompressor (codec).</span></span>

<span data-ttu-id="6dfd6-119">Con questo SDK sono inclusi diversi codec Windows Media e forniscono una compressione di qualità eccellente per i supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-119">Several Windows Media codecs are included with this SDK, and they provide excellent quality compression for digital media.</span></span> <span data-ttu-id="6dfd6-120">Per ulteriori informazioni sui codec Windows Media, vedere funzionalità di [codec](codec-features.md).</span><span class="sxs-lookup"><span data-stu-id="6dfd6-120">For more information about the Windows Media codecs, see [Codec Features](codec-features.md).</span></span> <span data-ttu-id="6dfd6-121">Molti altri codec sono disponibili da varie origini.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-121">Many other codecs are available from various sources.</span></span> <span data-ttu-id="6dfd6-122">È possibile usare qualsiasi codec, ad esempio, durante la creazione di file ASF, ma solo i codec Windows Media sono supportati direttamente dagli oggetti di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-122">You can use whatever codecs you like when creating ASF files, but only the Windows Media codecs are directly supported by the objects of this SDK.</span></span> <span data-ttu-id="6dfd6-123">Per usare altri codec, è necessario comprimere gli esempi e passarli all'oggetto writer come dati arbitrari.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-123">To use other codecs, you must compress samples and pass them to the writer object as arbitrary data.</span></span>

<span data-ttu-id="6dfd6-124">La differenza più importante tra flussi audio o video e flussi arbitrari è che i flussi contenenti dati audio o video di Windows Media vengono convalidati dagli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-124">The most important distinction between audio or video streams and arbitrary streams is that streams containing Windows Media audio or video data are validated by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="6dfd6-125">I flussi di dati arbitrari non vengono convalidati automaticamente e devono essere controllati per verificare l'integrità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-125">Arbitrary data streams are not validated automatically, and should be checked for integrity by your application.</span></span>

<span data-ttu-id="6dfd6-126">Le proprietà di un flusso audio o video sono descritte nel profilo usato per creare il file.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-126">The properties of an audio or video stream are described in the profile used to create the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dfd6-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6dfd6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dfd6-128">**Flussi arbitrari**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-128">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="6dfd6-129">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-129">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="6dfd6-130">**Utilizzo dei profili**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-130">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




