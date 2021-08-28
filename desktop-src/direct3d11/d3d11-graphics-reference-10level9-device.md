---
title: 10Level9 ID3D11Dispositori del dispositivo
description: Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D FEATURE LEVEL 11 0 e superiore per i \_ \_ metodi \_ \_ ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467e47d7ba623f1c28111cf3bf7cc6a07da8317
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475787"
---
# <a name="10level9-id3d11device-methods"></a>10Level9 ID3D11Dispositori del dispositivo

Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D FEATURE LEVEL 11 0 e superiore per i \_ \_ metodi \_ \_ [**ID3D11Device.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)

-   [ID3D11Device::CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device::CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device::CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device::CreateBlendState](#id3d11devicecreateblendstate)
-   [ID3D11Device::CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device::CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device::CreateCounter](#id3d11devicecreatecounter)
-   [ID3D11Device::CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device::CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device::CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device::CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device::CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device::CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device::CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device::CreatePredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device::CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device::CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device::CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device::CreateSamplerState](#id3d11devicecreatesamplerstate)
-   [ID3D11Device::CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device::CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device::CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device::CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device::CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device::CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device::OpenSharedResource](#id3d11deviceopensharedresource)
-   [Argomenti correlati](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device::CheckCounter




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | I contatori dipendenti dal dispositivo sono supportati facoltativamente. Usare <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> per determinare il supporto.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device::CheckFormatSupport




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Vedere il supporto del formato <a href="overviews-direct3d-11-devices-downlevel-intro.md">per livello di</a>funzionalità ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device::CheckMultisampleQualityLevels




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | I livelli di funzionalità non garantiscono il supporto MSAA.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device::CreateBlendState



| Livello di funzionalità              | Differenze di comportamento                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1  | AlphaToCoverageEnable deve essere **FALSE.**<br/> Le prime quattro blendEnable devono avere tutte lo stesso valore.<br/> D3D11 \_ BLEND \_ SRC \_ ALPHASAT non supportato.<br/> Combinazione di colori dual source non supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)<br/>                                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2  | AlphaToCoverageEnable deve essere **FALSE.**<br/> Le prime quattro blendEnable devono avere tutte lo stesso valore.<br/> I primi quattro RenderTargetWriteMasks devono avere tutti lo stesso valore.<br/> D3D11 \_ BLEND \_ SRC \_ ALPHASAT non supportato.<br/> Combinazione di colori dual source non supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3  | AlphaToCoverageEnable deve essere **FALSE.**<br/> Le prime quattro blendEnable devono avere tutte lo stesso valore.<br/> D3D11 \_ BLEND \_ SRC \_ ALPHASAT non supportato.<br/> Combinazione di colori dual source non supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)<br/>                                                                                |
| LIVELLO DI FUNZIONALITÀ D3D \_ \_ \_ 10 \_ 0 | Aggiunge alfa-to-coverage                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device::CreateBlendState1



| Livello di funzionalità              | Differenze di comportamento                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1  | Non supportato<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2  | Non supportato<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3  | Non supportato<br/>                                                                                                                                                                                                                                                                                                                                       |
| LIVELLO DI FUNZIONALITÀ D3D \_ \_ \_ 10 \_ 0 | Il membro *OutputMergerLogicOp* è stato aggiunto a [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)per determinare il supporto per le operazioni logiche (le operazioni logiche bit per bit tra l'output di pixel shader e il contenuto della destinazione di rendering, vedere [**D3D11 \_ RENDER TARGET BLEND \_ \_ \_ DESC1).**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1) |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device::CreateBuffer




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | I buffer non possono avere visualizzazioni di destinazione di rendering.<br /> I buffer devono avere esattamente D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.<br /> Consente solo buffer di indice con DXGI_FORMAT_R16_UINT formato. <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  I buffer non possono avere visualizzazioni di destinazione di rendering.<br /> I buffer devono avere esattamente D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.<br /> Consente buffer di indice con i DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT come D3D_FEATURE_LEVEL_10_0 e versioni successive. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device::CreateCounter




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device::CreateDepthStencilView




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supporta lo stencil a due lati.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device::CreateDomainShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*. ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device::CreateGeometryShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device::CreateGeometryShaderWithStreamOutput




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device::CreateHullShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device::CreateInputLayout



| Livello di funzionalità             | Differenze di comportamento                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | Non supporta INPUT D3D11 \_ \_ PER DATI \_ ISTANZA \_                                                                |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 2 | Non supporta INPUT D3D11 \_ \_ PER DATI \_ ISTANZA \_                                                                |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 3 | Il flusso del vertice zero deve avere D3D11 INPUT PER VERTEX DATA, se i flussi hanno \_ \_ \_ \_ D3D11 \_ INPUT \_ PER \_ VERTEX \_ DATA |



 

Per informazioni dettagliate sui formati che è possibile usare per i dati dei vertici a ogni livello di funzionalità, vedere il grafico supporto del formato in base al livello di funzionalità. [](overviews-direct3d-11-devices-downlevel-intro.md)

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device::CreatePixelShader



| Livello di funzionalità             | Differenze di comportamento                                    |
|---------------------------|---------------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | Deve usare ps \_ 4 \_ 0 \_ livello \_ 9 \_ 1                          |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 2 | Deve usare ps \_ 4 \_ 0 \_ livello \_ 9 \_ 1                          |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 3 | Deve usare ps \_ 4 \_ 0 \_ livello \_ 9 \_ 3 o ps \_ 4 \_ 0 \_ livello \_ 9 \_ 1 |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device::CreatePredicate




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatequery"></a>ID3D11Device::CreateQuery



| Livello di funzionalità             | Differenze di comportamento                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | Le query di eventi sono supportate. Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto.               |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 2 | Sono supportate le query di evento e occlusione. Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto. |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 3 | Sono supportate le query di evento e occlusione. Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device::CreateRasterizerState




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | DepthClipEnable deve essere <strong>TRUE.</strong> DepthBiasClamp deve essere impostato su 0.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device::CreateRenderTargetView




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Può supportare solo le visualizzazioni di destinazione di rendering degli oggetti Texture2D.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device::CreateSamplerState




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Il filtro di confronto non è supportato.<br /> Il colore del bordo deve essere compreso tra [0,1]<br /> Min LOD non può essere frazionaria<br /> Max LOD must be FLT_MAX<br /> L'anisotropia massima è 2.<br /> D3D11_TEXTURE_ADDRESS_MIRRORONCE non è supportato.<br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Il filtro di confronto non è supportato.<br /> Il colore del bordo deve essere compreso tra [0,1]<br /> Min LOD non può essere frazionaria<br /> Max LOD must be FLT_MAX<br /> L'anisotropia massima è 16.<br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device::CreateShaderResourceView



| Livello di funzionalità             | MostDetailedMip e MipLevels devono includere il livello di dettaglio più basso (sottorisorsa più piccola) | La vista deve includere tutti gli elementi della matrice di risorse |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | Sì                                                                          | sì                                           |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 2 | Sì                                                                          | Sì                                           |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 3 | Sì                                                                          | Sì                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device::CreateTexture1D




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device::CreateTexture2D

Le risorse Texture2D hanno limiti per la larghezza e l'altezza che differiscono tra [i livelli di funzionalità.](overviews-direct3d-11-devices-downlevel-intro.md) Nei livelli di funzionalità 9 3 sono garantiti i minimi garantiti e le \_ singole implementazioni possono superare i requisiti.



| Livello di funzionalità             | Se MipCount > 1, Dimensions deve essere una potenza integrale di due | Dimensione minima della trama supportata | Le dimensioni delle trame del cubo devono essere potenza di due | Se l'opzione MISC \_ TEXTURECUBE è impostata, ArraySize è: | Se l'opzione MISC \_ TEXTURECUBE non è impostata, arraySize è . |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | Sì                                                          | 2048                                | Sì                                           | 6                                              | 1                                                  |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 2 | Sì                                                          | 2048                                | Sì                                           | 6                                              | 1                                                  |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 3 | Sì                                                          | 4096                                | Sì                                           | 6                                              | 1                                                  |



 

Nella tabella precedente il nome completo di **MISC \_ TEXTURECUBE** è [**D3D11 \_ RESOURCE \_ MISC \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).

Di seguito sono riportati i 9 livelli \_ \* [di funzionalità:](overviews-direct3d-11-devices-downlevel-intro.md)

-   Quando si usa D3D11 \_ USAGE \_ DEFAULT o D3D11 \_ USAGE \_ IMMUTABLE, BindFlags non può essere zero.
-   Quando si usa D3D11 \_ BIND \_ DEPTH \_ STENCIL, MipLevels deve essere 1.
-   Quando si usa la risorsa BIND SHADER D3D11, \_ \_ \_ SampleDesc.Count deve essere 1.
-   Quando si usa D3D11 BIND PRESENT, la risorsa non può avere una risorsa \_ \_ BIND SHADER D3D11. \_ \_ \_
-   Quando si usa D3D10 DDI RESOURCE MISC SHARED, Format non può essere \_ \_ \_ \_ DXGI \_ FORMAT \_ R8G8B8A8 UNORM o \_ DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device::CreateTexture3D



| Livello di funzionalità             | Dimensione massima (qualsiasi asse) | Le dimensioni devono essere potenza di due |
|---------------------------|------------------------------|---------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | 256                          | Sì                             |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 2 | 512                          | Sì                             |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 3 | 512                          | Sì                             |



 

Se la risorsa è D3D11 \_ USAGE \_ DEFAULT o D3D11 \_ USAGE \_ IMMUTABLE, BindFlags non può essere zero.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device::CreateUnorderedAccessView




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device::CreateVertexShader



| Livello di funzionalità             | Differenze di comportamento                                    |
|---------------------------|---------------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | Deve usare rispetto a \_ 4 \_ 0 \_ livello \_ 9 \_ 1                          |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 2 | Deve usare rispetto a \_ 4 \_ 0 \_ livello \_ 9 \_ 1                          |
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 3 | Deve usare rispetto a \_ 4 \_ 0 \_ livello \_ 9 \_ 3 o \_ 4 \_ 0 \_ livello \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device::OpenSharedResource




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Usare <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> con il valore <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> e la struttura <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> per determinare se un formato può essere condiviso. Se il formato può essere condiviso, <strong>CheckFeatureSupport</strong> restituisce <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> flag .<br /><blockquote>[!Note]<br />[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> non sono mai condivisibili quando si usa il livello di funzionalità 9, anche se il dispositivo indica il supporto delle funzionalità facoltativo <strong>per D3D11_FORMAT_SUPPORT_SHAREABLE</strong>. Il tentativo di creare risorse condivise <strong></strong> con formati DXGI DXGI_FORMAT_R8G8B8A8_UNORM e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> avrà sempre esito negativo a meno che il livello di funzionalità non sia 10_0 o superiore.</blockquote><br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

