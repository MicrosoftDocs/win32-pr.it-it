---
description: Strutture utilizzate per creare e usare le risorse.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Strutture di risorse (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb45ff5d77d7bb0417b54b88a4014e2a96f522d2e026c778efcd05d23f624bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635021"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Strutture di risorse (grafica Direct3D 10)

Strutture utilizzate per creare e usare [le risorse](d3d10-graphics-programming-guide-resources-types.md).



| Strutture                                                                 | Descrizione                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Descrizione di una [risorsa buffer.](d3d10-graphics-programming-guide-resources-types.md)                                                                     |
| [**D3D10 \_ BUFFER \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Descrive gli elementi in un [buffer](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione di rendering.                                |
| [**D3D10 \_ BUFFER \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Descrive gli elementi in una risorsa [buffer](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.                         |
| [**D3D10 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Descrive una visualizzazione depth-stencil.                                                                                                                               |
| [**TRAMA MAPPATA \_ D3D102D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Fornisce l'accesso ai dati della sottorisorsa in una [trama 2D.](d3d10-graphics-programming-guide-resources-types.md)                                                  |
| [**TRAMA MAPPATA \_ D3D103D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Fornisce l'accesso ai dati della sottorisorsa in una [trama 3D.](d3d10-graphics-programming-guide-resources-types.md)                                                  |
| [**D3D10 \_ RENDER \_ TARGET \_ VIEW \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Descrive una visualizzazione di destinazione di rendering.                                                                                                                               |
| [**DATI DELLE SOTTORISORSE D3D10 \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Specifica i dati per l'inizializzazione di una risorsa.                                                                                                                   |
| [**D3D10 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Specifica il livello mipmap e le trame in una matrice [di trame 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione depth-stencil.       |
| [**D3D10 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Specifica le sottorisorse da una matrice di [trame 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione di rendering.             |
| [**D3D10 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Specifica i livelli e le trame mipmap in una matrice [di trame 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.      |
| [**D3D10 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Specifica le sottorisorse da una [trama 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione depth-stencil.                        |
| [**D3D10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Specifica le sottorisorse da una trama [1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione di rendering.                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Specifica le sottorisorse da una [trama 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.                      |
| [**D3D10 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Specifica il livello mipmap e le trame in una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione depth-stencil. |
| [**D3D10 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Specifica il livello mipmap e le trame in una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione di rendering. |
| [**D3D10 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Specifica le sottorisorse da una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.           |
| [**D3D10 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Specifica le sottorisorse da una [trama 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione depth-stencil.                        |
| [**D3D10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Specifica le sottorisorse da una trama [2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione di rendering.                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Specifica le sottorisorse da una [trama 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.                      |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Specifica le sottorisorse da una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione depth-stencil.             |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Specifica le sottorisorse da una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione di rendering.             |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Specifica le sottorisorse da una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.           |
| [**D3D10 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Specifica le sottorisorse da una trama [2D](d3d10-graphics-programming-guide-resources-types.md) multicampionata da usare in una visualizzazione depth-stencil.           |
| [**D3D10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Specifica le sottorisorse da una trama [2D](d3d10-graphics-programming-guide-resources-types.md) multicampionata da usare in una visualizzazione di destinazione di rendering.           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Specifica le sottorisorse da una trama [2D](d3d10-graphics-programming-guide-resources-types.md) multicampionata da usare in una visualizzazione di risorse shader.         |
| [**D3D10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Specifica le sottorisorse da una trama [3D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione di rendering.                        |
| [**D3D10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Specifica le sottorisorse da una [trama 3D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.                      |
| [**D3D10 \_ TEXCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Specifica le sottorisorse da una trama [del cubo](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Specifica le sottorisorse da una trama [del cubo](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione shader-risorsa.                    |
| [**D3D10 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Descrive una risorsa [trama 1D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |
| [**D3D10 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Descrive una risorsa [trama 2D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |
| [**D3D10 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Descrive una risorsa [trama 3D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla risorsa](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



