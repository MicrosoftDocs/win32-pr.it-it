---
title: ret (sm4 - asm)
description: Istruzione Return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7482c2c7351944824e2590f5c87dac63bde8f639a5ad42dffdfc71e4134603b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853751"
---
# <a name="ret-sm4---asm"></a>ret (sm4 - asm)

Istruzione Return.



| Ret |
|-----|



 

## <a name="remarks"></a>Commenti

Se all'interno di una subroutine, tornare all'istruzione dopo la chiamata. Se non si trova all'interno di una subroutine, terminare l'esecuzione del programma.

L'esempio seguente illustra come usare questa istruzione.

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

-   **Ret** può essere visualizzato in qualsiasi punto di un programma, in qualsiasi numero di volte.
-   Se [un'istruzione](label--sm4---asm-.md) etichetta viene visualizzata in uno shader, deve essere preceduta da un **comando ret** che non è annidato in alcuna istruzione di controllo di flusso.
-   Se in uno shader sono presenti subroutine, l'ultima istruzione nello shader deve essere **ret**.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




