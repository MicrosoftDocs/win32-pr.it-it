---
title: umad (sm4 - asm)
description: Numero intero senza segno moltiplicato e sommato.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6a6c649a61c78eebee249b9fec5c032a07a8a0761a3d23d6e45da573be122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405991"
---
# <a name="umad-sm4---asm"></a>umad (sm4 - asm)

Numero intero senza segno moltiplicato e sommato.



| umad dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle, \] src2 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valore da moltiplicare per *src1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Valore da moltiplicare per *src1*.<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Valore da aggiungere al prodotto di *src0* e *src1*.<br/> |



 

## <a name="remarks"></a>Commenti

Umul [](umul--sm4---asm-.md) a livello di componente degli operandi a 32 bit *src0* e *src1* senza segno, mantenendo i 32 bit bassi, per componente, del risultato. Questa istruzione esegue quindi un [iadd](iadd--sm4---asm-.md) di *src2,* producendo il risultato corretto basso a 32 bit (per componente). I risultati a 32 bit vengono inseriti in *dest*.

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

 

 





