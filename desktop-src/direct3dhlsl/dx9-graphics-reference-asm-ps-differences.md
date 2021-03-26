---
title: Differenze di pixel shader
description: Differenze di pixel shader
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399212"
---
# <a name="pixel-shader-differences"></a>Differenze di pixel shader

## <a name="instruction-slots"></a>Slot di istruzioni

Ogni versione supporta un numero diverso di slot di istruzioni massime.



| Versione  | Numero massimo di slot di istruzioni                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| PS \_ 1 \_ 1 | 4 trama + 8 aritmetica                                                                                              |
| PS \_ 1 \_ 2 | 4 trama + 8 aritmetica                                                                                              |
| PS \_ 1 \_ 3 | 4 trama + 8 aritmetica                                                                                              |
| PS \_ 1 \_ 4 | 6 trama + 8 aritmetico per fase                                                                                    |
| PS \_ 2 \_ 0 | 32 trama + 64 aritmetico                                                                                            |
| PS \_ 2 \_ x | 96 minimo e fino al numero di slot in D3DCAPS9. D3DPSHADERCAPS2 \_ 0. NumInstructionSlots. Vedere D3DPSHADERCAPS2 \_ 0. |
| PS \_ 3 \_ 0 | 512 minimo e fino al numero di slot in D3DCAPS9. MaxPixelShader30InstructionSlots. Vedere D3DPSHADERCAPS2 \_ 0.      |



 

Per informazioni sulle limitazioni degli shader software, vedere [software shaders](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Limiti di nidificazione del controllo di flusso

-   Vedere [limitazioni del controllo di flusso](dx9-graphics-reference-asm-ps-instructions-flow-control.md).

## <a name="ps_1_x-features"></a>Funzionalità di PS \_ 1 \_ x

Nuove istruzioni:

Vedere [ \_ \_ le istruzioni PS 1 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).

Nuovi registri:

Vedere i registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 4.

## <a name="ps_2_0-features"></a>Funzionalità di PS \_ 2 \_ 0

Nuove funzionalità:

-   Tre nuovi swizzles-. yzxw,. zxyw,. wzyx
-   Il numero di [registri temporanei](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) è aumentato a 12
-   Numero di registri di [Registro float costanti](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) aumentati a 32
-   Il numero di [registri delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t) è \# aumentato a 8

Nuove istruzioni:

-   Istruzioni di installazione- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)
-   Istruzioni aritmetiche [-ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [Exp-PS](exp---ps.md), [FRC-PS](frc---ps.md), [log-PS](log---ps.md), [M3X2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), m4x3 [-PS](m4x3---ps.md), [M4x4-PS](m4x4---ps.md), [max-PS](max---ps.md), [min-PS](min---ps.md), [NRM-PS](nrm---ps.md), [POW-PS](pow---ps.md), [RCP-](rcp---ps.md)PS, [RSQ-PS](rsq---ps.md), [SinCos-PS](sincos---ps.md)
-   Istruzioni di trama- [texld-PS \_ 2 \_ 0 e su](texld---ps-2-0.md) (sintassi diversa), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)

Nuovi registri:

-   [Campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) / \# i

## <a name="ps_2_x-features"></a>Funzionalità di PS \_ 2 \_ x

Nuove funzionalità (vedere [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)):

-   Controllo dinamico di flusso
-   Controllo di flusso statico
-   Annidamento per istruzioni di controllo di flusso statiche e dinamiche
-   Il numero di [registri temporanei](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) è aumentato
-   Swizzle di origine arbitrario
-   Istruzioni gradiente
-   Predicazione
-   Nessun limite di lettura della trama dipendente
-   Nessun limite di istruzioni di trama

Nuove istruzioni:

-   Istruzioni per il controllo di flusso statico: [se bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [endif-PS](endif---ps.md), [Rep-PS](rep---ps.md), [endrep-PS](endrep---ps.md), [Label-PS](label---ps.md), [ret-PS](ret---ps.md)
-   Istruzioni per il controllo dinamico del flusso- [break-PS](break---ps.md), [break \_ comp-PS](break-comp---ps.md), [Breakp-PS](break-p---ps.md), [callnz prede-PS](callnz-pred---ps.md), [if \_ comp-PS](if-comp---ps.md), [if prede-PS](if-pred---ps.md), [setp \_ comp-PS](setp-comp---ps.md)
-   Istruzioni aritmetiche- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)
-   Istruzione di trama- [texldd-PS](texldd---ps.md)

Nuovi registri:

-   [Registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0)

## <a name="ps_3_0-features"></a>Funzionalità di PS \_ 3 \_ 0

Nuove funzionalità:

-   10 [registri di input](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)consolidati s (v \# )
-   [Registro colori input](dx9-graphics-reference-asm-ps-registers-input-color.md) indicizzabile (v \# ) con [registro contatori cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al)
-   Il numero di [registri temporanei](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) è aumentato a 32
-   Il numero di [registri float costanti](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) è aumentato a 224

Nuove istruzioni:

-   Istruzioni di installazione [- \_ semantica DCL (SM3-PS ASM)](dcl-usage---ps.md)
-   Istruzioni per il flusso statico- [ciclo PS](loop---ps.md), [EndLoop-PS](endloop---ps.md)
-   Istruzione aritmetica- [SinCos-PS](sincos---ps.md) (nuova sintassi)
-   Istruzione di trama- [texldl-PS](texldl---ps.md)

Nuovi registri:

-   [Registro di input](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )
-   [Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)
-   [Registro viso](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 