---
title: break (sm4 - asm)
description: Sposta il punto di esecuzione nell'istruzione dopo l'endloop o endswitch successivo.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17ca99b0e16da016145f7f23fe6e4ce6bd410325ff98d4c6dd1387943fbc718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983341"
---
# <a name="break-sm4---asm"></a>break (sm4 - asm)

Sposta il punto di esecuzione nell'istruzione dopo [l'endloop o](endloop--sm4---asm-.md) [endswitch successivo.](endswitch--sm4---asm-.md)



| break |
|-------|



 

## <a name="remarks"></a>Commenti

Il formato del token contiene l'offset dell'istruzione **endloop** o **endswitch** corrispondente nello shader per praticità.

Nell'esempio seguente viene illustrata **l'istruzione break.**


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



Questa istruzione deve essere presente all'interno **di** / **un endloop del ciclo** o in un **caso** in **un switch** / **endswitch**.

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

 

 




