---
description: Strutture utilizzate per creare e utilizzare le risorse.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Strutture di risorse (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da964bf19c1ce5e1e5c4dfd0685df79b28ac5e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304715"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Strutture di risorse (grafica Direct3D 10)

Strutture utilizzate per creare e utilizzare [le risorse](d3d10-graphics-programming-guide-resources-types.md).



| Strutture                                                                 | Descrizione                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ buffer \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Descrizione di una risorsa del [buffer](d3d10-graphics-programming-guide-resources-types.md) .                                                                     |
| [**D3D10 \_ buffer \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Descrive gli elementi di un [buffer](d3d10-graphics-programming-guide-resources-types.md) da utilizzare in una visualizzazione di destinazione del rendering.                                |
| [**\_SRV buffer \_ D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Descrive gli elementi in una risorsa di [buffer](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione risorse dello shader.                         |
| [**\_ \_ Visualizzazione stencil profondità \_ D3D10 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Descrive una visualizzazione di stencil di profondità.                                                                                                                               |
| [**\_TEXTURE2D mappato D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Fornisce l'accesso ai dati delle sottorisorse in una [trama 2D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**\_TEXTURE3D mappato D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Consente di accedere ai dati delle sottorisorse in una [trama 3D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**\_Visualizzazione della destinazione di rendering D3D10 \_ \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Descrive una visualizzazione di destinazione del rendering.                                                                                                                               |
| [**\_Dati della SOTTORISORSA D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Specifica i dati per l'inizializzazione di una risorsa.                                                                                                                   |
| [**Vista \_ \_ origine dati matrice TEX1D D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Specifica il livello di mipmap e le trame in una [matrice di trama 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di stencil di profondità.       |
| [**D3D10 \_ TEX1D \_ array \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Specifica le sottorisorse da una matrice di [trame 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione di rendering.             |
| [**D3D10 \_ TEX1D \_ array \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Specifica i livelli e le trame di mipmap in una [matrice di trama 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione delle risorse dello shader.      |
| [**Vista \_ origine dati TEX1D D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Specifica le sottorisorse da una [trama 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di stencil di profondità.                        |
| [**D3D10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Specifica le sottorisorse da una [trama 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione del rendering.                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Specifica le sottorisorse da una [trama 1D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione risorse shader.                      |
| [**Vista \_ \_ origine dati matrice TEX2D D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Specifica il livello di mipmap e le trame in una [matrice di trama 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di stencil di profondità. |
| [**D3D10 \_ TEX2D \_ array \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Specifica il livello di mipmap e le trame in una [matrice di trama 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione del rendering. |
| [**D3D10 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Specifica le sottorisorse da una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione delle risorse dello shader.           |
| [**Vista \_ origine dati TEX2D D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Specifica le sottorisorse da una [trama 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di stencil di profondità.                        |
| [**D3D10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Specifica le sottorisorse da una [trama 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione del rendering.                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Specifica le sottorisorse da una [trama 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione risorse shader.                      |
| [**Vista \_ \_ origine dati matrice TEX2DMS D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Specifica le sottorisorse da una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di stencil di profondità.             |
| [**D3D10 \_ TEX2DMS \_ array \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Specifica le sottorisorse da una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione del rendering.             |
| [**D3D10 \_ TEX2DMS \_ array \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Specifica le sottorisorse da una matrice di [trame 2D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione delle risorse dello shader.           |
| [**Vista \_ origine dati TEX2DMS D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Specifica le sottorisorse da una [trama 2D](d3d10-graphics-programming-guide-resources-types.md) multicampionata da usare in una visualizzazione di stencil di profondità.           |
| [**D3D10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Specifica le sottorisorse da una [trama 2D](d3d10-graphics-programming-guide-resources-types.md) multicampionata da usare in una visualizzazione di destinazione del rendering.           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Specifica le sottorisorse da una [trama 2D](d3d10-graphics-programming-guide-resources-types.md) multicampionata da usare in una visualizzazione delle risorse dello shader.         |
| [**D3D10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Specifica le sottorisorse da una [trama 3D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione di destinazione del rendering.                        |
| [**D3D10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Specifica le sottorisorse da una [trama 3D](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione risorse dello shader.                      |
| [**D3D10 \_ \_ Array TEXCUBE \_ srv1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Specifica le sottorisorse da una [trama del cubo](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione risorse dello shader.                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Specifica le sottorisorse da una [trama del cubo](d3d10-graphics-programming-guide-resources-types.md) da usare in una visualizzazione risorse dello shader.                    |
| [**D3D10 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Descrive una risorsa di [trama 1D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Descrive una risorsa di [trama 2D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Descrive una risorsa di [trama 3D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento alla risorsa](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



