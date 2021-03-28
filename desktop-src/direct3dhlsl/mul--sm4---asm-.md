---
title: Mul (SM4-ASM)
description: Moltiplicazione componente.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ae22bcb9344936f9bc63e9b4fddf72dd8f6570
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335583"
---
# <a name="mul-sm4---asm"></a>Mul (SM4-ASM)

Moltiplicazione componente.



| Mul \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                        |
|-----------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nel \] risultato dell'operazione. dest = src0 \* src1<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] multiplicand.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nel \] moltiplicatore.<br/>                                  |



 

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.

F indica un numero reale finito.



|                     |          |        |          |             |        |        |            |          |        |          |         |
|---------------------|----------|--------|----------|-------------|--------|--------|------------|----------|--------|----------|---------|
| **src1 src0->** | **-INF** | **-F** | **-1,0** | **-denorm** | **-0** | **+0** | **denorm** | **+ 1,0** | **+ F** | **+ INF** | **NaN** |
| **-INF**            | +inf     | +inf   | +inf     | NaN         | NaN    | NaN    | NaN        | -inf     | -inf   | -inf     | NaN     |
| **-F**              | +inf     | + F     | -src0    | +0          | +0     | -0     | -0         | src0     | -F     | -inf     | NaN     |
| **-1**              | +inf     | -src1  | + 1,0     | +0          | +0     | -0     | -0         | -1.0     | -src1  | -inf     | NaN     |
| **-denorm**         | NaN      | +0     | +0       | +0          | +0     | -0     | -0         | -0       | -0     | NaN      | NaN     |
| **-0**              | NaN      | +0     | +0       | +0          | +0     | -0     | -0         | -0       | -0     | NaN      | NaN     |
| **+0**              | iNaN     | -0     | -0       | -0          | -0     | +0     | +0         | +0       | +0     | NaN      | NaN     |
| **+ denorm**         | NaN      | -0     | -0       | -0          | -0     | +0     | +0         | +0       | +0     | NaN      | NaN     |
| **+ 1,0**            | -inf     | src1   | -1.0     | -0          | -0     | +0     | +0         | + 1,0     | src1   | +inf     | NaN     |
| **+ F**              | -inf     | -F     | -src0    | -0          | -0     | +0     | +0         | src0     | + F     | +inf     | NaN     |
| **+ INF**            | -inf     | -inf   | -inf     | NaN         | NaN    | NaN    | NaN        | +inf     | +inf   | +inf     | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN         | NaN    | NaN    | NaN        | NaN      | NaN    | NaN      | NaN     |



 

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

 

 





