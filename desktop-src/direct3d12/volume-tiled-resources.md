---
title: Risorse affiancate del volume (Direct3D 12)
description: Le trame di volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d6e9b4d7ae9ad4b93bae5cf29749c293bf7f55ea7fa35a1e1ca71040218e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123512"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Risorse affiancate del volume (Direct3D 12)

Le trame di volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.

## <a name="overview"></a>Panoramica

Le risorse affiancate disaccoccollano un oggetto risorsa Direct3D dalla memoria di backup (le risorse in passato avevano una relazione 1:1 con la memoria di backup). Ciò consente un'ampia gamma di scenari interessanti, ad esempio lo streaming dei dati di trama e il riutilizzo o la riduzione dell'utilizzo della memoria.

Le risorse affiancate con trama 2D sono supportate in Direct3D 11.2. Il supporto facoltativo per le trame affiancate 3D è disponibile per Direct3D 12 e Direct3D 11.3 (vedere [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

Le dimensioni tipiche delle risorse usate nella affiancamento sono 4 x 4 riquadri per le trame 2D e 4 x 4 x 4 riquadri per le trame 3D.

| Bit/pixel (1 campione/pixel) | Dimensioni del riquadro (pixel, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128x64x16                           |
| BC 2,3,5,6,7                | 64x64x16                            |

Si noti che i formati seguenti non sono supportati con le risorse affiancate: formati 96bpp, formati video, **R1_UNORM**, **R8G8_B8G8_UNORM**, **R8R8_G8B8_UNORM**.

Nei diagrammi seguenti il grigio scuro rappresenta i riquadri NULL.

* [Mapping predefinito della risorsa affiancata trama 3D (mip più dettagliato)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [Mapping predefinito della risorsa affiancata Trama 3D (secondo mip più dettagliato)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [Risorsa affiancata Trama 3D (mip più dettagliato)](#texture-3d-tiled-resource-most-detailed-mip)
* [Risorsa affiancata Trama 3D (secondo mip più dettagliato)](#texture-3d-tiled-resource-second-most-detailed-mip)
* [Risorsa affiancata Trama 3D (riquadro singolo)](#texture-3d-tiled-resource-single-tile)
* [Risorsa affiancata Trama 3D (Uniform Box)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Mapping predefinito delle risorse affiancate texture 3D (mip più dettagliato)

![mapping predefinito di una risorsa tridimensionale affiancata](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Mapping predefinito delle risorse affiancate texture 3D (secondo mip più dettagliato)

![mostra il secondo mip più dettagliato](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Risorsa affiancata Trama 3D (mip più dettagliato)

Il codice seguente configura una risorsa affiancata 3D nel mip più dettagliato.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord{};
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize{};
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![mip più dettagliato per una trama tridimensionale](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Risorsa affiancata Trama 3D (secondo mip più dettagliato)

Il codice seguente configura una risorsa affiancata 3D e il secondo mip più dettagliato.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![secondo mip più dettagliato per una trama tridimensionale](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Risorsa affiancata Trama 3D (riquadro singolo)

Il codice seguente configura una singola risorsa riquadro.

```cpp
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

![una risorsa tridimensionale a riquadro singolo](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Risorsa affiancata Trama 3D (riquadro uniforme)

Il codice seguente configura una risorsa affiancata uniforme (si noti l'istruzione `trSize.bUseBox = true;) :`

```cpp
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

![una casella uniforme](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a>API delle risorse affiancate

Le stesse chiamate API vengono usate per le risorse affiancate 2D e 3D.

Enumerazioni

* [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determina il livello di supporto delle risorse affiancate.
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) : usato per testare il supporto delle risorse affiancate.
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determina il supporto delle risorse affiancate in una risorsa con campionamento multiplo.
* [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : contiene i flag per la copia da e verso risorse affiancate con swizzle e buffer lineari.

Struct

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : contiene le coordinate x, y e z e il riferimento alla sottorisorsa. Si noti che è presente una struttura helper: [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifica le dimensioni e il numero di riquadri dell'area affiancata.
* [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) : forma della tessera come larghezza, altezza e profondità nei texel.
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : contiene il livello di risorse del riquadro supportato e un valore *booleano, VolumeTiledResourcesSupported,* che indica se le risorse affiancate del volume sono supportate.

Metodi

* [**ID3D12Device::CheckFeatureSupport:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) usato per determinare quali funzionalità e a quale livello sono supportate dall'hardware corrente.
* [**ID3D12GraphicsCommandList::CopyTiles:**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) copia i riquadri dal buffer alla risorsa affiancata o viceversa.
* [**ID3D12CommandQueue::UpdateTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) aggiorna i mapping delle posizioni dei riquadri nelle risorse affiancate alle posizioni di memoria in un heap delle risorse.
* [**ID3D12CommandQueue::CopyTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) copia i mapping da una risorsa affiancata di origine a una risorsa affiancata di destinazione.
* [**ID3D12Device::GetResourceTiling:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) ottiene informazioni sul modo in cui una risorsa affiancata viene suddivisa in riquadri.

## <a name="related-topics"></a>Argomenti correlati

* [Associazione di risorse](resource-binding.md)
