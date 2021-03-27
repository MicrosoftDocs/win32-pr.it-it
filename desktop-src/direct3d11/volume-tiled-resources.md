---
title: Risorse affiancate al volume (grafica Direct3D 11)
description: Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb8b35e522ef3298abad1322d6fb7a2fe65bfcf
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "103719282"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="b87d1-103">Risorse affiancate al volume</span><span class="sxs-lookup"><span data-stu-id="b87d1-103">Volume Tiled Resources</span></span>

<span data-ttu-id="b87d1-104">Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.</span><span class="sxs-lookup"><span data-stu-id="b87d1-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="b87d1-105">Overview</span><span class="sxs-lookup"><span data-stu-id="b87d1-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="b87d1-106">API delle risorse affiancate di D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="b87d1-106">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="b87d1-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b87d1-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="b87d1-108">Panoramica</span><span class="sxs-lookup"><span data-stu-id="b87d1-108">Overview</span></span>

<span data-ttu-id="b87d1-109">Le risorse affiancate disaccoppiano un oggetto risorsa D3D dalla memoria di supporto (le risorse in passato hanno una relazione 1:1 con la relativa memoria di backup).</span><span class="sxs-lookup"><span data-stu-id="b87d1-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="b87d1-110">Questo consente un'ampia gamma di scenari interessanti, ad esempio il flusso di dati di trama e il riutilizzo o la riduzione dell'utilizzo della memoria</span><span class="sxs-lookup"><span data-stu-id="b87d1-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="b87d1-111">le risorse affiancate con trama 2D sono supportate in D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="b87d1-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="b87d1-112">D3D12 e D3D 11.3 aggiungono il supporto per le trame 3D affiancate.</span><span class="sxs-lookup"><span data-stu-id="b87d1-112">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="b87d1-113">Le dimensioni tipiche delle risorse utilizzate nell'affiancamento sono 4 x 4 riquadri per le trame 2D e 4 x 4 x 4 riquadri per le trame 3D.</span><span class="sxs-lookup"><span data-stu-id="b87d1-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



|                             |                                     |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="b87d1-114">Bits/pixel (1 campione/pixel)</span><span class="sxs-lookup"><span data-stu-id="b87d1-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="b87d1-115">Dimensioni riquadro (pixel, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="b87d1-115">Tile dimensions (pixels, w x h x d)</span></span> |
| <span data-ttu-id="b87d1-116">8</span><span class="sxs-lookup"><span data-stu-id="b87d1-116">8</span></span>                           | <span data-ttu-id="b87d1-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="b87d1-117">64x32x32</span></span>                            |
| <span data-ttu-id="b87d1-118">16</span><span class="sxs-lookup"><span data-stu-id="b87d1-118">16</span></span>                          | <span data-ttu-id="b87d1-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="b87d1-119">32x32x32</span></span>                            |
| <span data-ttu-id="b87d1-120">32</span><span class="sxs-lookup"><span data-stu-id="b87d1-120">32</span></span>                          | <span data-ttu-id="b87d1-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="b87d1-121">32x32x16</span></span>                            |
| <span data-ttu-id="b87d1-122">64</span><span class="sxs-lookup"><span data-stu-id="b87d1-122">64</span></span>                          | <span data-ttu-id="b87d1-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="b87d1-123">32x16x16</span></span>                            |
| <span data-ttu-id="b87d1-124">128</span><span class="sxs-lookup"><span data-stu-id="b87d1-124">128</span></span>                         | <span data-ttu-id="b87d1-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="b87d1-125">16x16x16</span></span>                            |
| <span data-ttu-id="b87d1-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="b87d1-126">BC 1,4</span></span>                      | <span data-ttu-id="b87d1-127">128x64x16</span><span class="sxs-lookup"><span data-stu-id="b87d1-127">128x64x16</span></span>                           |
| <span data-ttu-id="b87d1-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="b87d1-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="b87d1-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="b87d1-129">64x64x16</span></span>                            |



 

<span data-ttu-id="b87d1-130">Si noti che i formati seguenti non sono supportati con le risorse affiancate: formati 96bpp, formati video, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 UNORM \_ .</span><span class="sxs-lookup"><span data-stu-id="b87d1-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="b87d1-131">Nei diagrammi sotto il grigio scuro rappresenta i riquadri NULL.</span><span class="sxs-lookup"><span data-stu-id="b87d1-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="b87d1-132">Trama mapping predefinito della risorsa affiancata 3D (MIP più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="b87d1-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="b87d1-133">Trama-mapping predefinito della risorsa affiancata 3D (seconda MIP più dettagliata)</span><span class="sxs-lookup"><span data-stu-id="b87d1-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="b87d1-134">Trama-risorsa affiancata 3D (MIP più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="b87d1-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="b87d1-135">Trama-risorsa affiancata 3D (seconda MIP più dettagliata)</span><span class="sxs-lookup"><span data-stu-id="b87d1-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="b87d1-136">Trama-risorsa affiancata 3D (riquadro singolo)</span><span class="sxs-lookup"><span data-stu-id="b87d1-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="b87d1-137">Trama-risorsa affiancata 3D (casella uniforme)</span><span class="sxs-lookup"><span data-stu-id="b87d1-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="b87d1-138">Trama mapping predefinito della risorsa affiancata 3D (MIP più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="b87d1-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![mapping predefinito del MIP più dettagliato](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="b87d1-140">Trama-mapping predefinito della risorsa affiancata 3D (seconda MIP più dettagliata)</span><span class="sxs-lookup"><span data-stu-id="b87d1-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![mapping predefinito del secondo MIP più dettagliato](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="b87d1-142">Trama-risorsa affiancata 3D (MIP più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="b87d1-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="b87d1-143">Il codice seguente configura una risorsa affiancata 3D al MIP più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="b87d1-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="b87d1-145">Trama-risorsa affiancata 3D (seconda MIP più dettagliata)</span><span class="sxs-lookup"><span data-stu-id="b87d1-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="b87d1-146">Il codice seguente configura una risorsa affiancata 3D e il secondo MIP più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="b87d1-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

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

![secondo mapping più dettagliato di una risorsa affiancata 3D](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="b87d1-148">Trama-risorsa affiancata 3D (riquadro singolo)</span><span class="sxs-lookup"><span data-stu-id="b87d1-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="b87d1-149">Il codice seguente consente di configurare una singola risorsa di sezione:</span><span class="sxs-lookup"><span data-stu-id="b87d1-149">The following code sets up a Single Tile resource:</span></span>

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

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="b87d1-151">Trama-risorsa affiancata 3D (casella uniforme)</span><span class="sxs-lookup"><span data-stu-id="b87d1-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="b87d1-152">Il codice seguente consente di configurare una risorsa affiancata di box (nota l'istruzione). `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="b87d1-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

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

![casella uniforme](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="b87d1-154">API delle risorse affiancate di D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="b87d1-154">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="b87d1-155">Le stesse chiamate API vengono usate per le risorse affiancate 2D e 3D:</span><span class="sxs-lookup"><span data-stu-id="b87d1-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="b87d1-156">Enumerazioni</span><span class="sxs-lookup"><span data-stu-id="b87d1-156">Enums</span></span>

-   <span data-ttu-id="b87d1-157">[**D3d11 \_ Livello \_ risorse \_ affiancate**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determina il livello di supporto delle risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="b87d1-157">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="b87d1-158">[**D3d11 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : usato per verificare il supporto delle risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="b87d1-158">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="b87d1-159">[**D3d11 \_ Verifica \_ \_ \_ \_ flag livelli di qualità multicampione**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determina il supporto delle risorse affiancate in una risorsa di campionamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="b87d1-159">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="b87d1-160">[**D3d11 \_ \_ \_ Flag di copia dei riquadri**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : include i flag per la copia da e verso le risorse swizzled affiancate e i buffer lineari.</span><span class="sxs-lookup"><span data-stu-id="b87d1-160">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="b87d1-161">Strutture</span><span class="sxs-lookup"><span data-stu-id="b87d1-161">Structures</span></span>

-   <span data-ttu-id="b87d1-162">[**D3d11 \_ \_ \_ Coordinata della risorsa affiancata**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : include le coordinate x, y e z e il riferimento alla sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="b87d1-162">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="b87d1-163">Si noti che è presente una classe helper: \_ \_ coordinata di risorsa CD3D11 affiancata \_ .</span><span class="sxs-lookup"><span data-stu-id="b87d1-163">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="b87d1-164">[**D3d11 \_ \_ \_ Dimensioni area affiancata**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifica le dimensioni e il numero di riquadri dell'area affiancata.</span><span class="sxs-lookup"><span data-stu-id="b87d1-164">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="b87d1-165">[**D3d11 \_ \_Forma sezione**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : la forma sezione come larghezza, altezza e profondità nei Texel.</span><span class="sxs-lookup"><span data-stu-id="b87d1-165">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="b87d1-166">[**D3d11 \_ FEATURE \_ data \_ d3d11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): include il livello di livello risorse del riquadro supportato.</span><span class="sxs-lookup"><span data-stu-id="b87d1-166">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="b87d1-167">Metodi</span><span class="sxs-lookup"><span data-stu-id="b87d1-167">Methods</span></span>

-   <span data-ttu-id="b87d1-168">[**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : usato per determinare quali funzionalità e a quale livello sono supportate dall'hardware corrente.</span><span class="sxs-lookup"><span data-stu-id="b87d1-168">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="b87d1-169">[**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copia i riquadri dal buffer alla risorsa affiancata o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b87d1-169">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="b87d1-170">[**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : Aggiorna i mapping dei percorsi dei riquadri nelle risorse affiancate alle posizioni di memoria in un pool di sezioni.</span><span class="sxs-lookup"><span data-stu-id="b87d1-170">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="b87d1-171">[**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copia i mapping da una risorsa di origine affiancata a una risorsa affiancata di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b87d1-171">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="b87d1-172">[**ID3D11DeviceContext2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : ottiene informazioni sul modo in cui una risorsa affiancata viene suddivisa in riquadri.</span><span class="sxs-lookup"><span data-stu-id="b87d1-172">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b87d1-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b87d1-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b87d1-174">Funzionalità di Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="b87d1-174">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




