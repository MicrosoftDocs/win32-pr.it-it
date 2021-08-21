---
title: dmovc (sm5 - asm)
description: Spostamento condizionale per componente. | dmovc (sm5 - asm)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0ed15d81a91d8a93ce99eda3fa17b91900e0045301f1c5b5d1f56e4448954a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792382"
---
# <a name="dmovc-sm5---asm"></a>dmovc (sm5 - asm)

Spostamento condizionale per componente.



| dmovc \[ \_ sat \] dest \[ \] .mask, src0 \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle, \] \[ - \] src2 \[ \_ abs \] \[ .swizzle \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Destinazione di spostamento.<br/> Se *src0*, *dest*  =  *src1* else *dest*  =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti in cui testare la condizione.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Componenti da spostare se la condizione è true.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Componenti da spostare se la condizione è false.<br/>                                      |



 

## <a name="remarks"></a>Commenti

L'esempio seguente illustra come usare questa istruzione.

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

Le maschere valide per dest sono .xy, .zw, .xyzw.

Gli swizzle validi per *src0* sono qualsiasi cosa. I primi due componenti post-scorrimento vengono usati per rientrare due valori di condizione a 32 bit.

Gli swizzle validi per *src1* e *src2* contenenti valori double sono xyzw, xyxy, zwxy, zwzw. sono .xy, .zw e .xyzw.

I mapping *src* seguenti sono post-swizzle:

-   *dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* è un vec2 a 32 bit/componente tra x e y (zw ignorato).
-   *src1* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src2* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

I modificatori in *src1* e *src2*, diversi da swizzle, presuppongono che i dati siano double. L'assenza di modificatori sposta i dati senza modificare i bit.

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

 

 





