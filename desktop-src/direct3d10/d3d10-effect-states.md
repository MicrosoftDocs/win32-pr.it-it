---
description: Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Gruppi di stati effetti (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351741"
---
# <a name="effect-state-groups-direct3d-10"></a>Gruppi di stati effetti (Direct3D 10)

Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.

## <a name="blend-state"></a>Stato di Blend

| | |
|-|-|
| **ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK** | Membri di [ **D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>Stato profondità e stencil

| | |
|-|-|
| **DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK** | Membri di [ **D3D10 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| FRONTFACESTENCILFAIL * *, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS, BACKFACESTENCILFUNC**  | Membro di [ **D3D10 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>Stato rasterizzazione

| | |
|-|-|
| FILLMODE | [**\_Modalità di riempimento D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| CULLMODE | [**\_Modalità di eliminazione D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE** | Membri di [ **D3D10 \_ rasterizzator \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>Stato campionatore

| | |
|-|-|
| **Filter**, **AddressList**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD** | Membri del [ **\_ campionatore D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Per esempi, vedere [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .

## <a name="effect-object-state"></a>Stato dell'oggetto effetto

| Questo oggetto effetto | Mapping a |
|-|-|
| RASTERIZERSTATE | Oggetto stato di [rasterizzazione dello stato](#rasterizer-state) . |
| DEPTHSTENCILSTATE | Oggetto di stato di [profondità e stencil](#depth-and-stencil-state) . |
| BLENDSTATE | Oggetto di stato di [Blend](#blend-state) . |
| VERTEXSHADER | Oggetto vertex shader compilato. |
| PIXELSHADER | Oggetto pixel shader compilato. |
| GEOMETRYSHADER | Oggetto Geometry shader compilato. |
| DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK | Membri di [**D3D10 \_ pass \_ desc**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc). |

## <a name="defining-and-using-state-objects"></a>Definizione e utilizzo di oggetti stato

Gli oggetti di stato vengono dichiarati in file FX nel formato seguente. *StateObjectType* è uno degli Stati elencati sopra e *memberName* è il nome di qualsiasi membro che avrà un valore non predefinito.

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

Per impostare, ad esempio, un oggetto di stato Blend con AlphaToCoverageEnable e BlendEnable \[ 0 \] impostato su **false**, viene utilizzato il codice seguente.

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

L'oggetto di stato viene applicato a un passaggio di tecnica usando una delle funzioni SetStateGroup descritte in [effetto della sintassi tecnica (Direct3D 10)](d3d10-effect-technique-syntax.md). Per applicare, ad esempio, l'oggetto BlendState descritto sopra, verrebbe utilizzato il codice seguente.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Per un'esercitazione che descrive l'uso degli Stati, vedere la pagina relativa alla [gestione dello stato](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="related-topics"></a>Argomenti correlati

* [Sintassi della tecnica degli effetti](d3d10-effect-technique-syntax.md)
* [Formato effetto (Direct3D 10)](d3d10-effect-format.md)
