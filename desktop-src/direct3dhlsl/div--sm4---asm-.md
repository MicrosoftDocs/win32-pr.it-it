---
title: div (SM4-ASM)
description: Divisione a livello di componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046080"
---
# <a name="div-sm4---asm"></a>div (SM4-ASM)

Divisione a livello di componente.



| div \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nel \] risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] dividendo.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nel \] divisore.<br/>                 |



 

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.

Si notino le due implementazioni consentite di divide: a/b e a \* (1/b).

Un risultato è che sono presenti eccezioni alla tabella seguente per i valori del denominatore di grandi dimensioni (maggiore di 8.5070592 e + 37), dove 1/denominatore è una denorma. Poiché le implementazioni possono eseguire la divisione come \* (1/b), anziché a/b direttamente e 1/ \[ grande valore \] è una denorma che può essere scaricata, alcuni casi nella tabella produrrebbe risultati diversi. Ad esempio, il valore (+/-) INF/(+/-) \[ > 8.5070592 e + 37 \] può produrre Nan in alcune implementazioni, ma (+/-) inf in altre implementazioni

In questa tabella F indica un numero reale finito.



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **src1 src0->** | **-INF** | **-F**     | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F**     | **+ INF** | **Nan** |
| **-INF**            | -inf     | -inf       | -inf        | -inf   | -inf   | -inf        | -inf       | NaN      | NaN     |
| **-F**              | -inf     | -F         | src0        | src0   | src0   | src0        | +-F o +-0 | +inf     | NaN     |
| **-denorm**         | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **-0**              | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **+0**              | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ denorm**         | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ F**              | -inf     | +-F o +-0 | src0        | src0   | src0   | src0        | + F         | +inf     | NaN     |
| **+ INF**            | NaN      | +inf       | +inf        | +inf   | +inf   | +inf        | +inf       | +inf     | NaN     |
| **NaN**             | NaN      | NaN        | NaN         | NaN    | NaN    | NaN         | NaN        | NaN      | NaN     |



 

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

 

 





