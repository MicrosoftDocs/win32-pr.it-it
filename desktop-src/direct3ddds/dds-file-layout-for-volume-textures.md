---
title: Esempio di trama del volume DDS
description: Per una trama del volume, usare il \_ complesso ddsCaps, DDSCAPS2 \_ volume, DDSD \_ Depth, Flags e set e dwDepth. Una trama del volume è un'estensione di una trama standard per Direct3D 9; è possibile definire una trama del volume con o senza mipmap.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298363"
---
# <a name="dds-volume-texture-example"></a><span data-ttu-id="1ea79-104">Esempio di trama del volume DDS</span><span class="sxs-lookup"><span data-stu-id="1ea79-104">DDS Volume Texture Example</span></span>

<span data-ttu-id="1ea79-105">Per una trama del volume, usare il \_ complesso ddsCaps, DDSCAPS2 \_ volume, DDSD \_ Depth, Flags e set e dwDepth.</span><span class="sxs-lookup"><span data-stu-id="1ea79-105">For a volume texture, use the DDSCAPS\_COMPLEX, DDSCAPS2\_VOLUME, DDSD\_DEPTH, flags and set and dwDepth.</span></span> <span data-ttu-id="1ea79-106">Una trama del volume è un'estensione di una trama standard per Direct3D 9; è possibile definire una trama del volume con o senza mipmap.</span><span class="sxs-lookup"><span data-stu-id="1ea79-106">A volume texture is an extension of a standard texture for Direct3D 9; a volume texture is can be defined with or without mipmaps.</span></span>

<span data-ttu-id="1ea79-107">Per i volumi senza mipmap, ogni sezione di profondità viene scritta nel file in ordine.</span><span class="sxs-lookup"><span data-stu-id="1ea79-107">For volumes without mipmaps, each depth slice is written to the file in order.</span></span> <span data-ttu-id="1ea79-108">Se sono inclusi mipmap, tutte le sezioni di profondità per un determinato livello di mipmap vengono scritte insieme, con ogni livello che contiene la metà di un numero di sezioni pari al livello precedente con un minimo di 1.</span><span class="sxs-lookup"><span data-stu-id="1ea79-108">If mipmaps are included, all depth slices for a given mipmap level are written together, with each level containing half as many slices as the previous level with a minimum of 1.</span></span>

<span data-ttu-id="1ea79-109">Ad esempio, una mappa del volume 64 per 64 per 4 usando un formato pixel di R8G8B8 (3 byte per pixel) con tutti i livelli di mipmap conterrà quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1ea79-109">For example, a 64-by-64-by-4 volume map using a pixel format of R8G8B8 (3 bytes per pixel) with all mipmap levels would contain the following:</span></span>



| <span data-ttu-id="1ea79-110">Componenti DDS</span><span class="sxs-lookup"><span data-stu-id="1ea79-110">DDS Components</span></span>                      | <span data-ttu-id="1ea79-111">\# Byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-111">\# Bytes</span></span>    |
|-------------------------------------|-------------|
| <span data-ttu-id="1ea79-112">header</span><span class="sxs-lookup"><span data-stu-id="1ea79-112">header</span></span>                              | <span data-ttu-id="1ea79-113">128 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-113">128 bytes</span></span>   |
| <span data-ttu-id="1ea79-114">64-by-64 sezione 1 di 4 immagine principale.</span><span class="sxs-lookup"><span data-stu-id="1ea79-114">64-by-64 slice 1 of 4 main image.</span></span>   | <span data-ttu-id="1ea79-115">12288 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-115">12288 bytes</span></span> |
| <span data-ttu-id="1ea79-116">64-by-64 sezione 2 di 4 immagine principale.</span><span class="sxs-lookup"><span data-stu-id="1ea79-116">64-by-64 slice 2 of 4 main image.</span></span>   | <span data-ttu-id="1ea79-117">12288 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-117">12288 bytes</span></span> |
| <span data-ttu-id="1ea79-118">64-by-64 sezione 3 di 4 immagine principale.</span><span class="sxs-lookup"><span data-stu-id="1ea79-118">64-by-64 slice 3 of 4 main image.</span></span>   | <span data-ttu-id="1ea79-119">12288 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-119">12288 bytes</span></span> |
| <span data-ttu-id="1ea79-120">64-by-64 sezione 4 di 4 immagine principale.</span><span class="sxs-lookup"><span data-stu-id="1ea79-120">64-by-64 slice 4 of 4 main image.</span></span>   | <span data-ttu-id="1ea79-121">12288 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-121">12288 bytes</span></span> |
| <span data-ttu-id="1ea79-122">32-by-32 Slice 1 di 2 mipmap image.</span><span class="sxs-lookup"><span data-stu-id="1ea79-122">32-by-32 slice 1 of 2 mipmap image.</span></span> | <span data-ttu-id="1ea79-123">3072 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-123">3072 bytes</span></span>  |
| <span data-ttu-id="1ea79-124">32-by-32 Slice 2 of 2 mipmap image.</span><span class="sxs-lookup"><span data-stu-id="1ea79-124">32-by-32 slice 2 of 2 mipmap image.</span></span> | <span data-ttu-id="1ea79-125">3072 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-125">3072 bytes</span></span>  |
| <span data-ttu-id="1ea79-126">16 per 16 sezione 1 di 1 immagine mipmap.</span><span class="sxs-lookup"><span data-stu-id="1ea79-126">16-by-16 slice 1 of 1 mipmap image.</span></span> | <span data-ttu-id="1ea79-127">768 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-127">768 bytes</span></span>   |
| <span data-ttu-id="1ea79-128">8-by-8 sezione 1 di 1 immagine mipmap.</span><span class="sxs-lookup"><span data-stu-id="1ea79-128">8-by-8 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="1ea79-129">192 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-129">192 bytes</span></span>   |
| <span data-ttu-id="1ea79-130">4 per 4 Slice 1 di 1 mipmap image.</span><span class="sxs-lookup"><span data-stu-id="1ea79-130">4-by-4 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="1ea79-131">48 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-131">48 bytes</span></span>    |
| <span data-ttu-id="1ea79-132">2-by-2 Slice 1 di 1 mipmap image.</span><span class="sxs-lookup"><span data-stu-id="1ea79-132">2-by-2 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="1ea79-133">12 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-133">12 bytes</span></span>    |
| <span data-ttu-id="1ea79-134">1-per-1 sezione 1 di 1 immagine mipmap.</span><span class="sxs-lookup"><span data-stu-id="1ea79-134">1-by-1 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="1ea79-135">3 byte</span><span class="sxs-lookup"><span data-stu-id="1ea79-135">3 bytes</span></span>     |



 

<span data-ttu-id="1ea79-136">Si noti che il livello di mipmap più piccolo è di 3 byte perché bitCount è 24 e non è presente alcuna compressione aggiuntiva a questo livello.</span><span class="sxs-lookup"><span data-stu-id="1ea79-136">Note that the smallest mipmap level is only 3 bytes because the bitcount is 24 and there is no added compression at this level.</span></span>

<span data-ttu-id="1ea79-137">In DirectX 8 è stato aggiunto il supporto per le trame del volume.</span><span class="sxs-lookup"><span data-stu-id="1ea79-137">Support for volume textures was added in DirectX 8.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ea79-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ea79-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea79-139">Guida alla programmazione per DDS</span><span class="sxs-lookup"><span data-stu-id="1ea79-139">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




