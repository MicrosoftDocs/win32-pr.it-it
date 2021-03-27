---
title: ubfe (SM5-ASM)
description: Dato un intervallo di bit in un numero, spostare tali bit in LSB e impostare i bit rimanenti su 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857770"
---
# <a name="ubfe-sm5---asm"></a>ubfe (SM5-ASM)

Dato un intervallo di bit in un numero, spostare tali bit in LSB e impostare i bit rimanenti su 0.



| ubfe dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contiene i risultati dell'istruzione.<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] LSB 5 bits specificare la larghezza bit (0-31).<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] bit LSB 5 di *src1* specificare l'offset bit (0-31).<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[nel \] numero da spostare.<br/>                                         |



 

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

Usare questa istruzione per decomprimere interi senza segno o flag.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





