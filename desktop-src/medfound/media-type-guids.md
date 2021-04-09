---
description: Tipi di supporti principali
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Tipi di supporti principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968942"
---
# <a name="major-media-types"></a><span data-ttu-id="82d42-103">Tipi di supporti principali</span><span class="sxs-lookup"><span data-stu-id="82d42-103">Major Media Types</span></span>

<span data-ttu-id="82d42-104">In un tipo di supporto, il *tipo principale* descrive la categoria complessiva dei dati, ad esempio audio o video.</span><span class="sxs-lookup"><span data-stu-id="82d42-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="82d42-105">Il *sottotipo*, se presente, perfeziona ulteriormente il tipo principale.</span><span class="sxs-lookup"><span data-stu-id="82d42-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="82d42-106">Se, ad esempio, il tipo principale è video, il sottotipo potrebbe essere video RGB a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="82d42-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="82d42-107">I sottotipi distinguono inoltre formati codificati, ad esempio video H. 264, da formati non compressi.</span><span class="sxs-lookup"><span data-stu-id="82d42-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="82d42-108">Il tipo e il sottotipo principali sono identificati dai GUID e archiviati negli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="82d42-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="82d42-109">Attributo</span><span class="sxs-lookup"><span data-stu-id="82d42-109">Attribute</span></span>                                             | <span data-ttu-id="82d42-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82d42-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="82d42-111">\_ \_ tipo principale MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="82d42-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="82d42-112">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="82d42-112">Major type.</span></span> |
| [<span data-ttu-id="82d42-113">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="82d42-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="82d42-114">Sottotipo.</span><span class="sxs-lookup"><span data-stu-id="82d42-114">Subtype.</span></span>    |



 

<span data-ttu-id="82d42-115">Sono definiti i seguenti tipi principali.</span><span class="sxs-lookup"><span data-stu-id="82d42-115">The following major types are defined.</span></span>



| <span data-ttu-id="82d42-116">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="82d42-116">Major Type</span></span>                    | <span data-ttu-id="82d42-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82d42-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="82d42-118">Sottotipi</span><span class="sxs-lookup"><span data-stu-id="82d42-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="82d42-119">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d42-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="82d42-120">Audio.</span><span class="sxs-lookup"><span data-stu-id="82d42-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="82d42-121">[GUID del sottotipo audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="82d42-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="82d42-122">**\_Binario MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d42-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="82d42-123">Flusso binario.</span><span class="sxs-lookup"><span data-stu-id="82d42-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="82d42-124">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="82d42-124">None.</span></span>                                                |
| <span data-ttu-id="82d42-125">**MFMediaType \_ filetransfer**</span><span class="sxs-lookup"><span data-stu-id="82d42-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="82d42-126">Flusso contenente file di dati.</span><span class="sxs-lookup"><span data-stu-id="82d42-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="82d42-127">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="82d42-127">None.</span></span>                                                |
| <span data-ttu-id="82d42-128">**\_HTML MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d42-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="82d42-129">Flusso HTML.</span><span class="sxs-lookup"><span data-stu-id="82d42-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="82d42-130">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="82d42-130">None.</span></span>                                                |
| <span data-ttu-id="82d42-131">**Immagine di MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="82d42-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="82d42-132">Flusso di immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="82d42-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="82d42-133">[GUID e CLSID WIC](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="82d42-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="82d42-134">**MFMediaType \_ protetto**</span><span class="sxs-lookup"><span data-stu-id="82d42-134">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="82d42-135">Supporti protetti.</span><span class="sxs-lookup"><span data-stu-id="82d42-135">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="82d42-136">Il sottotipo specifica lo schema di protezione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="82d42-136">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="82d42-137">**\_Percezione MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d42-137">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="82d42-138">Flussi da un sensore della fotocamera o da un'unità di elaborazione che motiva e riconosce i dati video non elaborati e fornisce informazioni sull'ambiente o sugli utenti.</span><span class="sxs-lookup"><span data-stu-id="82d42-138">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="82d42-139">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="82d42-139">None.</span></span>                                                |
| <span data-ttu-id="82d42-140">**\_Sami MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d42-140">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="82d42-141">Didascalie di Media Interchange accessibili (SAMI) sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="82d42-141">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="82d42-142">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="82d42-142">None.</span></span>                                                |
| <span data-ttu-id="82d42-143">**\_Script MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d42-143">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="82d42-144">Flusso di script.</span><span class="sxs-lookup"><span data-stu-id="82d42-144">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="82d42-145">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="82d42-145">None.</span></span>                                                |
| <span data-ttu-id="82d42-146">**\_Flusso MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d42-146">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="82d42-147">Flusso multiplex o elementare.</span><span class="sxs-lookup"><span data-stu-id="82d42-147">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="82d42-148">GUID del sottotipo di flusso</span><span class="sxs-lookup"><span data-stu-id="82d42-148">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="82d42-149">**Video di MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="82d42-149">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="82d42-150">Video.</span><span class="sxs-lookup"><span data-stu-id="82d42-150">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="82d42-151">[GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="82d42-151">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="82d42-152">I componenti di terze parti possono definire nuovi tipi principali e nuovi sottotipi.</span><span class="sxs-lookup"><span data-stu-id="82d42-152">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82d42-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82d42-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82d42-154">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d42-154">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="82d42-155">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="82d42-155">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
