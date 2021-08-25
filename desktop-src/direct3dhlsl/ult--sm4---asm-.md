---
title: ult (sm4 - asm)
description: Confronto tra integer senza segno e vettore a livello di componente.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92fca937a083d4dc454b19549710790e186fc4b57a8ea7aa4a904fc85fb5378
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742351"
---
# <a name="ult-sm4---asm"></a>ult (sm4 - asm)

Confronto tra integer senza segno e vettore a livello di componente.



| ult dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valore da confrontare con *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Valore da confrontare con *src1*.<br/>             |



 

## <a name="remarks"></a>Commenti

Esegue il confronto di interi senza segno (*src0*  <  *src1*) per ogni componente e scrive il risultato *in dest*.

Se il confronto è true, questa istruzione restituisce 0xFFFFFFFF per tale componente. In caso contrario, restituisce 0x0000000.

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

 

 





