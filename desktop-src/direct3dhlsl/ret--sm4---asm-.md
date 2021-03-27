---
title: RET (SM4-ASM)
description: Istruzione return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719381"
---
# <a name="ret-sm4---asm"></a>RET (SM4-ASM)

Istruzione return.



| RET |
|-----|



 

## <a name="remarks"></a>Commenti

Se all'interno di una subroutine, tornare all'istruzione dopo la chiamata a. In caso contrario, terminare l'esecuzione del programma.

Nell'esempio seguente viene illustrato come utilizzare questa istruzione.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a>Restrizioni

-   **ret** può trovarsi in qualsiasi punto di un programma, un numero qualsiasi di volte.
-   Se un'istruzione [Label](label--sm4---asm-.md) viene visualizzata in uno shader, deve essere preceduta da un comando **ret** che non è annidato in alcuna istruzione di controllo di flusso.
-   Se sono presenti subroutine in uno shader, l'ultima istruzione nello shader deve essere **ret**.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




