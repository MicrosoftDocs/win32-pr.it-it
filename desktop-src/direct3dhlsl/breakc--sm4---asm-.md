---
title: breakc (SM4-ASM)
description: Sposta in modo condizionale il punto di esecuzione nell'istruzione dopo il EndLoop o endswitch successivo.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398254"
---
# <a name="breakc-sm4---asm"></a>breakc (SM4-ASM)

Sposta in modo condizionale il punto di esecuzione nell'istruzione dopo il [EndLoop](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md)successivo.



| breakc { \_ z \|\_NZ} src0. Select ( \_ componente) |
|------------------------------------------|



 



| Elemento                                                            | Descrizione                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] componente su cui eseguire il test della condizione.<br/> |



 

## <a name="remarks"></a>Commenti

Il formato del token contiene l'offset dell'istruzione **EndLoop** corrispondente nello shader per praticità.

Nell'esempio seguente viene illustrata l'istruzione **breakc** .


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Questa istruzione deve essere visualizzata all'interno di un **ciclo** / **EndLoop** o **Switch** / **endswitch**.

Il registro a 32 bit fornito da *src0* viene testato a livello di bit. Se un bit è diverso da zero, **breakc \_ NZ** eseguirà l'operazione break. Se tutti i bit sono zero, **breakc \_ z** eseguirà l'operazione break.

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

 

 





