---
title: dmul (sm5 - asm)
description: Moltiplicazione a precisione doppia per componente.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999088"
---
# <a name="dmul-sm5---asm"></a>dmul (sm5 - asm)

Moltiplicazione a precisione doppia per componente.



| dmul \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> *dest*  =  *src0* \* *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] I componenti da moltiplicare con *src1*.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] I componenti da moltiplicare con *src0*.<br/>                                          |



 

## <a name="remarks"></a>Commenti

Gli swizzle validi per i parametri di origine sono xyzw, xyxy, zwxy, zwzw. Le maschere *dest* valide sono xy, zw e xyzw. I mapping *src* seguenti sono post-swizzle:

-   *dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.

F indica un numero finito-reale.



| **src0 src1->** | **-inf** | **-F** | **-1.0** | **-0** | **+0** | **+1.0** | **+F** | **+inf** | **NaN** |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-inf**           | +inf     | +inf   | +inf     | NaN    | NaN    | -inf     | -inf   | -inf     | NaN     |
| **-F**             | +inf     | +F     | -src0    | +0     | -0     | src0     | -F     | -inf     | NaN     |
| **-1.0F**          | +inf     | -src1  | +1.0     | +0     | -0     | -1.0     | -src1  | -inf     | NaN     |
| **-0**             | NaN      | +0     | +0       | +0     | -0     | -0       | -0     | NaN      | NaN     |
| **+0**             | NaN      | -0     | -0       | -0     | +0     | +0       | +0     | NaN      | NaN     |
| **+1.0**           | -inf     | src1   | -1.0     | -0     | +0     | +1       | src1   | +inf     | NaN     |
| **+F**             | -inf     | -F     | -src0    | -0     | +0     | src0     | +F     | +inf     | NaN     |
| **+inf**           | -inf     | -inf   | -inf     | NaN    | NaN    | +inf     | +inf   | +inf     | NaN     |
| **NaN**            | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





