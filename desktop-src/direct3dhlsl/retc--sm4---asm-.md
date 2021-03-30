---
title: RETC (SM4-ASM)
description: Risultato condizionale.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976442"
---
# <a name="retc-sm4---asm"></a>RETC (SM4-ASM)

Risultato condizionale.



| RETC { \_ z \|\_NZ} src0. Select ( \_ componente) |
|----------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] registro in cui verificare la condizione.<br/> |



 

## <a name="remarks"></a>Commenti

Se all'interno di una subroutine, questa istruzione restituisce in modo condizionale l'istruzione dopo la chiamata. Se non si trova all'interno di una subroutine, questa istruzione termina l'esecuzione del programma.

Nell'esempio seguente viene illustrato come utilizzare questa istruzione.

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

-   **RETC** possono essere presenti in qualsiasi punto di un programma, un numero qualsiasi di volte.
-   L'ultima istruzione in un programma principale o in una subroutine non può essere **RETC \_ z** o **RETC \_ NZ**. Al contrario, è possibile utilizzare il [ret](ret--sm4---asm-.md) non condizionale.
-   Il registro a 32 bit fornito da *src0* viene testato a livello di bit. Se un bit è diverso da zero, **ret \_ NZ** restituirà. Se tutti i bit sono zero, **RETC \_ z** restituirà.

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

 

 





