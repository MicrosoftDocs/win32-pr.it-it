---
title: ieq (sm4 - asm)
description: Confronto di uguaglianza di numeri interi vettoriali a livello di componente.
ms.assetid: AD010554-80DC-4D2D-B04C-2638276DDC34
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942e45bedd6dd7e920d4c625a4c001d48f6650a47d74e1643eb162c87980de2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743661"
---
# <a name="ieq-sm4---asm"></a>ieq (sm4 - asm)

Confronto di uguaglianza di numeri interi vettoriali a livello di componente.



| dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|---------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valore da confrontare con *src1*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Valore da confrontare con *src0*.<br/>           |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue il confronto di interi (*src0*  ==  *src1*) per ogni componente e scrive il risultato in *dest*.

Se il confronto è true, viene restituito 0xFFFFFFFF per tale componente. In caso 0x0000000 viene restituito

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

 

 





