---
title: Break (SM4-ASM)
description: Sposta il punto di esecuzione nell'istruzione dopo il EndLoop o endswitch successivo.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335511"
---
# <a name="break-sm4---asm"></a>Break (SM4-ASM)

Sposta il punto di esecuzione nell'istruzione dopo il [EndLoop](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md)successivo.



| break |
|-------|



 

## <a name="remarks"></a>Commenti

Il formato del token contiene l'offset dell'istruzione **EndLoop** o **endswitch** corrispondente nello shader per praticità.

Nell'esempio seguente viene illustrata l'istruzione **break** .


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



Questa istruzione deve essere visualizzata all'interno di un **ciclo** / **EndLoop** o in un **caso** in un  / **endswitch** switch.

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

 

 




