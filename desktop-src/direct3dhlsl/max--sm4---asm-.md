---
title: max (sm4 - asm)
description: Valore massimo float per componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994728"
---
# <a name="max-sm4---asm"></a>max (sm4 - asm)

Valore massimo float per componente.



| max \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Risultato dell'operazione. <br/> *dest*  =  *src0*  >=  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti da confrontare con *src1*.<br/>                                                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Componenti da confrontare con *src0*.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

>= viene usato anziché > in modo che se min(x,y) = x allora max(x,y) = y.

NaN ha una gestione speciale. Se un operando di origine è NaN, viene restituito l'altro operando di origine e la scelta viene effettuata per componente. Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.

I denorm vengono scaricati con il segno mantenuto prima del confronto. Tuttavia, il risultato scritto *in dest* può essere scaricato o meno.

Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow. F indica un numero reale finito.



| **src0 src1->** | **-inf** | **F**        | **+inf** | **NaN** |
|--------------------|----------|--------------|----------|---------|
| **-inf**           | -inf     | src1         | +inf     | -inf    |
| **F**              | src0     | src0 o src1 | +inf     | src0    |
| **+inf**           | +inf     | +inf         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





