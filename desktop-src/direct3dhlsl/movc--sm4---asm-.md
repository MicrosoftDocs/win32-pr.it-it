---
title: MOVC (SM4-ASM)
description: Spostamento condizionale a livello di componente. | MOVC (SM4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995477"
---
# <a name="movc-sm4---asm"></a>MOVC (SM4-ASM)

Spostamento condizionale a livello di componente.



| MOVC \[ \_ Sat \] dest \[ . mask \] , src0 \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle \] , |
|----------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione. <br/> Se *src0*, quindi *dest*  =  *src1* else *dest*  =  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti su cui eseguire il test della condizione.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] componenti da spostare. <br/>                                                                                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[nei \] componenti da spostare.<br/>                                                                                      |



 

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrato come utilizzare questa istruzione.

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

I modificatori in *src1* e *src2*, diversi da Swizzle, presuppongono che i dati siano a virgola mobile. L'assenza di modificatori sposta solo i dati senza alterare i bit.

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

 

 





