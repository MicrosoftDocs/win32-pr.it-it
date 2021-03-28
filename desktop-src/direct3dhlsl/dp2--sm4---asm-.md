---
title: DP2 (SM4-ASM)
description: 2-dimensional Vector dot-prodotto dei componenti RG, POS-Swizzle.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398215"
---
# <a name="dp2-sm4---asm"></a>DP2 (SM4-ASM)

2-dimensional Vector dot-prodotto dei componenti RG, POS-Swizzle.



| DP2 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione. <br/> *dest*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti dell'operazione.<br/>                                                                             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] componenti dell'operazione.<br/>                                                                             |



 

## <a name="remarks"></a>Commenti

Risultato scalare replicato in componenti nella maschera di scrittura.

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

 

 





