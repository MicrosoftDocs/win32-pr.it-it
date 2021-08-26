---
title: Differenze tra vertex shader
description: Differenze tra vertex shader
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 411a3a742fca508839651d56912fa00b2a6d8b82908b159694a3b1eff88f2318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982821"
---
# <a name="vertex-shader-differences"></a>Differenze tra vertex shader

## <a name="instruction-slots"></a>Slot di istruzioni

Ogni versione supporta un numero diverso di slot di istruzioni massimi.



| Versione  | Numero massimo di slot di istruzioni                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | Almeno 512 e fino al numero di slot in D3DCAPS9. MaxVertexShader30InstructionSlots. Vedere [**D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) |



 

Per informazioni sulle limitazioni degli shader software, vedere [Software Shader.](dx9-graphics-reference-asm-software-shaders.md)

## <a name="flow-control-nesting-limits"></a>Flow Limiti di annidamento dei controlli

-   Vedere [Flow limiti di annidamento dei controlli.](dx9-graphics-reference-asm-vs-instructions-flow-control.md)

## <a name="vs_1_1-features"></a>Vs 1 1 1 Features (Funzionalità di vs \_ \_ 1 1)

Nuove istruzioni:

Vedere [Instructions - vs 1 1 ( Istruzioni - vs \_ \_ 1 1).](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md)

Nuovi registri:

Vedere [Registri - vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>Vs 2 0 Features (Funzionalità di vs \_ \_ 2 0)

Nuove funzionalità:

-   Controllo di flusso statico
-   Sono disponibili tutti e quattro [i componenti](dx9-graphics-reference-asm-vs-registers-address.md) del registro indirizzi (a0).

Nuove istruzioni:

-   Istruzioni di installazione - [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)
-   Istruzioni aritmetiche - [abs -](abs---vs.md)vs , [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)
-   Istruzioni per il controllo di flusso statico - call [- vs](call---vs.md), [callnz bool - vs](callnz-bool---vs.md), else [-](else---vs.md)vs , [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), if [bool - vs](if-bool---vs.md), label - [vs](label---vs.md), loop [- vs](loop---vs.md), rep - [vs](rep---vs.md), [ret - vs](ret---vs.md)

Nuovi registri:

-   [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Registro contatori cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)

## <a name="vs_2_x-features"></a>Vs \_ 2 \_ x Features

Nuove funzionalità (D3DCAPS9. VS20Caps):

-   Controllo dinamico del flusso
-   Annidamento per istruzioni di controllo dinamico e statico del flusso
-   Numero di [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) aumentati
-   Predicazione

Nuove istruzioni:

-   Istruzioni per il controllo dinamico del flusso - break [- vs](break---vs.md), break comp [- \_ vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), if comp - [ \_ vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp comp - \_ vs](setp-comp---vs.md)

Nuovi registri:

-   [Registro predicati](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)

## <a name="vs_3_0-features"></a>Vs 3 0 Features (Funzionalità di vs \_ \_ 3 0)

Nuove funzionalità:

-   Ricerca trame
-   Registri di [output indicizzabili](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# )
-   Numero di [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) aumentati a 32

Nuove istruzioni:

-   Istruzione di installazione - [dcl \_ samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)
-   Istruzione texture - [texldl - vs](texldl---vs.md)

Nuovi registri:

-   [Campionatore (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 