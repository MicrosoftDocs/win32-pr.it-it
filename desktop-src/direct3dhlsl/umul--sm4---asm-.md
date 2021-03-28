---
title: umul (SM4-ASM)
description: Integer senza segno moltiplicato.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398238"
---
# <a name="umul-sm4---asm"></a>umul (SM4-ASM)

Integer senza segno moltiplicato.



| umul destHI \[ . mask \] , destLO \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[nei \] bit 32 alti del risultato, per componente.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[nei \] 32 bit bassi del risultato, per componente.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[nei \] componenti in base ai quali moltiplicare *src1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[nei \] componenti in base ai quali moltiplicare *src0*.<br/>    |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue una moltiplicazione per componente degli operandi senza segno a 32 bit *src0* e *src1*, producendo il risultato corretto a 64 bit completo per ogni componente. I 32 bit inferiori per ogni componente sono posizionati in *destLO*. I 32 bit alti per componente sono posizionati in *destHI*.

È possibile specificare *destHI* o *destLO* come null invece di specificare un registro se non sono necessari i bit 32 massimi o bassi del risultato 64 bit.

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

 

 





