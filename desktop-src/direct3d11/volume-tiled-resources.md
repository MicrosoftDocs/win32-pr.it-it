---
title: Risorse affiancate del volume (grafica Direct3D 11)
description: Informazioni su come usare trame di volume (3D) come risorse affiancate. Si noti che la risoluzione del riquadro è tridimensionale.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf9b3ed8b1db89d9718fa904eefd23ce2e871db
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335435"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="087e9-104">Risorse in riquadri del volume</span><span class="sxs-lookup"><span data-stu-id="087e9-104">Volume Tiled Resources</span></span>

<span data-ttu-id="087e9-105">Le trame di volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione del riquadro è tridimensionale.</span><span class="sxs-lookup"><span data-stu-id="087e9-105">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="087e9-106">Panoramica</span><span class="sxs-lookup"><span data-stu-id="087e9-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="087e9-107">API delle risorse in riquadri D3D11.3</span><span class="sxs-lookup"><span data-stu-id="087e9-107">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="087e9-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="087e9-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="087e9-109">Panoramica</span><span class="sxs-lookup"><span data-stu-id="087e9-109">Overview</span></span>

<span data-ttu-id="087e9-110">Le risorse affiancate disaccontivano un oggetto risorsa D3D dalla memoria di backup (le risorse in passato avevano una relazione 1:1 con la memoria di backup).</span><span class="sxs-lookup"><span data-stu-id="087e9-110">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="087e9-111">Ciò consente un'ampia gamma di scenari interessanti, ad esempio lo streaming dei dati delle trame e il riutilizzo o la riduzione dell'utilizzo della memoria</span><span class="sxs-lookup"><span data-stu-id="087e9-111">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="087e9-112">Le risorse affiancate con trama 2D sono supportate in D3D11.2.</span><span class="sxs-lookup"><span data-stu-id="087e9-112">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="087e9-113">D3D12 e D3D11.3 aggiungono il supporto per le trame affiancate 3D.</span><span class="sxs-lookup"><span data-stu-id="087e9-113">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="087e9-114">Le dimensioni tipiche delle risorse usate nell'affiancamento sono 4 x 4 riquadri per trame 2D e 4 x 4 x 4 riquadri per trame 3D.</span><span class="sxs-lookup"><span data-stu-id="087e9-114">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="087e9-115">Bit/pixel (1 campione/pixel)</span><span class="sxs-lookup"><span data-stu-id="087e9-115">Bits/pixel (1 sample/pixel)</span></span>                            | <span data-ttu-id="087e9-116">Dimensioni del riquadro (pixel, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="087e9-116">Tile dimensions (pixels, w x h x d)</span></span>                                    |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="087e9-117">8</span><span class="sxs-lookup"><span data-stu-id="087e9-117">8</span></span>                           | <span data-ttu-id="087e9-118">64x32x32</span><span class="sxs-lookup"><span data-stu-id="087e9-118">64x32x32</span></span>                            |
| <span data-ttu-id="087e9-119">16</span><span class="sxs-lookup"><span data-stu-id="087e9-119">16</span></span>                          | <span data-ttu-id="087e9-120">32x32x32</span><span class="sxs-lookup"><span data-stu-id="087e9-120">32x32x32</span></span>                            |
| <span data-ttu-id="087e9-121">32</span><span class="sxs-lookup"><span data-stu-id="087e9-121">32</span></span>                          | <span data-ttu-id="087e9-122">32x32x16</span><span class="sxs-lookup"><span data-stu-id="087e9-122">32x32x16</span></span>                            |
| <span data-ttu-id="087e9-123">64</span><span class="sxs-lookup"><span data-stu-id="087e9-123">64</span></span>                          | <span data-ttu-id="087e9-124">32x16x16</span><span class="sxs-lookup"><span data-stu-id="087e9-124">32x16x16</span></span>                            |
| <span data-ttu-id="087e9-125">128</span><span class="sxs-lookup"><span data-stu-id="087e9-125">128</span></span>                         | <span data-ttu-id="087e9-126">16x16x16</span><span class="sxs-lookup"><span data-stu-id="087e9-126">16x16x16</span></span>                            |
| <span data-ttu-id="087e9-127">BC 1,4</span><span class="sxs-lookup"><span data-stu-id="087e9-127">BC 1,4</span></span>                      | <span data-ttu-id="087e9-128">128x64x16</span><span class="sxs-lookup"><span data-stu-id="087e9-128">128x64x16</span></span>                           |
| <span data-ttu-id="087e9-129">BC 2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="087e9-129">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="087e9-130">64x64x16</span><span class="sxs-lookup"><span data-stu-id="087e9-130">64x64x16</span></span>                            |



 

<span data-ttu-id="087e9-131">Si noti che i formati seguenti non sono supportati con le risorse affiancate: formati 96bpp, formati video, R1 \_ UNORM, \_ R8G8 B8G8 \_ UNORM, \_ R8R8 G8B8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="087e9-131">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="087e9-132">Nei diagrammi seguenti il grigio scuro rappresenta i riquadri NULL.</span><span class="sxs-lookup"><span data-stu-id="087e9-132">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="087e9-133">Mapping predefinito della risorsa affiancata trama 3D (mip più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="087e9-133">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="087e9-134">Mapping predefinito della risorsa affiancata Trama 3D (secondo mip più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="087e9-134">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="087e9-135">Risorsa affiancata Trama 3D (mip più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="087e9-135">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="087e9-136">Risorsa affiancata Trama 3D (secondo mip più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="087e9-136">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="087e9-137">Risorsa affiancata Trama 3D (riquadro singolo)</span><span class="sxs-lookup"><span data-stu-id="087e9-137">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="087e9-138">Risorsa affiancata Trama 3D (Uniform Box)</span><span class="sxs-lookup"><span data-stu-id="087e9-138">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="087e9-139">Mapping predefinito della risorsa affiancata trama 3D (mip più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="087e9-139">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![mapping predefinito del mip più dettagliato](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="087e9-141">Mapping predefinito della risorsa affiancata Trama 3D (secondo mip più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="087e9-141">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![mapping predefinito del secondo mip più dettagliato](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="087e9-143">Risorsa affiancata Trama 3D (mip più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="087e9-143">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="087e9-144">Il codice seguente configura una risorsa affiancata 3D nel mip più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="087e9-144">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![mapping più dettagliato di una risorsa affiancata 3D](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="087e9-146">Risorsa affiancata Trama 3D (secondo mip più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="087e9-146">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="087e9-147">Il codice seguente configura una risorsa affiancata 3D e il secondo mip più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="087e9-147">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![secondo mapping più dettagliato di una risorsa affiancata 3d](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="087e9-149">Risorsa affiancata 3D trama (riquadro singolo)</span><span class="sxs-lookup"><span data-stu-id="087e9-149">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="087e9-150">Il codice seguente configura una risorsa Riquadro singolo:</span><span class="sxs-lookup"><span data-stu-id="087e9-150">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![un singolo riquadro](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="087e9-152">Trama 3D Tiled Resource (Uniform Box)</span><span class="sxs-lookup"><span data-stu-id="087e9-152">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="087e9-153">Il codice seguente configura una risorsa affiancata di Uniform Box (si noti l'istruzione `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="087e9-153">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![una casella uniforme](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="087e9-155">API delle risorse in riquadri D3D11.3</span><span class="sxs-lookup"><span data-stu-id="087e9-155">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="087e9-156">Le stesse chiamate API vengono usate per le risorse affiancate 2D e 3D:</span><span class="sxs-lookup"><span data-stu-id="087e9-156">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="087e9-157">Enumerazioni</span><span class="sxs-lookup"><span data-stu-id="087e9-157">Enums</span></span>

-   <span data-ttu-id="087e9-158">[**D3D11 \_ LIVELLO RISORSE \_ \_ AFFIANCATE:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) determina il livello di supporto delle risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="087e9-158">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="087e9-159">[**D3D11 \_ FORMAT \_ SUPPORT2:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) usato per testare il supporto delle risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="087e9-159">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="087e9-160">[**D3D11 \_ CHECK \_ MULTISAMPLE \_ QUALITY LEVELS \_ \_ FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determina il supporto delle risorse affiancate in una risorsa a campionamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="087e9-160">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="087e9-161">[**D3D11 \_ TILE \_ COPY \_ FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contiene i flag per la copia da e verso le risorse affiancate e i buffer lineari.</span><span class="sxs-lookup"><span data-stu-id="087e9-161">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="087e9-162">Strutture</span><span class="sxs-lookup"><span data-stu-id="087e9-162">Structures</span></span>

-   <span data-ttu-id="087e9-163">[**D3D11 \_ TILED \_ RESOURCE \_ COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contiene il riferimento alla coordinata x, y e z e alla sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="087e9-163">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="087e9-164">Si noti che è presente una classe helper: CD3D11 \_ TILED \_ RESOURCE \_ COORDINATE.</span><span class="sxs-lookup"><span data-stu-id="087e9-164">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="087e9-165">[**D3D11 \_ TILE \_ REGION \_ SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifica le dimensioni e il numero di riquadri dell'area affiancata.</span><span class="sxs-lookup"><span data-stu-id="087e9-165">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="087e9-166">[**D3D11 \_ TILE \_ SHAPE:**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) forma del riquadro come larghezza, altezza e profondità in texel.</span><span class="sxs-lookup"><span data-stu-id="087e9-166">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="087e9-167">[**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)contiene il livello di risorsa riquadro supportato.</span><span class="sxs-lookup"><span data-stu-id="087e9-167">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="087e9-168">Metodi</span><span class="sxs-lookup"><span data-stu-id="087e9-168">Methods</span></span>

-   <span data-ttu-id="087e9-169">[**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) usato per determinare quali funzionalità e a quale livello sono supportate dall'hardware corrente.</span><span class="sxs-lookup"><span data-stu-id="087e9-169">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="087e9-170">[**ID3D11DeviceContext2::CopyTiles:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) copia i riquadri dal buffer alla risorsa affiancata o viceversa.</span><span class="sxs-lookup"><span data-stu-id="087e9-170">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="087e9-171">[**ID3D11DeviceContext2::UpdateTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) aggiorna i mapping delle posizioni dei riquadri nelle risorse affiancate alle posizioni di memoria in un pool di riquadri.</span><span class="sxs-lookup"><span data-stu-id="087e9-171">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="087e9-172">[**ID3D11DeviceContext2::CopyTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) copia i mapping da una risorsa affiancata di origine a una risorsa affiancata di destinazione.</span><span class="sxs-lookup"><span data-stu-id="087e9-172">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="087e9-173">[**ID3D11DeviceContext2::GetResourceTiling:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) ottiene informazioni su come una risorsa affiancata viene suddivisa in riquadri.</span><span class="sxs-lookup"><span data-stu-id="087e9-173">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="087e9-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="087e9-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="087e9-175">Funzionalità di Direct3D 11.3</span><span class="sxs-lookup"><span data-stu-id="087e9-175">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




