---
description: Principali tipi di supporti
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Principali tipi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549576"
---
# <a name="major-media-types"></a><span data-ttu-id="5c8c2-103">Principali tipi di supporti</span><span class="sxs-lookup"><span data-stu-id="5c8c2-103">Major Media Types</span></span>

<span data-ttu-id="5c8c2-104">In un tipo di supporto, *il tipo principale* descrive la categoria complessiva dei dati, ad esempio audio o video.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="5c8c2-105">Il *sottotipo*, se presente, perfeziona ulteriormente il tipo principale.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="5c8c2-106">Ad esempio, se il tipo principale è video, il sottotipo potrebbe essere un video RGB a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="5c8c2-107">I sottotipi distinguono anche i formati codificati, ad esempio i video H.264, dai formati non compressi.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="5c8c2-108">Il tipo principale e il sottotipo sono identificati dai GUID e archiviati negli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c8c2-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="5c8c2-109">Attributo</span><span class="sxs-lookup"><span data-stu-id="5c8c2-109">Attribute</span></span>                                             | <span data-ttu-id="5c8c2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c8c2-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="5c8c2-111">MF \_ MT \_ MAJOR \_ TYPE</span><span class="sxs-lookup"><span data-stu-id="5c8c2-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="5c8c2-112">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-112">Major type.</span></span> |
| [<span data-ttu-id="5c8c2-113">MF \_ MT \_ SUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5c8c2-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="5c8c2-114">Sottotipo.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-114">Subtype.</span></span>    |



 

<span data-ttu-id="5c8c2-115">Vengono definiti i tipi principali seguenti.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-115">The following major types are defined.</span></span>



| <span data-ttu-id="5c8c2-116">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="5c8c2-116">Major Type</span></span>                    | <span data-ttu-id="5c8c2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c8c2-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="5c8c2-118">Sottotipi</span><span class="sxs-lookup"><span data-stu-id="5c8c2-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c8c2-119">**MFMediaType \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="5c8c2-120">Audio.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="5c8c2-121">[GUID del sottotipo audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="5c8c2-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="5c8c2-122">**Binario MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="5c8c2-123">Flusso binario.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="5c8c2-124">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-124">None.</span></span>                                                |
| <span data-ttu-id="5c8c2-125">**MFMediaType \_ FileTransfer**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="5c8c2-126">Flusso che contiene i file di dati.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="5c8c2-127">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-127">None.</span></span>                                                |
| <span data-ttu-id="5c8c2-128">**MFMediaType \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="5c8c2-129">Flusso HTML.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="5c8c2-130">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-130">None.</span></span>                                                |
| <span data-ttu-id="5c8c2-131">**Immagine \_ MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="5c8c2-132">Flusso di immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="5c8c2-133">[GUID WIC e CLSID](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="5c8c2-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="5c8c2-134">**Metadati di \_ MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-134">**MFMediaType\_Metadata**</span></span>        | <span data-ttu-id="5c8c2-135">Flusso di metadati.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-135">Metadata stream.</span></span>                                                                                                                                        | <span data-ttu-id="5c8c2-136">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-136">None.</span></span>       |
| <span data-ttu-id="5c8c2-137">**MFMediaType \_ Protected**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-137">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="5c8c2-138">Supporti protetti.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-138">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="5c8c2-139">Il sottotipo specifica lo schema di protezione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-139">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="5c8c2-140">**Percezione di MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-140">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="5c8c2-141">Flussi da un sensore di fotocamera o da un'unità di elaborazione che causa e comprende i dati video non elaborati e fornisce informazioni sull'ambiente o sugli esseri umani in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-141">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="5c8c2-142">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-142">None.</span></span>                                                |
| <span data-ttu-id="5c8c2-143">**MFMediaType \_ SAMI**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-143">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="5c8c2-144">Didascalie SAMI (Accessible Media Interchange) sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-144">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="5c8c2-145">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-145">None.</span></span>                                                |
| <span data-ttu-id="5c8c2-146">**MFMediaType \_ Script**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-146">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="5c8c2-147">Flusso di script.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-147">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="5c8c2-148">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-148">None.</span></span>                                                |
| <span data-ttu-id="5c8c2-149">**Flusso \_ MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-149">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="5c8c2-150">Flusso multiplexed o flusso elementare.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-150">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="5c8c2-151">GUID del sottotipo di flusso</span><span class="sxs-lookup"><span data-stu-id="5c8c2-151">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="5c8c2-152">**Video su MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-152">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="5c8c2-153">Video.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-153">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="5c8c2-154">[GUID del sottotipo video.](video-subtype-guids.md)</span><span class="sxs-lookup"><span data-stu-id="5c8c2-154">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="5c8c2-155">I componenti di terze parti possono definire nuovi tipi principali e nuovi sottotipi.</span><span class="sxs-lookup"><span data-stu-id="5c8c2-155">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c8c2-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c8c2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c8c2-157">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5c8c2-157">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5c8c2-158">Tipi di supporti</span><span class="sxs-lookup"><span data-stu-id="5c8c2-158">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
