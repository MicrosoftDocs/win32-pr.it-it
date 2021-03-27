---
title: Differenze di vertex shader
description: Differenze di vertex shader
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046875"
---
# <a name="vertex-shader-differences"></a>Differenze di vertex shader

## <a name="instruction-slots"></a>Slot di istruzioni

Ogni versione supporta un numero diverso di slot di istruzioni massime.



| Versione  | Numero massimo di slot di istruzioni                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | 512 minimo e fino al numero di slot in D3DCAPS9. MaxVertexShader30InstructionSlots. Vedere [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). |



 

Per informazioni sulle limitazioni degli shader software, vedere [software shaders](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Limiti di nidificazione del controllo di flusso

-   Vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md).

## <a name="vs_1_1-features"></a>funzionalità di Visual Studio \_ 1 \_ 1

Nuove istruzioni:

Vedere [le istruzioni-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Nuovi registri:

Vedere [Registers-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>Funzionalità di vs \_ 2 \_ 0

Nuove funzionalità:

-   Controllo di flusso statico
-   Sono disponibili tutti e quattro i componenti del [Registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md) (a0).

Nuove istruzioni:

-   Istruzioni di installazione- [defb-vs](defb---vs.md), [defi-vs](defi---vs.md)
-   Istruzioni aritmetiche- [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [mova-vs](mova---vs.md), [NRM-vs](nrm---vs.md), [POW-vs](pow---vs.md), [SGN-vs](sgn---vs.md), [SinCos-vs](sincos---vs.md)
-   Istruzioni per il controllo di flusso statico- [Call-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [else-vs](else---vs.md), [endif-vs](endif---vs.md), [EndLoop-vs](endloop---vs.md), [endrep-vs](endrep---vs.md), [if bool-vs](if-bool---vs.md), [Label-vs](label---vs.md), [loop-vs](loop---vs.md), [Rep-vs](rep---vs.md), [ret-vs](ret---vs.md)

Nuovi registri:

-   [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Registro Integer costante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Registro contatore cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al)

## <a name="vs_2_x-features"></a>Funzionalità di vs \_ 2 \_ x

Nuove funzionalità (D3DCAPS9. VS20Caps):

-   Controllo dinamico di flusso
-   Annidamento per istruzioni di controllo di flusso statiche e dinamiche
-   Il numero di [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) è aumentato
-   Predicazione

Nuove istruzioni:

-   Istruzioni per il controllo dinamico del flusso- [Break-vs](break---vs.md), [break \_ comp-vs](break-comp---vs.md), [Breakp-vs](breakp---vs.md), [callnz Predator-vs](callnz-pred---vs.md), [if \_ comp-vs](if-comp---vs.md), [if prede-vs](if-pred---vs.md), [setp \_ comp-vs](setp-comp---vs.md)

Nuovi registri:

-   [Registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0)

## <a name="vs_3_0-features"></a>Funzionalità di vs \_ 3 \_ 0

Nuove funzionalità:

-   Ricerca trama
-   Registri di [output](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) indicizzabili (o \# )
-   Il numero di [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) è aumentato a 32

Nuove istruzioni:

-   Istruzioni di installazione- [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)
-   Istruzione di trama- [texldl-vs](texldl---vs.md)

Nuovi registri:

-   [Campionatore (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) / \# i

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 