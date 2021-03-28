---
title: Aggiungi (SM4-ASM)
description: Aggiunta di 2 vettori a livello di componente.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5630b983c88da3ba512b5fece6202e0217b2ed39
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516507"
---
# <a name="add-sm4---asm"></a>Aggiungi (SM4-ASM)

Aggiunta di 2 vettori a livello di componente.



| aggiungere \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] vettore da aggiungere a *src1*.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nel \] vettore da aggiungere a *src0*.<br/>                |



 

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow. F indica un numero reale finito.



|                    |          |            |             |        |        |            |            |          |         |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| **src1 src0->** | **-INF** | **-F**     | **-denorm** | **-0** | **+0** | **denorm** | **+ F**     | **+ INF** | **NaN** |
| **-INF**           | -inf     | -inf       | -inf        | -inf   | -inf   | -inf       | -inf       | NaN      | NaN     |
| **-F**             | -inf     | -F         | src0        | src0   | src0   | src0       | +-F o +-0 | +inf     | NaN     |
| **-denorm**        | -inf     | src1       | -0          | -0     | +0     | +0         | src1       | +inf     | NaN     |
| **-0**             | -inf     | src1       | -0          | -0     | +0     | +0         | src1       | +inf     | NaN     |
| **+0**             | i-INF    | src1       | +0          | +0     | +0     | +0         | src1       | +inf     | NaN     |
| **+ denorm**        | -inf     | src1       | +0          | +0     | +0     | +0         | src1       | +inf     | NaN     |
| **+ F**             | -inf     | +-F o +-0 | src0        | src0   | src0   | src0       | + F         | +inf     | NaN     |
| **+ INF**           | NaN      | +inf       | +inf        | +inf   | +inf   | +inf       | +inf       | +inf     | NaN     |
| **NaN**            | NaN      | NaN        | NaN         | NaN    | NaN    | NaN        | NaN        | NaN      | NaN     |



 

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

 

 





