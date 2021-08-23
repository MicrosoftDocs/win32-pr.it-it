---
title: Strutture di risorse (grafica Direct3D 11)
description: Le strutture vengono usate per creare e usare le risorse.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- strutture, risorsa Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acff7e10538910082dcd15220cb41a2ec360c24472837a569530f0b306313db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125125"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Strutture di risorse (grafica Direct3D 11)

Le strutture vengono usate per creare e usare le risorse.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                         | Descrizione                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Descrive una risorsa buffer.<br/>                                                                           |
| [**D3D11 \_ BUFFER \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Specifica gli elementi in una risorsa buffer da usare in una visualizzazione di destinazione di rendering.<br/>                            |
| [**D3D11 \_ BUFFER \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Specifica gli elementi in una risorsa buffer da usare in una visualizzazione shader-risorsa.<br/>                          |
| [**D3D11 \_ BUFFER \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Descrive gli elementi in un buffer da utilizzare in una visualizzazione di accesso non ordinato.<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Descrive gli elementi in una risorsa buffer non elaborato da usare in una visualizzazione shader-risorsa.<br/>                      |
| [**D3D11 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Specifica le sottorisorse di una trama accessibili da una visualizzazione depth-stencil.<br/>                 |
| [**SOTTORISORSA MAPPATA D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Fornisce l'accesso ai dati della sottorisorsa.<br/>                                                                   |
| [**D3D11 \_ PACKED \_ MIP \_ DESC**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Descrive la struttura del riquadro di una risorsa affiancata con mipmap. <br/>                                        |
| [**D3D11 \_ RENDER \_ TARGET \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Specifica le sottorisorse da una risorsa accessibile tramite una visualizzazione di destinazione di rendering.<br/>             |
| [**D3D11 \_ RENDER \_ TARGET \_ VIEW \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Descrive le sottorisorse di una risorsa accessibili tramite una visualizzazione di destinazione di rendering.<br/>             |
| [**D3D11 \_ SHADER \_ RESOURCE \_ VIEW \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Descrive una visualizzazione shader-risorsa.<br/>                                                                      |
| [**VISUALIZZAZIONE DELLE RISORSE DELLO SHADER D3D11 \_ \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Descrive una visualizzazione shader-risorsa.<br/>                                                                      |
| [**DATI DELLA SOTTORISORSA D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Specifica i dati per l'inizializzazione di una sottorisorsa.<br/>                                                         |
| [**AFFIANCAMENTO DELLE \_ SOTTORISORSE D3D11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Descrive un volume di sottorisorse affiancate.<br/>                                                                  |
| [**D3D11 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Specifica le sottorisorse da una matrice di trame 1D da usare in una visualizzazione depth-stencil.<br/>                |
| [**D3D11 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Specifica le sottorisorse da una matrice di trame 1D da usare in una visualizzazione di destinazione di rendering.<br/>                |
| [**D3D11 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Specifica le sottorisorse da una matrice di trame 1D da usare in una visualizzazione shader-risorsa.<br/>              |
| [**UAV MATRICE D3D11 \_ TEX1D \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Descrive una matrice di risorse di trama 1D ad accesso non ordinato.<br/>                                           |
| [**D3D11 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Specifica la sottorisorsa da una trama 1D accessibile a una visualizzazione depth-stencil.<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Specifica la sottorisorsa da una trama 1D da usare in una visualizzazione di destinazione di rendering.<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Specifica la sottorisorsa da una trama 1D da usare in una visualizzazione shader-risorsa.<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Descrive una risorsa trama 1D ad accesso non ordinato.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Specifica le sottorisorse da una matrice di trame 2D accessibili a una visualizzazione depth-stencil.<br/>      |
| [**D3D11 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Specifica le sottorisorse da una matrice di trame 2D da usare in una visualizzazione di destinazione di rendering.<br/>                |
| [**MATRICE D3D11 \_ TEX2D \_ \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Descrive le sottorisorse da una matrice di trame 2D da usare in una visualizzazione di destinazione di rendering.<br/>                |
| [**D3D11 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Specifica le sottorisorse da una matrice di trame 2D da usare in una visualizzazione shader-risorsa.<br/>              |
| [**D3D11 \_ TEX2D \_ ARRAY \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Descrive le sottorisorse di una matrice di trame 2D da usare in una visualizzazione shader-risorsa.<br/>              |
| [**UAV MATRICE D3D11 \_ TEX2D \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Descrive una matrice di risorse di trama 2D ad accesso non ordinato.<br/>                                           |
| [**D3D11 \_ TEX2D \_ ARRAY \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Descrive una matrice di risorse di trama 2D ad accesso non ordinato.<br/>                                           |
| [**D3D11 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Specifica la sottorisorsa da una trama 2D accessibile a una visualizzazione stencil di profondità.<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Specifica la sottorisorsa da una trama 2D da usare in una visualizzazione di destinazione di rendering.<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Descrive la sottorisorsa da una trama 2D da usare in una visualizzazione di destinazione di rendering.<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Specifica la sottorisorsa da una trama 2D da usare in una visualizzazione shader-risorsa.<br/>                          |
| [**D3D11 \_ TEX2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Descrive la sottorisorsa da una trama 2D da usare in una visualizzazione shader-risorsa.<br/>                          |
| [**D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Descrive una risorsa trama 2D ad accesso non ordinato.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Descrive una risorsa trama 2D ad accesso non ordinato.<br/>                                                      |
| [**D3D11 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Specifica le sottorisorse da una matrice di trame 2D multicampionato per una visualizzazione depth-stencil.<br/>         |
| [**MATRICE D3D11 \_ TEX2DMS \_ \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Specifica le sottorisorse da una matrice di trame 2D multicampionato da usare in una visualizzazione di destinazione di rendering.<br/> |
| [**D3D11 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Specifica le sottorisorse da una matrice di trame 2D multicampionato da usare in una visualizzazione shader-risorsa.<br/> |
| [**D3D11 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Specifica la sottorisorsa da una trama 2D multicampionata accessibile a una visualizzazione depth-stencil.<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Specifica la sottorisorsa da una trama 2D multicampionata da usare in una visualizzazione di destinazione di rendering.<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Specifica le sottorisorse da una trama 2D multicampionata da usare in una visualizzazione shader-risorsa.<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Specifica le sottorisorse da una trama 3D da usare in una visualizzazione di destinazione di rendering.<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Specifica le sottorisorse da una trama 3D da usare in una visualizzazione shader-risorsa.<br/>                         |
| [**D3D11 \_ TEX3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Descrive una risorsa trama 3D ad accesso non ordinato.<br/>                                                      |
| [**D3D11 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Specifica le sottorisorse da una matrice di trame del cubo da usare in una visualizzazione shader-risorsa.<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Specifica la sottorisorsa da una trama del cubo da usare in una visualizzazione shader-risorsa.<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Descrive una trama 1D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Descrive una trama 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Descrive una trama 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Descrive una trama 3D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Descrive una trama 3D.<br/>                                                                                |
| [**DIMENSIONI DELL'AREA DEL RIQUADRO D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Descrive le dimensioni di un'area affiancata.<br/>                                                                  |
| [**COORDINATA DI RISORSA \_ AFFIANCATA D3D11 \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Descrive le coordinate di una risorsa affiancata.<br/>                                                         |
| [**FORMA RIQUADRO D3D11 \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Descrive la forma di un riquadro specificandone le dimensioni.<br/>                                            |
| [**VISTA DI ACCESSO NON ORDINATO D3D11 \_ \_ \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Specifica le sottorisorse da una risorsa accessibile tramite una visualizzazione di accesso non ordinato.<br/>         |
| [**VISTA DI ACCESSO NON ORDINATO D3D11 \_ \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Descrive le sottorisorse di una risorsa accessibile tramite una visualizzazione di accesso non ordinato.<br/>         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla risorsa](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





