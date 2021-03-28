---
title: Gruppi di stati effetti (Direct3D 11)
description: Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- effetti, gruppi di stato (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963110"
---
# <a name="effect-state-groups-direct3d-11"></a>Gruppi di stati effetti (Direct3D 11)

Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.

-   [Stato di Blend](#blend-state)
-   [Stato profondità e stencil](#depth-and-stencil-state)
-   [Stato rasterizzazione](#rasterizer-state)
-   [Stato campionatore](#sampler-state)
-   [Stato dell'oggetto effetto](#effect-object-state)
-   [Definizione e utilizzo di oggetti stato](#defining-and-using-state-objects)
-   [Argomenti correlati](#related-topics)

## <a name="blend-state"></a>Stato di Blend



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK | Membri di [ **d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>Stato profondità e stencil



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK                                                                                 | Membri di [ **d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC | Membro di [ **d3d11 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>Stato rasterizzazione



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| FILLMODE                                                                                                                        | [**\_Modalità di riempimento d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| CULLMODE                                                                                                                        | [**\_Modalità di eliminazione d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE | Membri di [ **d3d11 \_ rasterizzator \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>Stato campionatore



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filter Address AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD | Membri del [ **\_ campionatore d3d11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

Per esempi, vedere [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) .

## <a name="effect-object-state"></a>Stato dell'oggetto effetto



| Questo oggetto effetto                          | Mapping a                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| RASTERIZERSTATE                             | Oggetto stato di [rasterizzazione dello stato](#rasterizer-state) .               |
| DEPTHSTENCILSTATE                           | Oggetto di stato di [profondità e stencil](#depth-and-stencil-state) . |
| BLENDSTATE                                  | Oggetto di stato di [Blend](#blend-state) .                         |
| VERTEXSHADER                                | Oggetto vertex shader compilato.                                    |
| PIXELSHADER                                 | Oggetto pixel shader compilato.                                     |
| GEOMETRYSHADER                              | Oggetto Geometry shader compilato.                                  |
| DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK | Membri di [**D3DX11 \_ pass \_ desc**](d3dx11-pass-desc.md).          |



 

## <a name="defining-and-using-state-objects"></a>Definizione e utilizzo di oggetti stato

Gli oggetti di stato vengono dichiarati in file FX nel formato seguente. StateObjectType è uno degli Stati elencati sopra e MemberName è il nome di qualsiasi membro che avrà un valore non predefinito.


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



Per impostare, ad esempio, un oggetto di stato Blend con AlphaToCoverageEnable e BlendEnable \[ 0 \] impostato su **false** , viene utilizzato il codice seguente.


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



L'oggetto di stato viene applicato a un passaggio di tecnica usando una delle funzioni SetStateGroup descritte in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md). Per applicare, ad esempio, l'oggetto BlendState descritto sopra, verrebbe utilizzato il codice seguente.


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi della tecnica degli effetti](d3d11-effect-technique-syntax.md)
</dt> <dt>

[Formato effetto (Direct3D 11)](d3d11-effect-format.md)
</dt> </dl>

 

 