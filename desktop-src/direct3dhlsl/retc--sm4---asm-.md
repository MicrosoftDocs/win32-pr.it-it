---
title: retc (sm4 - asm)
description: Restituzione condizionale.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d65cf64c3c1fb7945f93053f280be3eb3bd9d5fe76e34f30102316b1f1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853741"
---
# <a name="retc-sm4---asm"></a>retc (sm4 - asm)

Restituzione condizionale.



| retc{ \_ z\|\_nz} src0.select \_ component |
|----------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] registro in cui testare la condizione.<br/> |



 

## <a name="remarks"></a>Commenti

Se all'interno di una subroutine, questa istruzione torna in modo condizionale all'istruzione dopo la chiamata. Se non si trova all'interno di una subroutine, questa istruzione termina l'esecuzione del programma.

L'esempio seguente illustra come usare questa istruzione.

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a>Restrizioni

-   **retc** può essere visualizzato in qualsiasi punto di un programma, in qualsiasi numero di volte.
-   L'ultima istruzione in un programma principale o in una subroutine non può essere **retc \_ z** o **retc \_ nz**. È invece possibile usare il [ret non](ret--sm4---asm-.md) condizionale.
-   Il registro a 32 bit fornito da *src0* viene testato a livello di bit. Se un bit qualsiasi è diverso da zero, **ret \_ nz** restituirà . Se tutti i bit sono pari a zero, **retc \_ z** restituirà .

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

 

 





