---
title: min (sm4 - asm)
description: Minimo float per componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993898"
---
# <a name="min-sm4---asm"></a>min (sm4 - asm)

Minimo float per componente.



| min \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Risultato dell'operazione.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti da confrontare con *src1*.<br/>                                                  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Componenti da confrontare con *src0*.<br/>                                                  |



 

## <a name="remarks"></a>Commenti

>= viene usato anziché > in modo che se min(x,y) = x allora max(x,y) = y.

NaN ha una gestione speciale. Se un operando di origine è NaN, viene restituito l'altro operando di origine e la scelta viene effettuata per componente. Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN. Questo è conforme alle nuove regole IEEE 754R.

I denorm vengono scaricati, con il segno mantenuto, prima del confronto. Tuttavia, il risultato scritto *in dest* può essere scaricato o meno.

La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichino overflow o underflow. F indica un numero reale finito.



| **src0 src1->** | **-inf** | **F**        | **+inf** | **NaN** |
|--------------------|----------|--------------|----------|---------|
| **-inf**           | -inf     | -inf         | -inf     | -inf    |
| **F**              | -inf     | src0 o src1 | src0     | src0    |
| **-inf**           | -inf     | src1         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





