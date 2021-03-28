---
title: Metodi ID3D11Device di 10Level9
description: Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D \_ \_ \_ 11 \_ 0 e un livello di funzionalità superiore per i metodi ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399466"
---
# <a name="10level9-id3d11device-methods"></a>Metodi ID3D11Device di 10Level9

Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D \_ \_ \_ 11 \_ 0 e un livello di funzionalità superiore per i metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .

-   [ID3D11Device:: CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device:: CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device:: CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device:: CreateBlendState](#id3d11devicecreateblendstate)
-   [ID3D11Device:: CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device:: CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device:: CreateCounter](#id3d11devicecreatecounter)
-   [ID3D11Device:: CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device:: CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device:: CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device:: CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device:: CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device:: CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device:: CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device:: CreatePredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device:: CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device:: CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device:: CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device:: CreateSamplerState](#id3d11devicecreatesamplerstate)
-   [ID3D11Device:: CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device:: CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device:: CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device:: CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device:: CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device:: CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device:: OpenSharedResource](#id3d11deviceopensharedresource)
-   [Argomenti correlati](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device:: CheckCounter



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">I contatori dipendenti dal dispositivo sono facoltativamente supportati. Usare <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: CheckCounterInfo</strong></a> per determinare il supporto. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device:: CheckFormatSupport



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Vedere supporto del formato in base al <a href="overviews-direct3d-11-devices-downlevel-intro.md">livello di funzionalità</a>$ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device:: CheckMultisampleQualityLevels



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">I livelli di funzionalità non offrono alcuna garanzia sul supporto MSAA. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device:: CreateBlendState



| Livello funzionalità              | Differenze di comportamento                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1  | AlphaToCoverageEnable deve essere **false**.<br/> I primi quattro BlendEnables devono avere lo stesso valore.<br/> D3D11 \_ di \_ Blend \_ ALPHASAT src non supportato.<br/> La combinazione di colori dual source non è supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)<br/>                                                                                |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2  | AlphaToCoverageEnable deve essere **false**.<br/> I primi quattro BlendEnables devono avere lo stesso valore.<br/> I primi quattro RenderTargetWriteMasks devono avere lo stesso valore.<br/> D3D11 \_ di \_ Blend \_ ALPHASAT src non supportato.<br/> La combinazione di colori dual source non è supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)<br/> |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3  | AlphaToCoverageEnable deve essere **false**.<br/> I primi quattro BlendEnables devono avere lo stesso valore.<br/> D3D11 \_ di \_ Blend \_ ALPHASAT src non supportato.<br/> La combinazione di colori dual source non è supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)<br/>                                                                                |
| \_Livello di funzionalità D3D \_ \_ 10 \_ 0 | Aggiunge l'alfa al code coverage                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device:: CreateBlendState1



| Livello funzionalità              | Differenze di comportamento                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1  | Non supportato<br/>                                                                                                                                                                                                                                                                                                                                       |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2  | Non supportato<br/>                                                                                                                                                                                                                                                                                                                                       |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3  | Non supportato<br/>                                                                                                                                                                                                                                                                                                                                       |
| \_Livello di funzionalità D3D \_ \_ 10 \_ 0 | Il membro *OutputMergerLogicOp* è stato aggiunto alle [**\_ \_ \_ \_ Opzioni d3d11 dei dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)per determinare il supporto per le operazioni logiche (operazioni logiche bit per bit tra pixel shader output e il contenuto della destinazione di rendering, fare riferimento a [**d3d11 \_ Render \_ target \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)). |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device:: CreateBuffer



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>I buffer non possono avere visualizzazioni di destinazione di rendering.<br/> I buffer devono avere esattamente uno dei D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.<br/> Consente solo buffer di indice con il formato DXGI_FORMAT_R16_UINT. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> I buffer non possono avere visualizzazioni di destinazione di rendering.<br/> I buffer devono avere esattamente uno dei D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.<br/> Consente i buffer di indice con i formati DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT come D3D_FEATURE_LEVEL_10_0 e versioni successive. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device:: CreateCounter



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device:: CreateDepthStencilView



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supporta lo stencil a due lati. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device:: CreateDomainShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device:: CreateGeometryShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device:: CreateGeometryShaderWithStreamOutput



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device:: CreateHullShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device:: CreateInputLayout



| Livello funzionalità             | Differenze di comportamento                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | Non supporta \_ i dati di input d3d11 \_ per \_ istanza \_                                                                |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | Non supporta \_ i dati di input d3d11 \_ per \_ istanza \_                                                                |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | Il flusso di vertici zero deve avere \_ input d3d11 \_ per \_ \_ i dati del vertice, se i flussi hanno input di d3d11 \_ \_ per \_ dati del vertice \_ |



 

Per informazioni dettagliate sui formati che possono essere usati per i dati dei vertici a ogni livello di funzionalità, vedere il formato supporto per [grafico a livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) .

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device:: CreatePixelShader



| Livello funzionalità             | Differenze di comportamento                                    |
|---------------------------|---------------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | Usare PS \_ 4 \_ 0 \_ level \_ 9 \_ 1                          |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | Usare PS \_ 4 \_ 0 \_ level \_ 9 \_ 1                          |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | È necessario usare PS \_ 4 \_ 0 \_ level \_ 9 \_ 3 o PS \_ 4 \_ 0 \_ level \_ 9 \_ 1 |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device:: CreatePredicate



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a>ID3D11Device:: CreateQuery



| Livello funzionalità             | Differenze di comportamento                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | Sono supportate le query di eventi. Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto.               |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | Sono supportate le query di eventi e occlusioni. Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto. |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | Sono supportate le query di eventi e occlusioni. Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device:: CreateRasterizerState



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">DepthClipEnable deve essere <strong>true</strong>. DepthBiasClamp deve essere impostato su 0. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device:: CreateRenderTargetView



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Può supportare solo visualizzazioni di destinazione di rendering di oggetti Texture2D. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device:: CreateSamplerState



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Il filtro di confronto non è supportato.<br/> Il colore del bordo deve essere compreso tra [0,1]<br/> Min LOD non può essere frazionario<br/> Il numero massimo di LOD deve essere FLT_MAX<br/> Il numero massimo di anisotropia è 2.<br/> D3D11_TEXTURE_ADDRESS_MIRRORONCE non supportato.<br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Il filtro di confronto non è supportato.<br/> Il colore del bordo deve essere compreso tra [0,1]<br/> Min LOD non può essere frazionario<br/> Il numero massimo di LOD deve essere FLT_MAX<br/> Il numero massimo di anisotropia è 16.<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device:: CreateShaderResourceView



| Livello funzionalità             | MostDetailedMip Plus MipLevels deve includere il valore LOD minimo (subresource più piccolo) | La vista deve includere tutti gli elementi della matrice di risorse |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | Sì                                                                          | sì                                           |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | Sì                                                                          | Sì                                           |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | Sì                                                                          | Sì                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device:: CreateTexture1D



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device:: CreateTexture2D

Le risorse di Texture2D presentano limiti per la larghezza e l'altezza che variano in base ai [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md). Nei livelli di funzionalità 9 \_ 3, di seguito sono riportate le garanzie minime e le singole implementazioni possono superare i requisiti.



| Livello funzionalità             | Se MipCount > 1, le dimensioni devono essere una potenza integrale di due | Dimensione di trama minima supportata | Le dimensioni delle trame del cubo devono essere una potenza di due | Se \_ è impostata la TEXTURECUBE misc, ArraySize è: | Se varie \_ TEXTURECUBE non è impostata, ArraySize è. |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | Sì                                                          | 2048                                | Sì                                           | 6                                              | 1                                                  |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | Sì                                                          | 2048                                | Sì                                           | 6                                              | 1                                                  |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | Sì                                                          | 4096                                | Sì                                           | 6                                              | 1                                                  |



 

Nella tabella precedente il nome completo di **varie \_ TEXTURECUBE** è [**d3d11 \_ Resource \_ varie \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).

Per tutti i 9 livelli di funzionalità sono soddisfatte le condizioni seguenti \_ \* [](overviews-direct3d-11-devices-downlevel-intro.md):

-   Quando si usa \_ il \_ valore predefinito di utilizzo D3D11 o l' \_ utilizzo \_ di d3d11 non è modificabile, BindFlags non può essere zero
-   Quando si usa \_ lo \_ \_ stencil di profondità di binding d3d11, MipLevels deve essere 1.
-   Quando si usa \_ la \_ risorsa shader bind d3d11 \_ , SampleDesc. Count deve essere 1.
-   Quando si usa il \_ Binding d3d11 \_ presente, la risorsa non può avere una \_ \_ risorsa shader bind d3d11 \_ .
-   Quando si usa \_ la \_ risorsa D3D10 DDI \_ \_ Shared, il formato non può essere DXGI \_ Format \_ R8G8B8A8 \_ UNORM o DXGI \_ Format R8G8B8A8 \_ \_ UNORM \_ sRGB.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device:: CreateTexture3D



| Livello funzionalità             | Dimensione massima (qualsiasi asse) | Le dimensioni devono essere una potenza di due |
|---------------------------|------------------------------|---------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | 256                          | Sì                             |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | 512                          | Sì                             |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | 512                          | Sì                             |



 

Se la risorsa è \_ un \_ valore predefinito di utilizzo D3D11 o l' \_ utilizzo \_ di d3d11 non è modificabile, BindFlags non può essere zero.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device:: CreateUnorderedAccessView



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device:: CreateVertexShader



| Livello funzionalità             | Differenze di comportamento                                    |
|---------------------------|---------------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | È necessario usare vs \_ 4 \_ 0 \_ livello \_ 9 \_ 1                          |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | È necessario usare vs \_ 4 \_ 0 \_ livello \_ 9 \_ 1                          |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | È necessario usare vs \_ 4 \_ 0 \_ livello \_ 9 \_ 3 o vs \_ 4 \_ 0 \_ livello \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device:: OpenSharedResource



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Usare <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a> con il valore <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> e la struttura <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> per determinare se un formato può essere condiviso. Se il formato può essere condiviso, <strong>CheckFeatureSupport</strong> restituisce il flag <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .<br/>
<blockquote>
[!Note]<br />
[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> non sono mai condivisibili quando si usa il livello di funzionalità 9, anche se il dispositivo indica il supporto della funzionalità facoltativo per <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>. Il tentativo di creare risorse condivise con formati DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> avrà sempre esito negativo a meno che il livello di funzionalità non sia 10_0 o superiore.
</blockquote>
<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

