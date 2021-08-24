---
title: ishl (sm5 - asm)
description: Maiusc a sinistra. | ishl (sm5 - asm)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6908d12824c5aa84e04db38fb2462031bb2ae4a198700f98938456ecbd8619a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854211"
---
# <a name="ishl-sm5---asm"></a>ishl (sm5 - asm)

Maiusc a sinistra.



| ishl dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|--------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Contiene i risultati dello spostamento.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valori a 32 bit da spostare.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Numero di bit da spostare.<br/>        |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue uno spostamento a livello di componente di ogni valore a 32 bit in *src0* lasciato da un conteggio di bit intero senza segno fornito dai 5 bit LSB (intervallo 0-31) in *src1,* inserendo 0. I risultati a 32 bit per componente vengono inseriti in *dest*.

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

 

 





