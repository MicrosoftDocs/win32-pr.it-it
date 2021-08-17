---
title: ubfe (sm5 - asm)
description: Dato un intervallo di bit in un numero, spostare tali bit nell'LSB e impostare i bit rimanenti su 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3149173bf495957bb38800234e4d853d0e32797254eecfdb3e5b77faf4498ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722162"
---
# <a name="ubfe-sm5---asm"></a>ubfe (sm5 - asm)

Dato un intervallo di bit in un numero, spostare tali bit nell'LSB e impostare i bit rimanenti su 0.



| ubfe dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle, \] src2 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Contiene i risultati dell'istruzione .<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] I 5 bit LSB forniscono la larghezza del campo di bit (0-31).<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] I 5 bit LSB di *src1* forniscono l'offset del campo di bit (0-31).<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Numero da spostare.<br/>                                         |



 

## <a name="remarks"></a>Commenti

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

Usare questa istruzione per decomprimere i flag o gli interi senza segno.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





