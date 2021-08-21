---
title: deq (sm5 - asm)
description: Confronto di uguaglianza a precisione doppia a livello di componente.
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5781c0b7d757e8bf72b81da54a4d6a8fe7467a40fa2509abdf093e27eb119ddc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950551"
---
# <a name="deq-sm5---asm"></a>deq (sm5 - asm)

Confronto di uguaglianza a precisione doppia a livello di componente.



| deq \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti da confrontare con *src1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Componenti da confrontare con *src0*.<br/>         |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue il confronto a virgola mobile e precisione doppia (*src0*  ==  *src1*) per ogni componente e scrive il risultato in *dest*.

Se il confronto è true, viene restituito un 0xFFFFFFFF a 32 bit per tale componente. In caso contrario, viene restituito 0x00000000 a 32 bit.

Il confronto con NaN restituisce false.

Le maschere *dest* valide sono uno o due componenti. Ad esempio: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw Il primo componente *dest* nella maschera riceve il risultato a 32 bit per il primo confronto double. Il secondo componente della maschera, se presente, riceve il risultato a 32 bit per il secondo confronto double.

Gli swizzle validi per i parametri di origine sono .xyzw, .xyxy, .zwxy, .zwzw. I mapping *src* seguenti sono post-swizzle:

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

 

 





