---
title: caso (SM4-ASM)
description: Etichetta in un'istruzione switch.
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976370"
---
# <a name="case-sm4---asm"></a>caso (SM4-ASM)

Etichetta in un'istruzione switch.



| Case \[ 32-bit immediate\] |
|---------------------------|



 

## <a name="remarks"></a>Commenti

Poiché il passaggio attraverso i **case** è valido solo se non viene aggiunto codice, più **case** (incluso il [valore predefinito](default--sm4---asm-.md)) possono condividere lo stesso blocco di codice.

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

 

 




