---
title: dmov (SM5-ASM)
description: Spostamento a livello di componente. | dmov (SM5-ASM)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969278"
---
# <a name="dmov-sm5---asm"></a>dmov (SM5-ASM)

Spostamento a livello di componente.



| dmov \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nella \] destinazione di spostamento. *dest*  =  *src0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti da spostare.<br/>            |



 

## <a name="remarks"></a>Commenti

I modificatori, diversi da Swizzle, presuppongono che i dati siano a virgola mobile. L'assenza di modificatori sposta i dati senza alterare i bit.

I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw. I mapping *src* seguenti sono post-swizzle:

-   *src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

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

 

 





