---
description: Gli stati degli effetti sono coppie nome-valore sotto forma di espressione.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Gruppi di stati degli effetti (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335570"
---
# <a name="effect-state-groups-direct3d-10"></a>Gruppi di stati degli effetti (Direct3D 10)

Gli stati dell'effetto sono coppie nome-valore sotto forma di espressione.

## <a name="blend-state"></a>Stato di fusione

| Stato dell'effetto | Gruppo |
|-|-|
| **ALPHATOCOVERAGEENABLE,** **BLENDENABLE,** **SRCBLEND,** **DESTBLEND,** **BLENDOP,** **SRCBLENDALPHA,** **DESTBLENDALPHA,** **BLENDOPALPHA,** **RENDERTARGETWRITEMASK** | Membri di [ **D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>Stato di profondità e stencil

| Stato dell'effetto| Gruppo |
|-|-|
| **DEPTHENABLE,** **DEPTHWRITEMASK,** **DEPTHFUNC,** **STENCILENABLE,** **STENCILREADMASK,** **STENCILWRITEMASK** | Membri di [ **D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| **FRONTFACESTENCILFAIL,** **FRONTFACESTENCILZFAIL,** **FRONTFACESTENCILPASS,** **FRONTFACESTENCILFUNC,** **BACKFACESTENCILFAIL,** **BACKFACESTENCILZFAIL,** **BACKFACESTENCILPASS,** **BACKFACESTENCILFUNC** | Membro di [ **D3D10 \_ DEPTH \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>Stato del rasterizzatore

| Stato dell'effetto| Gruppo |
|-|-|
| Fillmode | [**MODALITÀ DI RIEMPIMENTO D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| CULLMODE | [**MODALITÀ CULL D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **FRONTCOUNTERCLOCKWISE,** **DEPTHBIAS,** **DEPTHBIASCLAMP,** **SLOPESCALEDDEPTHBIAS,** **ZCLIPENABLE,** **SCISSORENABLE,** **MULTISAMPLEENABLE,** **ANTIALIASEDLINEENABLE** | Membri di [ **D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>Stato del campionatore

| Stato dell'effetto | Gruppo |
|-|-|
| **Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD** | Membri di [ **D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Per [esempi, vedere Sampler type (DirectX HLSL) (Tipo](../direct3dhlsl/dx-graphics-hlsl-sampler.md) di campionatore ( DirectX HLSL).

## <a name="effect-object-state"></a>Stato dell'oggetto Effect

| Questo oggetto effetto | Mapping a |
|-|-|
| RASTERIZERSTATE | Oggetto [stato rasterizzatore.](#rasterizer-state) |
| DEPTHSTENCILSTATE | Oggetto [di stato Depth e Stencil State.](#depth-and-stencil-state) |
| BLENDSTATE | Oggetto [stato blend.](#blend-state) |
| VERTEXSHADER | Oggetto vertex shader compilato. |
| Pixelshader | Oggetto pixel shader compilato. |
| GEOMETRYSHADER | Oggetto geometry shader compilato. |
| DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK | Membri di [**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc). |

## <a name="defining-and-using-state-objects"></a>Definizione e uso di oggetti di stato

Gli oggetti di stato vengono dichiarati nei file FX nel formato seguente. *StateObjectType* è uno degli stati elencati in precedenza e *MemberName* è il nome di qualsiasi membro che avrà un valore non predefinito.

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

L'oggetto stato viene applicato a un passaggio di tecnica usando una delle funzioni SetStateGroup descritte in Sintassi della tecnica degli effetti [(Direct3D 10).](d3d10-effect-technique-syntax.md) Ad esempio, per applicare l'oggetto BlendState descritto sopra, verrà usato il codice seguente.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Per un'esercitazione che descrive l'uso degli stati, vedere [Gestione dello stato](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="related-topics"></a>Argomenti correlati

* [Sintassi della tecnica degli effetti](d3d10-effect-technique-syntax.md)
* [Formato effetto (Direct3D 10)](d3d10-effect-format.md)
