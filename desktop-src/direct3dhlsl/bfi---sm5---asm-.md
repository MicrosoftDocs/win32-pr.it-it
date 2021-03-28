---
title: BFI (SM5-ASM)
description: Dato un intervallo di bit dall'LSB di un numero, inserire tale numero di bit in un altro numero a qualsiasi offset.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046098"
---
# <a name="bfi-sm5---asm"></a>BFI (SM5-ASM)

Dato un intervallo di bit dall'LSB di un numero, inserire tale numero di bit in un altro numero a qualsiasi offset.



| BFI dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle \] , src3 \[ . Swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei risultati.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nella \] larghezza bit da *src2*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nell' \] offset bit per la sostituzione di bit in *src3*.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[il \] numero di bit da cui vengono ricavati i bit. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[nel \] numero con bit da sostituire.<br/>              |



 

## <a name="remarks"></a>Commenti

I LSB 5 bit di *src0* forniscono la larghezza bit (0-31) da *src2*.

I LSB 5 bit di *src1* forniscono l'offset bit (0-31) per iniziare a sostituire bits nel numero letto da *src3*.

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Questa istruzione viene utilizzata per la compressione di interi o flag.

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

 

 





