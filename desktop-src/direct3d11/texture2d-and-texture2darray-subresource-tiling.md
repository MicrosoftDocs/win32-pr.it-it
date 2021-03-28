---
title: Divisione in riquadri di sottorisorse Texture2D e Texture2DArray
description: In queste tabelle viene illustrato come affiancare le sottorisorse Texture2D e Texture2DArray.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399352"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a><span data-ttu-id="7c80c-103">Divisione in riquadri di sottorisorse Texture2D e Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="7c80c-103">Texture2D and Texture2DArray subresource tiling</span></span>

<span data-ttu-id="7c80c-104">In queste tabelle viene illustrato come affiancare le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) .</span><span class="sxs-lookup"><span data-stu-id="7c80c-104">These tables show how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources are tiled.</span></span> <span data-ttu-id="7c80c-105">I valori in queste tabelle non contano la compressione della parte finale MIP.</span><span class="sxs-lookup"><span data-stu-id="7c80c-105">The values in these tables don't count tail mip packing.</span></span>

<span data-ttu-id="7c80c-106">Questa tabella mostra il modo in cui vengono affiancate le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con conteggi multicampionamento pari a 1.</span><span class="sxs-lookup"><span data-stu-id="7c80c-106">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with multisample counts of 1 are tiled.</span></span>



| <span data-ttu-id="7c80c-107">Bits/pixel (1 campione/pixel)</span><span class="sxs-lookup"><span data-stu-id="7c80c-107">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="7c80c-108">Dimensioni riquadro (pixel, WxH)</span><span class="sxs-lookup"><span data-stu-id="7c80c-108">Tile Dimensions (Pixels, WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="7c80c-109">8</span><span class="sxs-lookup"><span data-stu-id="7c80c-109">8</span></span>                           | <span data-ttu-id="7c80c-110">256x256</span><span class="sxs-lookup"><span data-stu-id="7c80c-110">256x256</span></span>                       |
| <span data-ttu-id="7c80c-111">16</span><span class="sxs-lookup"><span data-stu-id="7c80c-111">16</span></span>                          | <span data-ttu-id="7c80c-112">con dimensioni 256x128</span><span class="sxs-lookup"><span data-stu-id="7c80c-112">256x128</span></span>                       |
| <span data-ttu-id="7c80c-113">32</span><span class="sxs-lookup"><span data-stu-id="7c80c-113">32</span></span>                          | <span data-ttu-id="7c80c-114">128x128</span><span class="sxs-lookup"><span data-stu-id="7c80c-114">128x128</span></span>                       |
| <span data-ttu-id="7c80c-115">64</span><span class="sxs-lookup"><span data-stu-id="7c80c-115">64</span></span>                          | <span data-ttu-id="7c80c-116">128x64</span><span class="sxs-lookup"><span data-stu-id="7c80c-116">128x64</span></span>                        |
| <span data-ttu-id="7c80c-117">128</span><span class="sxs-lookup"><span data-stu-id="7c80c-117">128</span></span>                         | <span data-ttu-id="7c80c-118">64x64</span><span class="sxs-lookup"><span data-stu-id="7c80c-118">64x64</span></span>                         |
| <span data-ttu-id="7c80c-119">BC1, 4</span><span class="sxs-lookup"><span data-stu-id="7c80c-119">BC1,4</span></span>                       | <span data-ttu-id="7c80c-120">512x256</span><span class="sxs-lookup"><span data-stu-id="7c80c-120">512x256</span></span>                       |
| <span data-ttu-id="7c80c-121">BC2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="7c80c-121">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="7c80c-122">256x256</span><span class="sxs-lookup"><span data-stu-id="7c80c-122">256x256</span></span>                       |



 

<span data-ttu-id="7c80c-123">I conteggi dei bit di formato non supportati con le risorse affiancate sono formati di 96 BPP, formati video, \_ formato DXGI \_ R1 \_ UNORM, \_ formato DXGI \_ R8G8 B8G8 UNORM \_ \_ e \_ formato DXGI \_ \_ \_ R8R8 G8B8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="7c80c-123">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="7c80c-124">Questa tabella mostra il modo in cui vengono affiancate le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con diversi conteggi multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="7c80c-124">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with various multisample counts are tiled.</span></span>



| <span data-ttu-id="7c80c-125">Conteggio multicampionamento</span><span class="sxs-lookup"><span data-stu-id="7c80c-125">Multisample Count</span></span>           | <span data-ttu-id="7c80c-126">Dividere le dimensioni del riquadro sopra per (WxH)</span><span class="sxs-lookup"><span data-stu-id="7c80c-126">Divide Tile Dimensions Above by (WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="7c80c-127">1</span><span class="sxs-lookup"><span data-stu-id="7c80c-127">1</span></span>                           | <span data-ttu-id="7c80c-128">1x1</span><span class="sxs-lookup"><span data-stu-id="7c80c-128">1x1</span></span>                           |
| <span data-ttu-id="7c80c-129">2</span><span class="sxs-lookup"><span data-stu-id="7c80c-129">2</span></span>                           | <span data-ttu-id="7c80c-130">2x1</span><span class="sxs-lookup"><span data-stu-id="7c80c-130">2x1</span></span>                           |
| <span data-ttu-id="7c80c-131">4</span><span class="sxs-lookup"><span data-stu-id="7c80c-131">4</span></span>                           | <span data-ttu-id="7c80c-132">2x2</span><span class="sxs-lookup"><span data-stu-id="7c80c-132">2x2</span></span>                           |
| <span data-ttu-id="7c80c-133">8</span><span class="sxs-lookup"><span data-stu-id="7c80c-133">8</span></span>                           | <span data-ttu-id="7c80c-134">4x2</span><span class="sxs-lookup"><span data-stu-id="7c80c-134">4x2</span></span>                           |
| <span data-ttu-id="7c80c-135">16</span><span class="sxs-lookup"><span data-stu-id="7c80c-135">16</span></span>                          | <span data-ttu-id="7c80c-136">4x4</span><span class="sxs-lookup"><span data-stu-id="7c80c-136">4x4</span></span>                           |



 

<span data-ttu-id="7c80c-137">Solo i conteggi dei campioni 1 e 4 sono obbligatori (e consentiti) per essere supportati con le risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="7c80c-137">Only sample counts 1 and 4 are required (and allowed) to be supported with tiled resources.</span></span> <span data-ttu-id="7c80c-138">Le risorse affiancate non supportano attualmente 2, 8 e 16 anche se sono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="7c80c-138">Tiled resources don't currently support 2, 8, and 16 even though they are shown.</span></span>

<span data-ttu-id="7c80c-139">Le implementazioni possono scegliere di supportare 2, 8 e/o 16 modalità di anti-aliasing di esempio multisample (MSAA) per le risorse non affiancate, anche se la risorsa affiancata non le supporta.</span><span class="sxs-lookup"><span data-stu-id="7c80c-139">Implementations can choose to support 2, 8, and/or 16 sample multisample antialiasing (MSAA) mode for non-tiled resources even though tiled resource don't support them.</span></span>

<span data-ttu-id="7c80c-140">Le risorse affiancate con conteggi di esempio maggiori di 1 non possono usare formati di 128 BPP.</span><span class="sxs-lookup"><span data-stu-id="7c80c-140">Tiled resources with sample counts larger than 1 can't use 128 bpp formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c80c-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c80c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c80c-142">Come affiancare l'area di una risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="7c80c-142">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 