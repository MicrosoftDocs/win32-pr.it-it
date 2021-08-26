---
title: udiv (sm4 - asm)
description: Divisione di interi senza segno.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b1320d0518034129efe2222a42aa2694df0422db524da0714377cb43a2b9a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948981"
---
# <a name="udiv-sm4---asm"></a>udiv (sm4 - asm)

Divisione di interi senza segno.



| udiv destQUOT \[ .mask \] , destREM \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|------------------------------------------------------------------------------|



 



| Elemento                                                                                                   | Descrizione                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[in \] Indirizzo del quoziente risultante.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[in \] Indirizzo del resto risultante.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[in \] I componenti da dividere per *src1*.<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                        | \[in \] The components by whch to divide *src0*.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue una divisione senza segno a livello di componente dell'operando a 32 bit *src0* per l'operando a 32 bit *src1*. I risultati delle divisioni sono i quozienti a 32 bit inseriti in *destQUOT* e i resto a 32 bit inseriti in *destREM*.

La divisione per zero restituisce 0xffffffff per il quoziente e il resto.

È possibile specificare *destQUOT* o *destREM* come NULL anziché specificare un registro, se il quoziente o il resto non sono necessari.

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

 

 





