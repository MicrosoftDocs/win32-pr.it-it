---
title: Bor (SM5-ASM)
description: Confronto a precisione doppia a livello di componente maggiore di o uguale a.
ms.assetid: 2E769077-E861-4EFA-817F-7D1AE998746C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508354affbabe1ebab70be31ab45f0e7f80d0765
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046068"
---
# <a name="dge-sm5---asm"></a>Bor (SM5-ASM)

Confronto a precisione doppia a livello di componente maggiore di o uguale a.



| Bor \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | Componenti da confrontare con *src1*.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | Componenti da confrontare con *src0*.<br/>                |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue il confronto a virgola mobile a precisione doppia (*src0*  >=  *src1*) per ogni componente e scrive il risultato in *dest*.

Se il confronto è true, viene restituito 0xFFFFFFFF a 32 bit per quel componente. In caso contrario, viene restituito 0x00000000 a 32 bit.

Il confronto con NaN restituisce false.

Le maschere *dest* valide sono uno o due componenti. Ovvero:. x,. y,. z,. w,. XY,. xz,. XW,. YZ,. YW,. ZW il primo componente *dest* nella maschera riceve il risultato 32 bit per il primo doppio confronto. Il secondo componente della maschera, se presente, riceve il risultato di 32 bit per il secondo confronto doppio.

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

 

 





