---
title: udiv (SM4-ASM)
description: Divisione di interi senza segno.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398240"
---
# <a name="udiv-sm4---asm"></a>udiv (SM4-ASM)

Divisione di interi senza segno.



| udiv destQUOT \[ . mask \] , destREM \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|------------------------------------------------------------------------------|



 



| Elemento                                                                                                   | Descrizione                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[nell' \] indirizzo del quoziente risultante.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[nell' \] indirizzo del resto risultante.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[nei \] componenti da dividere per *src1*.<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                        | \[nei \] componenti di serve per dividere *src0*.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue una divisione senza segno a livello di componente dell'operando a 32 bit *src0* dall'operando *src1* a 32 bit. I risultati delle divisioni sono i quozienti a 32 bit posizionati in *destQUOT* e i restanti 32 bit posizionati in *destREM*.

Divide per zero restituisce 0xFFFFFFFF per quoziente e resto.

È possibile specificare *destQUOT* o *destREM* come null anziché specificare un registro, se il quoziente o il resto non sono necessari.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





