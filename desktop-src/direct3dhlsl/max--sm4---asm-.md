---
title: Max (SM4-ASM)
description: Valore massimo float per componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398205"
---
# <a name="max-sm4---asm"></a>Max (SM4-ASM)

Valore massimo float per componente.



| Max \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nel \] risultato dell'operazione. <br/> *dest*  =  *src0*  >=  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti da confrontare con *src1*.<br/>                                                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] componenti da confrontare con *src0*.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

>= viene usato al posto di > in modo che se min (x, y) = x then Max (x, y) = y.

NaN ha una gestione speciale. Se un operando di origine è NaN, viene restituito l'altro operando di origine e viene effettuata la scelta per ogni componente. Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.

Le denormazioni vengono scaricate con il segno mantenuto prima del confronto. Tuttavia, il risultato scritto in *dest* potrebbe o non essere denormalizzato.

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow. F indica un numero reale finito.



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| **src1 src0->** | **-INF** | **F**        | **+ INF** | **NaN** |
| **-INF**           | -inf     | src1         | +inf     | -inf    |
| **F**              | src0     | src0 o src1 | +inf     | src0    |
| **+ INF**           | +inf     | +inf         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

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

 

 





