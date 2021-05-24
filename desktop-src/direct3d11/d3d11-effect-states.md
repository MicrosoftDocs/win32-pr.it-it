---
title: Gruppi di stati degli effetti (Direct3D 11)
description: Gli stati dell'effetto sono coppie nome-valore sotto forma di espressione.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- effect, state groups (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335335"
---
# <a name="effect-state-groups-direct3d-11"></a>Gruppi di stati degli effetti (Direct3D 11)

Gli stati dell'effetto sono coppie nome-valore sotto forma di espressione.

-   [Stato di blend](#blend-state)
-   [Profondità e stato dello stencil](#depth-and-stencil-state)
-   [Stato rasterizzazione](#rasterizer-state)
-   [Stato del campionatore](#sampler-state)
-   [Stato dell'oggetto effect](#effect-object-state)
-   [Definizione e uso di oggetti di stato](#defining-and-using-state-objects)
-   [Argomenti correlati](#related-topics)

## <a name="blend-state"></a>Stato di blend



| Stato dell'effetto                                                                                                                      | Gruppo                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK | Membri di [ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>Profondità e stato dello stencil



|  Stato dell'effetto                                                                                                                                                              | Gruppo                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK                                                                                 | Membri di [ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC | Membro di [ **D3D11 \_ DEPTH \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>Stato rasterizzazione



| Stato dell'effetto                                                                                                                                | Gruppo                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Fillmode                                                                                                                        | [**MODALITÀ RIEMPIMENTO D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| CULLMODE                                                                                                                        | [**MODALITÀ CULL D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE | Membri di [ **D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>Stato del campionatore



| Stato dell'effetto                                                                                                    | Gruppo                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filtro AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD | Membri di [ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

Per [esempi, vedere Sampler Type (DirectX HLSL) (Tipo](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) di campionatore - DirectX HLSL).

## <a name="effect-object-state"></a>Stato dell'oggetto Effect



| Questo oggetto Effect                          | Mapping a                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| RASTERIZERSTATE                             | Oggetto [stato rasterizzatore.](#rasterizer-state)               |
| DEPTHSTENCILSTATE                           | Oggetto [di stato Depth e Stencil State.](#depth-and-stencil-state) |
| BLENDSTATE                                  | Oggetto [stato blend.](#blend-state)                         |
| VERTEXSHADER                                | Oggetto vertex shader compilato.                                    |
| Pixelshader                                 | Oggetto pixel shader compilato.                                     |
| GEOMETRYSHADER                              | Oggetto geometry shader compilato.                                  |
| DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK | Membri di [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md).          |



 

## <a name="defining-and-using-state-objects"></a>Definizione e uso di oggetti di stato

Gli oggetti di stato vengono dichiarati nei file FX nel formato seguente. StateObjectType è uno degli stati elencati in precedenza e MemberName è il nome di qualsiasi membro che avrà un valore non predefinito.


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



Ad esempio, per impostare un oggetto stato di blend con AlphaToCoverageEnable e BlendEnable 0 impostato su FALSE, verrà usato \[ \] il codice seguente. 


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



L'oggetto state viene applicato a un passaggio di tecnica usando una delle funzioni SetStateGroup descritte in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md). Ad esempio, per applicare l'oggetto BlendState descritto sopra, verrà usato il codice seguente.


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi della tecnica degli effetti](d3d11-effect-technique-syntax.md)
</dt> <dt>

[Formato effetto (Direct3D 11)](d3d11-effect-format.md)
</dt> </dl>

 

 