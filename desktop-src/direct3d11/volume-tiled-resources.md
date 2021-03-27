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
# <a name="volume-tiled-resources"></a>Risorse affiancate al volume

Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.

-   [Overview](#overview)
-   [API delle risorse affiancate di D3D 11.3](#d3d113-tiled-resource-apis)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Le risorse affiancate disaccoppiano un oggetto risorsa D3D dalla memoria di supporto (le risorse in passato hanno una relazione 1:1 con la relativa memoria di backup). Questo consente un'ampia gamma di scenari interessanti, ad esempio il flusso di dati di trama e il riutilizzo o la riduzione dell'utilizzo della memoria

le risorse affiancate con trama 2D sono supportate in D3D 11.2. D3D12 e D3D 11.3 aggiungono il supporto per le trame 3D affiancate.

Le dimensioni tipiche delle risorse utilizzate nell'affiancamento sono 4 x 4 riquadri per le trame 2D e 4 x 4 x 4 riquadri per le trame 3D.



|                             |                                     |
|-----------------------------|-------------------------------------|
| Bits/pixel (1 campione/pixel) | Dimensioni riquadro (pixel, w x h x d) |
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

![mapping predefinito del MIP più dettagliato](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Trama-mapping predefinito della risorsa affiancata 3D (seconda MIP più dettagliata)

![mapping predefinito del secondo MIP più dettagliato](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Trama-risorsa affiancata 3D (MIP più dettagliato)

Il codice seguente configura una risorsa affiancata 3D al MIP più dettagliato.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Trama-risorsa affiancata 3D (seconda MIP più dettagliata)

Il codice seguente configura una risorsa affiancata 3D e il secondo MIP più dettagliato:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Trama-risorsa affiancata 3D (riquadro singolo)

Il codice seguente consente di configurare una singola risorsa di sezione:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Trama-risorsa affiancata 3D (casella uniforme)

Il codice seguente consente di configurare una risorsa affiancata di box (nota l'istruzione). `trSize.bUseBox = true;) :`

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

## <a name="d3d113-tiled-resource-apis"></a>API delle risorse affiancate di D3D 11.3

Le stesse chiamate API vengono usate per le risorse affiancate 2D e 3D:

Enumerazioni

-   [**D3d11 \_ Livello \_ risorse \_ affiancate**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determina il livello di supporto delle risorse affiancate.
-   [**D3d11 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : usato per verificare il supporto delle risorse affiancate.
-   [**D3d11 \_ Verifica \_ \_ \_ \_ flag livelli di qualità multicampione**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determina il supporto delle risorse affiancate in una risorsa di campionamento multiplo.
-   [**D3d11 \_ \_ \_ Flag di copia dei riquadri**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : include i flag per la copia da e verso le risorse swizzled affiancate e i buffer lineari.

Strutture

-   [**D3d11 \_ \_ \_ Coordinata della risorsa affiancata**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : include le coordinate x, y e z e il riferimento alla sottorisorsa. Si noti che è presente una classe helper: \_ \_ coordinata di risorsa CD3D11 affiancata \_ .
-   [**D3d11 \_ \_ \_ Dimensioni area affiancata**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifica le dimensioni e il numero di riquadri dell'area affiancata.
-   [**D3d11 \_ \_Forma sezione**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : la forma sezione come larghezza, altezza e profondità nei Texel.
-   [**D3d11 \_ FEATURE \_ data \_ d3d11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): include il livello di livello risorse del riquadro supportato.

Metodi

-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : usato per determinare quali funzionalità e a quale livello sono supportate dall'hardware corrente.
-   [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copia i riquadri dal buffer alla risorsa affiancata o viceversa.
-   [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : Aggiorna i mapping dei percorsi dei riquadri nelle risorse affiancate alle posizioni di memoria in un pool di sezioni.
-   [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copia i mapping da una risorsa di origine affiancata a una risorsa affiancata di destinazione.
-   [**ID3D11DeviceContext2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : ottiene informazioni sul modo in cui una risorsa affiancata viene suddivisa in riquadri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




