---
title: breakc (sm4 - asm)
description: Sposta in modo condizionale il punto di esecuzione nell'istruzione dopo l'endloop o endswitch successivo.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eff9be2428db0d0df24879f50964ce14f6831e235c54655958d9401224d7225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626471"
---
# <a name="breakc-sm4---asm"></a>breakc (sm4 - asm)

Sposta in modo condizionale il punto di esecuzione nell'istruzione dopo [l'endloop o](endloop--sm4---asm-.md) [endswitch successivo.](endswitch--sm4---asm-.md)



| breakc{ \_ z\|\_nz} src0.select \_ component |
|------------------------------------------|



 



| Elemento                                                            | Descrizione                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componente in cui testare la condizione.<br/> |



 

## <a name="remarks"></a>Commenti

Il formato del token contiene l'offset **dell'istruzione endloop** corrispondente nello shader per praticità.

Nell'esempio seguente viene illustrata **l'istruzione breakc.**


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Questa istruzione deve essere visualizzata all'interno di / **un ciclo endloop** o **switch** / **endswitch**.

Il registro a 32 bit fornito da *src0* viene testato a livello di bit. Se un bit qualsiasi è diverso da zero, **breakc \_ nz** eseguirà l'interruzione. Se tutti i bit sono pari a zero, **breakc \_ z** eseguirà l'interruzione.

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

 

 





