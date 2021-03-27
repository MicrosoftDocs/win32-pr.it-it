---
title: Strutture di risorse (grafica Direct3D 11)
description: Le strutture vengono usate per creare e usare le risorse.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- strutture, risorsa Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5020792e1fb56a52e7a4354964c45bb5d65bbba4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873237"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Strutture di risorse (grafica Direct3D 11)

Le strutture vengono usate per creare e usare le risorse.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                         | Descrizione                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Descrive una risorsa del buffer.<br/>                                                                           |
| [**D3D11 \_ buffer \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Specifica gli elementi in una risorsa buffer da usare in una visualizzazione di destinazione di rendering.<br/>                            |
| [**\_SRV buffer \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Specifica gli elementi in una risorsa di buffer da usare in una visualizzazione risorse dello shader.<br/>                          |
| [**\_UAV buffer \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Descrive gli elementi di un buffer da utilizzare in una visualizzazione di accesso non ordinato.<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Descrive gli elementi in una risorsa di buffer non elaborato da usare in una visualizzazione risorse dello shader.<br/>                      |
| [**\_ \_ Visualizzazione stencil profondità \_ d3d11 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Specifica le sottorisorse di una trama a cui è possibile accedere da una visualizzazione di stencil profondità.<br/>                 |
| [**\_Sottorisorsa mappata d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Consente di accedere ai dati della sottorisorsa.<br/>                                                                   |
| [**D3D11 \_ ( \_ MIP) compresso \_ DESC**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Descrive la struttura dei riquadri di una risorsa affiancata con mipmap. <br/>                                        |
| [**\_Visualizzazione della destinazione di rendering d3d11 \_ \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Specifica le sottorisorse di una risorsa accessibili tramite una visualizzazione di destinazione del rendering.<br/>             |
| [**\_ \_ Visualizzazione destinazione rendering \_ d3d11 \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Descrive le sottorisorse di una risorsa accessibile tramite una visualizzazione di destinazione del rendering.<br/>             |
| [**\_ \_ Descrizione della visualizzazione risorse \_ shader \_ d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Descrive una visualizzazione delle risorse dello shader.<br/>                                                                      |
| [**\_ \_ Visualizzazione risorse shader d3d11 \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Descrive una visualizzazione delle risorse dello shader.<br/>                                                                      |
| [**\_Dati della SOTTORISORSA d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Specifica i dati per l'inizializzazione di una sottorisorsa.<br/>                                                         |
| [**\_Affiancamento di SOTTORISORSE d3d11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Descrive un volume di sottorisorse affiancato.<br/>                                                                  |
| [**Vista \_ \_ origine dati matrice TEX1D d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Specifica le sottorisorse da una matrice di trame 1D da usare in una visualizzazione di stencil di profondità.<br/>                |
| [**D3D11 \_ TEX1D \_ array \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Specifica le sottorisorse da una matrice di trame 1D da usare in una visualizzazione di destinazione di rendering.<br/>                |
| [**D3D11 \_ TEX1D \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Specifica le sottorisorse da una matrice di trame 1D da usare in una visualizzazione delle risorse dello shader.<br/>              |
| [**D3D11 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Descrive una matrice di risorse di trama 1D con accesso non ordinato.<br/>                                           |
| [**Vista \_ origine dati TEX1D d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Specifica la sottorisorsa da una trama 1D accessibile a una visualizzazione di stencil di profondità.<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Specifica la sottorisorsa da una trama 1D da usare in una visualizzazione di destinazione di rendering.<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Specifica la sottorisorsa da una trama 1D da usare in una visualizzazione risorse dello shader.<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Descrive una risorsa di trama 1D con accesso non ordinato.<br/>                                                      |
| [**Vista \_ \_ origine dati matrice TEX2D d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Specifica le sottorisorse di una matrice di trame 2D accessibili a una visualizzazione di stencil di profondità.<br/>      |
| [**D3D11 \_ TEX2D \_ array \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Specifica le sottorisorse da una matrice di trame 2D da usare in una visualizzazione di destinazione del rendering.<br/>                |
| [**D3D11 \_ \_ Array TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Descrive le sottorisorse di una matrice di trame 2D da usare in una visualizzazione di destinazione del rendering.<br/>                |
| [**D3D11 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Specifica le sottorisorse da una matrice di trame 2D da usare in una visualizzazione risorse shader.<br/>              |
| [**D3D11 \_ \_ Array TEX2D \_ srv1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Descrive le sottorisorse di una matrice di trame 2D da usare in una visualizzazione risorse shader.<br/>              |
| [**D3D11 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Descrive una matrice di risorse di trama 2D con accesso non ordinato.<br/>                                           |
| [**D3D11 \_ \_ Array TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Descrive una matrice di risorse di trama 2D con accesso non ordinato.<br/>                                           |
| [**Vista \_ origine dati TEX2D d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Specifica la sottorisorsa da una trama 2D accessibile a una visualizzazione di stencil di profondità.<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Specifica la sottorisorsa da una trama 2D da usare in una visualizzazione di destinazione del rendering.<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Descrive la sottorisorsa da una trama 2D da usare in una visualizzazione di destinazione di rendering.<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Specifica la sottorisorsa da una trama 2D da usare in una visualizzazione risorse dello shader.<br/>                          |
| [**D3D11 \_ TEX2D \_ srv1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Descrive la sottorisorsa da una trama 2D da usare in una visualizzazione risorse shader.<br/>                          |
| [**D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Descrive una risorsa di trama 2D con accesso non ordinato.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Descrive una risorsa di trama 2D con accesso non ordinato.<br/>                                                      |
| [**Vista \_ \_ origine dati matrice TEX2DMS d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Specifica le sottorisorse da una matrice di trame 2D multicampionate per una visualizzazione dello stencil di profondità.<br/>         |
| [**D3D11 \_ TEX2DMS \_ array \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Specifica le sottorisorse da una matrice di trame 2D multicampionate da usare in una visualizzazione di destinazione del rendering.<br/> |
| [**D3D11 \_ TEX2DMS \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Specifica le sottorisorse da una matrice di trame 2D multicampionate da usare in una visualizzazione delle risorse dello shader.<br/> |
| [**Vista \_ origine dati TEX2DMS d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Specifica la sottorisorsa da una trama 2D multicampionata accessibile a una visualizzazione di stencil di profondità.<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Specifica la sottorisorsa da una trama 2D multicampionata da usare in una visualizzazione di destinazione di rendering.<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Specifica le sottorisorse da una trama 2D multicampionata da usare in una visualizzazione risorse shader.<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Specifica le sottorisorse da una trama 3D da usare in una visualizzazione di destinazione del rendering.<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Specifica le sottorisorse da una trama 3D da usare in una visualizzazione risorse dello shader.<br/>                         |
| [**D3D11 \_ TEX3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Descrive una risorsa di trama 3D con accesso non ordinato.<br/>                                                      |
| [**D3D11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Specifica le sottorisorse da una matrice di trame del cubo da usare in una visualizzazione delle risorse dello shader.<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Specifica la sottorisorsa da una trama del cubo da usare in una visualizzazione risorse dello shader.<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Descrive una trama 1D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Descrive una trama 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Descrive una trama 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Descrive una trama 3D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Descrive una trama 3D.<br/>                                                                                |
| [**\_ \_ Dimensioni area del riquadro d3d11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Descrive le dimensioni di un'area affiancata.<br/>                                                                  |
| [**\_Coordinata risorse d3d11 affiancata \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Descrive le coordinate di una risorsa affiancata.<br/>                                                         |
| [**\_Forma riquadro \_ d3d11**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Descrive la forma di un riquadro specificandone le dimensioni.<br/>                                            |
| [**D3D11 \_ vista di accesso non ordinato \_ \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Specifica le sottorisorse di una risorsa accessibili tramite una visualizzazione di accesso non ordinato.<br/>         |
| [**D3D11 \_ vista di accesso non ordinato \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Descrive le sottorisorse di una risorsa accessibile tramite una visualizzazione di accesso non ordinato.<br/>         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento alla risorsa](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





