---
title: dmul (SM5-ASM)
description: Moltiplicazione a precisione doppia per componente.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993053"
---
# <a name="dmul-sm5---asm"></a>dmul (SM5-ASM)

Moltiplicazione a precisione doppia per componente.



| dmul \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/> *dest*  =  *src0* \* *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti da moltiplicare con *src1*.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] componenti da moltiplicare con *src0*.<br/>                                          |



 

## <a name="remarks"></a>Commenti

I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw. Le maschere *dest* valide sono. XY,. ZW e. xyzw. I mapping *src* seguenti sono post-swizzle:

-   *dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.

F indica un numero reale finito.



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **src1 src0->** | **-INF** | **-F** | **-1,0** | **-0** | **+0** | **+ 1,0** | **+ F** | **+ INF** | **NaN** |
| **-INF**           | +inf     | +inf   | +inf     | NaN    | NaN    | -inf     | -inf   | -inf     | NaN     |
| **-F**             | +inf     | + F     | -src0    | +0     | -0     | src0     | -F     | -inf     | NaN     |
| **-1.0 f**          | +inf     | -src1  | + 1,0     | +0     | -0     | -1.0     | -src1  | -inf     | NaN     |
| **-0**             | NaN      | +0     | +0       | +0     | -0     | -0       | -0     | NaN      | NaN     |
| **+0**             | NaN      | -0     | -0       | -0     | +0     | +0       | +0     | NaN      | NaN     |
| **+ 1,0**           | -inf     | src1   | -1.0     | -0     | +0     | +1       | src1   | +inf     | NaN     |
| **+ F**             | -inf     | -F     | -src0    | -0     | +0     | src0     | + F     | +inf     | NaN     |
| **+ INF**           | -inf     | -inf   | -inf     | NaN    | NaN    | +inf     | +inf   | +inf     | NaN     |
| **NaN**            | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





