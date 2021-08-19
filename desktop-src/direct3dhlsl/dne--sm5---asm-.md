---
title: dne (sm5 - asm)
description: Confronto tra precisione doppia e componente e non confronto di uguaglianza.
ms.assetid: 7C69A86D-0820-4640-AF5A-2993EC77D2AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b86ea21aa55b3d9f13f414fb5c386c9719eee65bdd62aaea47fa38190a2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986581"
---
# <a name="dne-sm5---asm"></a>dne (sm5 - asm)

Confronto tra precisione doppia e componente e non confronto di uguaglianza.



| dne \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti da confrontare con *src1*.<br/>      |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Componenti da confrontare con *src0*.<br/>      |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue il confronto a virgola mobile e precisione doppia (*src0* != *src1*) per ogni componente e scrive il risultato in *dest*.

Se il confronto è true, viene restituito un 0xFFFFFFFF a 32 bit per tale componente. In caso contrario, viene restituito 0x00000000 a 32 bit.

Il confronto con NaN restituisce true.

Le maschere *dest* valide sono uno o due componenti. Ad esempio: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw Il primo componente *dest* nella maschera riceve il risultato a 32 bit per il primo confronto doppio. Il secondo componente nella maschera, se presente, riceve il risultato a 32 bit per il secondo confronto doppio.

Gli swizzle validi per i parametri di origine sono xyzw, xyxy, zwxy, zwzw. I mapping *src* seguenti sono post-swizzle:

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

 

 





