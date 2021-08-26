---
title: bfi (sm5 - asm)
description: Dato un intervallo di bit dall'LSB di un numero, posizionare tale numero di bit in un altro numero in qualsiasi offset.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1452b1f15525753738ee6f74a1bd43473f43033346c9b493cd72222eaab22cb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068531"
---
# <a name="bfi-sm5---asm"></a>bfi (sm5 - asm)

Dato un intervallo di bit dall'LSB di un numero, posizionare tale numero di bit in un altro numero in qualsiasi offset.



| bfi dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle, \] src2 \[ .swizzle, \] src3 \[ .swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Larghezza del campo di bit da prendere da *src2*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Offset del campo di bit per la sostituzione dei bit in *src3*.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Numero da cui vengono presi i bit. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[in \] Numero con bit da sostituire.<br/>              |



 

## <a name="remarks"></a>Commenti

I 5 bit LSB di *src0* forniscono la larghezza del campo di bit (0-31) da prendere da *src2*.

I 5 bit LSB di *src1* forniscono l'offset del campo di bit (0-31) per iniziare a sostituire i bit nel numero letto da *src3*.

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Questa istruzione viene usata per la creazione di numeri interi o flag.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





