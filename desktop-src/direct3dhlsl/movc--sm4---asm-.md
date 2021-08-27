---
title: movc (sm4 - asm)
description: Spostamento condizionale per componente. | movc (sm4 - asm)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81da36b39f60929bdfbac3b4a37c379189cf358ed4844e1a4cc899f867970065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095361"
---
# <a name="movc-sm4---asm"></a>movc (sm4 - asm)

Spostamento condizionale per componente.



| movc \[ \_ sat \] dest \[ \] .mask, src0 \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle, \] \[ - \] src2 \[ \_ abs \] \[ .swizzle \] , |
|----------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione. <br/> Se *src0*, *dest*  =  *src1* else *dest*  =  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti in cui testare la condizione.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Componenti da spostare. <br/>                                                                                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Componenti da spostare.<br/>                                                                                      |



 

## <a name="remarks"></a>Commenti

L'esempio seguente illustra come usare questa istruzione.

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

I modificatori in *src1* e *src2*, diversi da swizzle, presuppongono che i dati siano a virgola mobile. L'assenza di modificatori sposta semplicemente i dati senza modificare i bit.

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

 

 





