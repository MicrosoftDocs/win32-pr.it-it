---
title: DP3 (SM4-ASM)
description: vettore tridimensionale punto-prodotto dei componenti RGB, POS-Swizzle.
ms.assetid: 8E6EA6CD-B5BB-4D64-8846-F7B9F7135582
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2598053abed93675107f15af762e0844d4938fbf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857758"
---
# <a name="dp3-sm4---asm"></a>DP3 (SM4-ASM)

vettore tridimensionale punto-prodotto dei componenti RGB, POS-Swizzle.



| DP3 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nel \] risultato dell'operazione.<br/> *dest*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*  +  *src0. b* \* *src1. b*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti di operazione.<br/>                                                                                   |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] componenti di operazione.<br/>                                                                                   |



 

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

 

 





