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
# <a name="volume-tiled-resources-direct3d-12"></a>Risorse affiancate al volume (Direct3D 12)

Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.

-   [Overview](#overview)
-   [API di risorse affiancate](#tiled-resource-apis)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Le risorse affiancate disaccoppiano un oggetto risorsa D3D dalla memoria di supporto (le risorse in passato hanno una relazione 1:1 con la relativa memoria di backup). Ciò consente un'ampia gamma di scenari interessanti, ad esempio il flusso di dati di trama e il riutilizzo o la riduzione dell'utilizzo della memoria.

le risorse affiancate con trama 2D sono supportate in D3D 11.2. È disponibile il supporto facoltativo per le trame 3D affiancate per D3D12 e D3D 11.3 (vedere il [**\_ \_ \_ livello di risorse affiancate D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

Le dimensioni tipiche delle risorse utilizzate nell'affiancamento sono 4 x 4 riquadri per le trame 2D e 4 x 4 x 4 riquadri per le trame 3D.



| Bits/pixel (1 campione/pixel) | Dimensioni riquadro (pixel, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1, 4                      | 128x64x16                           |
| BC 2, 3, 5, 6, 7                | 64x64x16                            |

Si noti che i formati seguenti non sono supportati con le risorse affiancate: formati 96bpp, formati video, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 UNORM \_ .

Nei diagrammi sotto il grigio scuro rappresenta i riquadri NULL.

-   [Trama mapping predefinito della risorsa affiancata 3D (MIP più dettagliato)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Trama-mapping predefinito della risorsa affiancata 3D (seconda MIP più dettagliata)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Trama-risorsa affiancata 3D (MIP più dettagliato)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Trama-risorsa affiancata 3D (seconda MIP più dettagliata)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Trama-risorsa affiancata 3D (riquadro singolo)](#texture-3d-tiled-resource-single-tile)
-   [Trama-risorsa affiancata 3D (casella uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Trama mapping predefinito della risorsa affiancata 3D (MIP più dettagliato)

![mapping predefinito di una risorsa 3D affiancata](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Trama-mapping predefinito della risorsa affiancata 3D (seconda MIP più dettagliata)

![Mostra la seconda MIP più dettagliata](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Trama-risorsa affiancata 3D (MIP più dettagliato)

Il codice seguente configura una risorsa affiancata 3D al MIP più dettagliato.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Trama-risorsa affiancata 3D (seconda MIP più dettagliata)

Il codice seguente configura una risorsa affiancata 3D e il secondo MIP più dettagliato:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Trama-risorsa affiancata 3D (riquadro singolo)

Il codice seguente consente di configurare una singola risorsa di sezione:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Trama-risorsa affiancata 3D (casella uniforme)

Il codice seguente consente di configurare una risorsa affiancata di box (nota l'istruzione). `trSize.bUseBox = true;) :`

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

## <a name="tiled-resource-apis"></a>API di risorse affiancate

Le stesse chiamate API vengono usate per le risorse affiancate 2D e 3D:

Enumerazioni

-   [**D3D12 \_ Livello \_ risorse \_ affiancate**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determina il livello di supporto delle risorse affiancate.
-   [**D3D12 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : usato per verificare il supporto delle risorse affiancate.
-   [**D3D12 \_ \_ \_ \_ Flag del livello di qualità multicampione**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determina il supporto delle risorse affiancate in una risorsa di campionamento multiplo.
-   [**D3D12 \_ \_ \_ Flag di copia dei riquadri**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : include i flag per la copia da e verso le risorse swizzled affiancate e i buffer lineari.

Struct

-   [**D3D12 \_ \_ \_ Coordinata della risorsa affiancata**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : include le coordinate x, y e z e il riferimento alla sottorisorsa. Si noti che è presente una struttura helper [**: \_ \_ \_ coordinata di risorsa CD3DX12 affiancata**](cd3dx12-tiled-resource-coordinate.md).
-   [**D3D12 \_ \_ \_ Dimensioni area affiancata**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifica le dimensioni e il numero di riquadri dell'area affiancata.
-   [**D3D12 \_ \_Forma sezione**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : la forma sezione come larghezza, altezza e profondità nei Texel.
-   [**D3D12 \_ \_Opzioni di \_ D3D12 \_ dei dati della funzionalità**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : include il livello di livello risorse del riquadro supportato e un valore booleano, *VolumeTiledResourcesSupported*, che indica se le risorse affiancate del volume sono supportate.

Metodi

-   [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : usato per determinare quali funzionalità e a quale livello sono supportate dall'hardware corrente.
-   [**ID3D12GraphcisCommandList:: CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copia i riquadri dal buffer alla risorsa affiancata o viceversa.
-   [**ID3D12CommandQueue:: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : Aggiorna i mapping dei percorsi dei riquadri nelle risorse affiancate alle posizioni di memoria in un heap delle risorse.
-   [**ID3D12CommandQueue:: CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copia i mapping da una risorsa di origine affiancata a una risorsa affiancata di destinazione.
-   [**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : ottiene informazioni sul modo in cui una risorsa affiancata viene suddivisa in riquadri.

## <a name="related-topics"></a>Argomenti correlati
* [Associazione di risorse](resource-binding.md)
