---
title: dmovc (SM5-ASM)
description: Spostamento condizionale a livello di componente. | dmovc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401864"
---
# <a name="dmovc-sm5---asm"></a>dmovc (SM5-ASM)

Spostamento condizionale a livello di componente.



| dmovc \[ \_ Sat \] dest \[ . mask \] , src0 \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nella \] destinazione di spostamento.<br/> Se *src0*, quindi *dest*  =  *src1* else *dest*  =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti su cui eseguire il test della condizione.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] componenti da spostare se la condizione è true.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[nei \] componenti da spostare se la condizione è false.<br/>                                      |



 

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrato come utilizzare questa istruzione.

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

Le maschere valide per dest sono. XY,. ZW,. xyzw.

Il valore di swizzles valido per *src0* è qualsiasi. I primi due componenti post-swizzle vengono usati per identificare i valori di condizione a 2 32 bit.

Il valore di swizzles valido per *src1* e *src2* che contiene i valori Double è. xyzw,. Xyxy,. zwxy,. zwzw. sono. XY,. ZW e. xyzw.

I mapping *src* seguenti sono post-swizzle:

-   *dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* è un vec2 a 32 bit/componente tra x e y (ZW ignorato).
-   *src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src2* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

I modificatori in *src1* e *src2*, diversi da Swizzle, presuppongono che i dati siano Double. L'assenza di modificatori sposta i dati senza alterare i bit.

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

 

 





