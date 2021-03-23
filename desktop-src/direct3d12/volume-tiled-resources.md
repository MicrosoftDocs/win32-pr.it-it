---
title: Risorse affiancate al volume (Direct3D 12)
description: Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42679155bbd8dc2cec560d2724e430c860f54bc0
ms.sourcegitcommit: 05e7efd3d8de6926d08802669f37e825a2fa2f46
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2020
ms.locfileid: "104548792"
---
# <a name="volume-tiled-resources-direct3d-12"></a><span data-ttu-id="af160-103">Risorse affiancate al volume (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="af160-103">Volume tiled resources (Direct3D 12)</span></span>

<span data-ttu-id="af160-104">Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.</span><span class="sxs-lookup"><span data-stu-id="af160-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="af160-105">Overview</span><span class="sxs-lookup"><span data-stu-id="af160-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="af160-106">API di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="af160-106">Tiled Resource APIs</span></span>](#tiled-resource-apis)
-   [<span data-ttu-id="af160-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af160-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="af160-108">Panoramica</span><span class="sxs-lookup"><span data-stu-id="af160-108">Overview</span></span>

<span data-ttu-id="af160-109">Le risorse affiancate disaccoppiano un oggetto risorsa D3D dalla memoria di supporto (le risorse in passato hanno una relazione 1:1 con la relativa memoria di backup).</span><span class="sxs-lookup"><span data-stu-id="af160-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="af160-110">Ciò consente un'ampia gamma di scenari interessanti, ad esempio il flusso di dati di trama e il riutilizzo o la riduzione dell'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="af160-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage.</span></span>

<span data-ttu-id="af160-111">le risorse affiancate con trama 2D sono supportate in D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="af160-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="af160-112">È disponibile il supporto facoltativo per le trame 3D affiancate per D3D12 e D3D 11.3 (vedere il [**\_ \_ \_ livello di risorse affiancate D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span><span class="sxs-lookup"><span data-stu-id="af160-112">Optional support for 3D tiled textures is available for D3D12 and D3D11.3 (refer to [**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span></span>

<span data-ttu-id="af160-113">Le dimensioni tipiche delle risorse utilizzate nell'affiancamento sono 4 x 4 riquadri per le trame 2D e 4 x 4 x 4 riquadri per le trame 3D.</span><span class="sxs-lookup"><span data-stu-id="af160-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="af160-114">Bits/pixel (1 campione/pixel)</span><span class="sxs-lookup"><span data-stu-id="af160-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="af160-115">Dimensioni riquadro (pixel, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="af160-115">Tile dimensions (pixels, w x h x d)</span></span> |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="af160-116">8</span><span class="sxs-lookup"><span data-stu-id="af160-116">8</span></span>                           | <span data-ttu-id="af160-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="af160-117">64x32x32</span></span>                            |
| <span data-ttu-id="af160-118">16</span><span class="sxs-lookup"><span data-stu-id="af160-118">16</span></span>                          | <span data-ttu-id="af160-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="af160-119">32x32x32</span></span>                            |
| <span data-ttu-id="af160-120">32</span><span class="sxs-lookup"><span data-stu-id="af160-120">32</span></span>                          | <span data-ttu-id="af160-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="af160-121">32x32x16</span></span>                            |
| <span data-ttu-id="af160-122">64</span><span class="sxs-lookup"><span data-stu-id="af160-122">64</span></span>                          | <span data-ttu-id="af160-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="af160-123">32x16x16</span></span>                            |
| <span data-ttu-id="af160-124">128</span><span class="sxs-lookup"><span data-stu-id="af160-124">128</span></span>                         | <span data-ttu-id="af160-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="af160-125">16x16x16</span></span>                            |
| <span data-ttu-id="af160-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="af160-126">BC 1,4</span></span>                      | <span data-ttu-id="af160-127">128x64x16</span><span class="sxs-lookup"><span data-stu-id="af160-127">128x64x16</span></span>                           |
| <span data-ttu-id="af160-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="af160-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="af160-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="af160-129">64x64x16</span></span>                            |

<span data-ttu-id="af160-130">Si noti che i formati seguenti non sono supportati con le risorse affiancate: formati 96bpp, formati video, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 UNORM \_ .</span><span class="sxs-lookup"><span data-stu-id="af160-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="af160-131">Nei diagrammi sotto il grigio scuro rappresenta i riquadri NULL.</span><span class="sxs-lookup"><span data-stu-id="af160-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="af160-132">Trama mapping predefinito della risorsa affiancata 3D (MIP più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="af160-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="af160-133">Trama-mapping predefinito della risorsa affiancata 3D (seconda MIP più dettagliata)</span><span class="sxs-lookup"><span data-stu-id="af160-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="af160-134">Trama-risorsa affiancata 3D (MIP più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="af160-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="af160-135">Trama-risorsa affiancata 3D (seconda MIP più dettagliata)</span><span class="sxs-lookup"><span data-stu-id="af160-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="af160-136">Trama-risorsa affiancata 3D (riquadro singolo)</span><span class="sxs-lookup"><span data-stu-id="af160-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="af160-137">Trama-risorsa affiancata 3D (casella uniforme)</span><span class="sxs-lookup"><span data-stu-id="af160-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="af160-138">Trama mapping predefinito della risorsa affiancata 3D (MIP più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="af160-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![mapping predefinito di una risorsa 3D affiancata](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="af160-140">Trama-mapping predefinito della risorsa affiancata 3D (seconda MIP più dettagliata)</span><span class="sxs-lookup"><span data-stu-id="af160-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![Mostra la seconda MIP più dettagliata](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="af160-142">Trama-risorsa affiancata 3D (MIP più dettagliato)</span><span class="sxs-lookup"><span data-stu-id="af160-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="af160-143">Il codice seguente configura una risorsa affiancata 3D al MIP più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="af160-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![MIP più dettagliato per una trama tridimensionale](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="af160-145">Trama-risorsa affiancata 3D (seconda MIP più dettagliata)</span><span class="sxs-lookup"><span data-stu-id="af160-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="af160-146">Il codice seguente configura una risorsa affiancata 3D e il secondo MIP più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="af160-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![secondo MIP più dettagliato per una trama tridimensionale](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="af160-148">Trama-risorsa affiancata 3D (riquadro singolo)</span><span class="sxs-lookup"><span data-stu-id="af160-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="af160-149">Il codice seguente consente di configurare una singola risorsa di sezione:</span><span class="sxs-lookup"><span data-stu-id="af160-149">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![una singola risorsa tridimensionale affiancata](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="af160-151">Trama-risorsa affiancata 3D (casella uniforme)</span><span class="sxs-lookup"><span data-stu-id="af160-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="af160-152">Il codice seguente consente di configurare una risorsa affiancata di box (nota l'istruzione). `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="af160-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![casella uniforme](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a><span data-ttu-id="af160-154">API di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="af160-154">Tiled Resource APIs</span></span>

<span data-ttu-id="af160-155">Le stesse chiamate API vengono usate per le risorse affiancate 2D e 3D:</span><span class="sxs-lookup"><span data-stu-id="af160-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="af160-156">Enumerazioni</span><span class="sxs-lookup"><span data-stu-id="af160-156">Enums</span></span>

-   <span data-ttu-id="af160-157">[**D3D12 \_ Livello \_ risorse \_ affiancate**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determina il livello di supporto delle risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="af160-157">[**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="af160-158">[**D3D12 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : usato per verificare il supporto delle risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="af160-158">[**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="af160-159">[**D3D12 \_ \_ \_ \_ Flag del livello di qualità multicampione**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determina il supporto delle risorse affiancate in una risorsa di campionamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="af160-159">[**D3D12\_MULTISAMPLE\_QUALITY\_LEVEL\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="af160-160">[**D3D12 \_ \_ \_ Flag di copia dei riquadri**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : include i flag per la copia da e verso le risorse swizzled affiancate e i buffer lineari.</span><span class="sxs-lookup"><span data-stu-id="af160-160">[**D3D12\_TILE\_COPY\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="af160-161">Struct</span><span class="sxs-lookup"><span data-stu-id="af160-161">Structs</span></span>

-   <span data-ttu-id="af160-162">[**D3D12 \_ \_ \_ Coordinata della risorsa affiancata**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : include le coordinate x, y e z e il riferimento alla sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="af160-162">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="af160-163">Si noti che è presente una struttura helper [**: \_ \_ \_ coordinata di risorsa CD3DX12 affiancata**](cd3dx12-tiled-resource-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="af160-163">Note there is a helper structure: [**CD3DX12\_TILED\_RESOURCE\_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).</span></span>
-   <span data-ttu-id="af160-164">[**D3D12 \_ \_ \_ Dimensioni area affiancata**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifica le dimensioni e il numero di riquadri dell'area affiancata.</span><span class="sxs-lookup"><span data-stu-id="af160-164">[**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="af160-165">[**D3D12 \_ \_Forma sezione**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : la forma sezione come larghezza, altezza e profondità nei Texel.</span><span class="sxs-lookup"><span data-stu-id="af160-165">[**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="af160-166">[**D3D12 \_ \_Opzioni di \_ D3D12 \_ dei dati della funzionalità**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : include il livello di livello risorse del riquadro supportato e un valore booleano, *VolumeTiledResourcesSupported*, che indica se le risorse affiancate del volume sono supportate.</span><span class="sxs-lookup"><span data-stu-id="af160-166">[**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : holds the supported tile resource tier level and a boolean, *VolumeTiledResourcesSupported*, indicated whether volume tiled resources are supported.</span></span>

<span data-ttu-id="af160-167">Metodi</span><span class="sxs-lookup"><span data-stu-id="af160-167">Methods</span></span>

-   <span data-ttu-id="af160-168">[**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : usato per determinare quali funzionalità e a quale livello sono supportate dall'hardware corrente.</span><span class="sxs-lookup"><span data-stu-id="af160-168">[**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="af160-169">[**ID3D12GraphcisCommandList:: CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copia i riquadri dal buffer alla risorsa affiancata o viceversa.</span><span class="sxs-lookup"><span data-stu-id="af160-169">[**ID3D12GraphcisCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="af160-170">[**ID3D12CommandQueue:: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : Aggiorna i mapping dei percorsi dei riquadri nelle risorse affiancate alle posizioni di memoria in un heap delle risorse.</span><span class="sxs-lookup"><span data-stu-id="af160-170">[**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a resource heap.</span></span>
-   <span data-ttu-id="af160-171">[**ID3D12CommandQueue:: CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copia i mapping da una risorsa di origine affiancata a una risorsa affiancata di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af160-171">[**ID3D12CommandQueue::CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="af160-172">[**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : ottiene informazioni sul modo in cui una risorsa affiancata viene suddivisa in riquadri.</span><span class="sxs-lookup"><span data-stu-id="af160-172">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af160-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af160-173">Related topics</span></span>
* [<span data-ttu-id="af160-174">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="af160-174">Resource Binding</span></span>](resource-binding.md)
