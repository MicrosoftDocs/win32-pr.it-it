---
title: imul (sm4 - asm)
description: Numero intero con segno moltiplicato.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87eabcc07dc5c6a662494c71a26c5f60e5fa1053265e3740ad3605ed685771a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986491"
---
# <a name="imul-sm4---asm"></a>imul (sm4 - asm)

Numero intero con segno moltiplicato.



| imul destHI \[ \] .mask, destLO \[ \] .mask, \[ - \] src0 \[ .swizzle, \] \[ - \] src1 \[ .swizzle\] |
|-------------------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[in \] Indirizzo dei 32 bit alti del risultato.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[in \] Indirizzo dei 32 bit bassi del risultato.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[in \] Valore da moltiplicare con *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[in \] Valore da moltiplicare con *src0*.<br/>             |



 

## <a name="remarks"></a>Commenti

Moltiplicazione per componente di operandi a 32 bit *src0* e *src1* (entrambi con segno), producendo il risultato completo a 64 bit (per componente) corretto. I 32 bit bassi (per componente) vengono inseriti in *destLO*. I 32 bit alti (per componente) vengono inseriti in *destHI*.

È *possibile specificare destHI* o *destLO* come NULL invece di specificare un registro, se i 32 bit alti o bassi del risultato a 64 bit non sono necessari.

Il modificatore di negazione facoltativo sugli operandi di origine accetta il complemento 2 prima di eseguire un'operazione aritmetica.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





