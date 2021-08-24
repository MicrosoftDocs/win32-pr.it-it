---
title: ibfe (sm5 - asm)
description: Dato un intervallo di bit in un numero, spostare tali bit nell'LSB e firmare estendere il valore MSB dell'intervallo.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b04bfcaea154a8a63e9b118da12a8994398357b7c6a022a4589353c6c06eb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949621"
---
# <a name="ibfe-sm5---asm"></a>ibfe (sm5 - asm)

Dato un intervallo di bit in un numero, spostare tali bit nell'LSB e firmare estendere il valore MSB dell'intervallo.



| ibfe dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle, \] src2 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Larghezza del campo di bit.<br/>                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Offset del campo di bit.<br/>                         |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Valore da spostare.<br/>                          |



 

## <a name="remarks"></a>Commenti

I 5 bit LSB di src0 forniscono la larghezza del campo di bit (0-31).

I 5 bit LSB di src1 forniscono l'offset del campo di bit (0-31).

Nell'esempio seguente viene illustrato come utilizzare questa istruzione.

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

Usare questa istruzione per decomprimere interi o flag con segno.

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

 

 





