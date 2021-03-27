---
title: IMUL (SM4-ASM)
description: Intero con segno Multiply.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719423"
---
# <a name="imul-sm4---asm"></a>IMUL (SM4-ASM)

Intero con segno Multiply.



| IMUL destHI \[ . mask \] , destLO \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle\] |
|-------------------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[nell' \] indirizzo dei bit 32 alti del risultato.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[nell' \] indirizzo dei bit 32 bassi del risultato.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[nel \] valore da moltiplicare per *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[nel \] valore da moltiplicare per *src0*.<br/>             |



 

## <a name="remarks"></a>Commenti

Moltiplicazione componente per gli operandi a 32 bit *src0* e *src1* (entrambi firmati), producendo il risultato corretto a 64 bit completo (per componente). I 32 bit bassi (per componente) sono posizionati in *destLO*. I 32 bit alti (per componente) sono posizionati in *destHI*.

È possibile specificare *destHI* o *destLO* come null anziché specificare un registro, se non sono necessari i bit 32 massimi o bassi del risultato 64 bit.

Il modificatore negazioni facoltativo negli operandi di origine richiede il complemento di 2 prima di eseguire un'operazione aritmetica.

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

 

 





