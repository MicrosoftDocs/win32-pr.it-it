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
# <a name="volume-tiled-resources"></a>Risorse in riquadri del volume

Le trame di volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione del riquadro è tridimensionale.

-   [Panoramica](#overview)
-   [API delle risorse in riquadri D3D11.3](#d3d113-tiled-resource-apis)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Le risorse affiancate disaccontivano un oggetto risorsa D3D dalla memoria di backup (le risorse in passato avevano una relazione 1:1 con la memoria di backup). Ciò consente un'ampia gamma di scenari interessanti, ad esempio lo streaming dei dati delle trame e il riutilizzo o la riduzione dell'utilizzo della memoria

Le risorse affiancate con trama 2D sono supportate in D3D11.2. D3D12 e D3D11.3 aggiungono il supporto per le trame affiancate 3D.

Le dimensioni tipiche delle risorse usate nell'affiancamento sono 4 x 4 riquadri per trame 2D e 4 x 4 x 4 riquadri per trame 3D.



| Bit/pixel (1 campione/pixel)                            | Dimensioni del riquadro (pixel, w x h x d)                                    |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128x64x16                           |
| BC 2,3,5,6,7                | 64x64x16                            |



 

Si noti che i formati seguenti non sono supportati con le risorse affiancate: formati 96bpp, formati video, R1 \_ UNORM, \_ R8G8 B8G8 \_ UNORM, \_ R8R8 G8B8 \_ UNORM.

Nei diagrammi seguenti il grigio scuro rappresenta i riquadri NULL.

-   [Mapping predefinito della risorsa affiancata trama 3D (mip più dettagliato)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Mapping predefinito della risorsa affiancata Trama 3D (secondo mip più dettagliato)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Risorsa affiancata Trama 3D (mip più dettagliato)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Risorsa affiancata Trama 3D (secondo mip più dettagliato)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Risorsa affiancata Trama 3D (riquadro singolo)](#texture-3d-tiled-resource-single-tile)
-   [Risorsa affiancata Trama 3D (Uniform Box)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Mapping predefinito della risorsa affiancata trama 3D (mip più dettagliato)

![mapping predefinito del mip più dettagliato](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Mapping predefinito della risorsa affiancata Trama 3D (secondo mip più dettagliato)

![mapping predefinito del secondo mip più dettagliato](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Risorsa affiancata Trama 3D (mip più dettagliato)

Il codice seguente configura una risorsa affiancata 3D nel mip più dettagliato.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Risorsa affiancata Trama 3D (secondo mip più dettagliato)

Il codice seguente configura una risorsa affiancata 3D e il secondo mip più dettagliato:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Risorsa affiancata 3D trama (riquadro singolo)

Il codice seguente configura una risorsa Riquadro singolo:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Trama 3D Tiled Resource (Uniform Box)

Il codice seguente configura una risorsa affiancata di Uniform Box (si noti l'istruzione `trSize.bUseBox = true;) :`

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

## <a name="d3d113-tiled-resource-apis"></a>API delle risorse in riquadri D3D11.3

Le stesse chiamate API vengono usate per le risorse affiancate 2D e 3D:

Enumerazioni

-   [**D3D11 \_ LIVELLO RISORSE \_ \_ AFFIANCATE:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) determina il livello di supporto delle risorse affiancate.
-   [**D3D11 \_ FORMAT \_ SUPPORT2:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) usato per testare il supporto delle risorse affiancate.
-   [**D3D11 \_ CHECK \_ MULTISAMPLE \_ QUALITY LEVELS \_ \_ FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determina il supporto delle risorse affiancate in una risorsa a campionamento multiplo.
-   [**D3D11 \_ TILE \_ COPY \_ FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contiene i flag per la copia da e verso le risorse affiancate e i buffer lineari.

Strutture

-   [**D3D11 \_ TILED \_ RESOURCE \_ COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contiene il riferimento alla coordinata x, y e z e alla sottorisorsa. Si noti che è presente una classe helper: CD3D11 \_ TILED \_ RESOURCE \_ COORDINATE.
-   [**D3D11 \_ TILE \_ REGION \_ SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifica le dimensioni e il numero di riquadri dell'area affiancata.
-   [**D3D11 \_ TILE \_ SHAPE:**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) forma del riquadro come larghezza, altezza e profondità in texel.
-   [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)contiene il livello di risorsa riquadro supportato.

Metodi

-   [**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) usato per determinare quali funzionalità e a quale livello sono supportate dall'hardware corrente.
-   [**ID3D11DeviceContext2::CopyTiles:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) copia i riquadri dal buffer alla risorsa affiancata o viceversa.
-   [**ID3D11DeviceContext2::UpdateTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) aggiorna i mapping delle posizioni dei riquadri nelle risorse affiancate alle posizioni di memoria in un pool di riquadri.
-   [**ID3D11DeviceContext2::CopyTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) copia i mapping da una risorsa affiancata di origine a una risorsa affiancata di destinazione.
-   [**ID3D11DeviceContext2::GetResourceTiling:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) ottiene informazioni su come una risorsa affiancata viene suddivisa in riquadri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11.3](direct3d-11-3-features.md)
</dt> </dl>

 

 




