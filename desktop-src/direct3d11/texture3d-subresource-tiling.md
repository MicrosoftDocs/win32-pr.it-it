---
title: Divisione in riquadri di sottorisorse Texture3D
description: Questa tabella Mostra come affiancare le sottorisorse di Texture3D.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993605"
---
# <a name="texture3d-subresource-tiling"></a><span data-ttu-id="06870-103">Divisione in riquadri di sottorisorse Texture3D</span><span class="sxs-lookup"><span data-stu-id="06870-103">Texture3D subresource tiling</span></span>

<span data-ttu-id="06870-104">Questa tabella Mostra come affiancare le sottorisorse di [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) .</span><span class="sxs-lookup"><span data-stu-id="06870-104">This table shows how [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) subresources are tiled.</span></span> <span data-ttu-id="06870-105">I valori in questa tabella non contano la compressione della parte finale MIP.</span><span class="sxs-lookup"><span data-stu-id="06870-105">The values in this table don't count tail mip packing.</span></span>

<span data-ttu-id="06870-106">Questa tabella prende il [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) di affiancamento e divide le dimensioni x/y di 4 ciascuna e aggiunge 16 livelli di profondità.</span><span class="sxs-lookup"><span data-stu-id="06870-106">This table takes the [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) tiling and divides the x/y dimensions by 4 each and adds 16 layers of depth.</span></span> <span data-ttu-id="06870-107">Tutti i riquadri per il primo piano (piano 2D dei riquadri che definiscono i primi 16 livelli di profondità) vengono visualizzati prima dei piani successivi.</span><span class="sxs-lookup"><span data-stu-id="06870-107">All the tiles for the first plane (2D plane of tiles defining the first 16 layers of depth) appear before the subsequent planes.</span></span>

> [!Note]  
> <span data-ttu-id="06870-108">Il supporto di [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) nelle risorse affiancate non viene esposto nell'implementazione iniziale delle risorse affiancate, ma le forme dei riquadri desiderate sono elencate qui perché il supporto potrebbe essere considerato in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="06870-108">[**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) support in tiled resources isn't exposed in the initial implementation of tiled resources, but the desired tile shapes are listed here because support might be consideration in a future release.</span></span>

 



| <span data-ttu-id="06870-109">Bits/pixel (1 campione/pixel)</span><span class="sxs-lookup"><span data-stu-id="06870-109">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="06870-110">Dimensioni riquadro (pixel, LxAxP)</span><span class="sxs-lookup"><span data-stu-id="06870-110">Tile Dimensions (Pixels, WxHxD)</span></span> |
|-----------------------------|---------------------------------|
| <span data-ttu-id="06870-111">8</span><span class="sxs-lookup"><span data-stu-id="06870-111">8</span></span>                           | <span data-ttu-id="06870-112">64x32x32</span><span class="sxs-lookup"><span data-stu-id="06870-112">64x32x32</span></span>                        |
| <span data-ttu-id="06870-113">16</span><span class="sxs-lookup"><span data-stu-id="06870-113">16</span></span>                          | <span data-ttu-id="06870-114">32x32x32</span><span class="sxs-lookup"><span data-stu-id="06870-114">32x32x32</span></span>                        |
| <span data-ttu-id="06870-115">32</span><span class="sxs-lookup"><span data-stu-id="06870-115">32</span></span>                          | <span data-ttu-id="06870-116">32x32x16</span><span class="sxs-lookup"><span data-stu-id="06870-116">32x32x16</span></span>                        |
| <span data-ttu-id="06870-117">64</span><span class="sxs-lookup"><span data-stu-id="06870-117">64</span></span>                          | <span data-ttu-id="06870-118">32x16x16</span><span class="sxs-lookup"><span data-stu-id="06870-118">32x16x16</span></span>                        |
| <span data-ttu-id="06870-119">128</span><span class="sxs-lookup"><span data-stu-id="06870-119">128</span></span>                         | <span data-ttu-id="06870-120">16x16x16</span><span class="sxs-lookup"><span data-stu-id="06870-120">16x16x16</span></span>                        |
| <span data-ttu-id="06870-121">BC1, 4</span><span class="sxs-lookup"><span data-stu-id="06870-121">BC1,4</span></span>                       | <span data-ttu-id="06870-122">128x64x16</span><span class="sxs-lookup"><span data-stu-id="06870-122">128x64x16</span></span>                       |
| <span data-ttu-id="06870-123">BC2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="06870-123">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="06870-124">64x64x16</span><span class="sxs-lookup"><span data-stu-id="06870-124">64x64x16</span></span>                        |



 

<span data-ttu-id="06870-125">I conteggi dei bit di formato non supportati con le risorse affiancate sono formati di 96 BPP, formati video, \_ formato DXGI \_ R1 \_ UNORM, \_ formato DXGI \_ R8G8 B8G8 UNORM \_ \_ e \_ formato DXGI \_ \_ \_ R8R8 G8B8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="06870-125">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06870-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06870-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06870-127">Come affiancare l'area di una risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="06870-127">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 