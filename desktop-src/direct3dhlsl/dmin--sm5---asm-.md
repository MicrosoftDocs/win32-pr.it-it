---
title: dmin (sm5 - asm)
description: Minimo a precisione doppia per componente.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20977a24113db111e85bc644ed68eccaa7e75db91c18bf71d80ac89f5ee19547
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855121"
---
# <a name="dmin-sm5---asm"></a>dmin (sm5 - asm)

Minimo a precisione doppia per componente.



| dmin \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati dell'operazione.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> < viene usato invece di <= in modo che se min(x,y) = x then max(x,y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti da confrontare con *src1*.<br/>                                                                                                                                                     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Componenti da confrontare con *src0*.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Commenti

NaN ha una gestione speciale. Se un operando di origine è NaN, viene restituito l'altro operando di origine. La scelta viene effettuata per componente. Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.

Gli swizzle validi per i parametri di origine sono .xyzw, .xyxy, .zwxy, .zwzw. Le maschere *DEST* valide sono .xy, .zw e .xyzw. I mapping *src* seguenti sono post-swizzle:

-   *dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

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

 

 





