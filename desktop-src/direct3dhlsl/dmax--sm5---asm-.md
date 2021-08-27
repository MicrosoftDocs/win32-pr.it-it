---
title: dmax (sm5 - asm)
description: Valore massimo a precisione doppia per componente.
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6846da6fbf3ad5d42be5131322e1214fc49fe2627b824775798e4527de3d24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068371"
---
# <a name="dmax-sm5---asm"></a>dmax (sm5 - asm)

Valore massimo a precisione doppia per componente.



| dmax \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati dell'operazione.<br/> *dest*  =  *src0*  >=  *src1* ? *src0* : *src1*<br/> >= viene usato anziché > in modo che se min(x,y) = x allora max(x,y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valore da confrontare con *src1*.<br/>                                                                                                                                                           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Valore da confrontare con *src0*.<br/>                                                                                                                                                           |



 

## <a name="remarks"></a>Commenti

NaN ha una gestione speciale. Se un operando di origine è NaN, viene restituito l'altro operando di origine. La scelta viene effettuata per componente. Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.

Gli swizzle validi per i parametri di origine sono xyzw, xyxy, zwxy, zwzw. Le maschere *dest* valide sono xy, zw e xyzw. I mapping *src* seguenti sono post-swizzle:

-   *dest* è un doppio vec2 attraverso (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





