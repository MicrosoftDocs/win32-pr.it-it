---
title: umul (sm4 - asm)
description: Numero intero senza segno moltiplicato.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec63b3a95ffbdf1f71142c9fc508e21e718b44d988b725dad5d73775746871c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721835"
---
# <a name="umul-sm4---asm"></a>umul (sm4 - asm)

Numero intero senza segno moltiplicato.



| umul destHI \[ \] .mask, destLO \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[in \] I 32 bit alti del risultato, per componente.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[in \] I 32 bit bassi del risultato, per componente.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[in \] Componenti per cui moltiplicare *src1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[in \] Componenti per cui moltiplicare *src0*.<br/>    |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue una moltiplicazione per componente degli operandi a 32 bit senza segno *src0* e *src1,* producendo il risultato completo a 64 bit corretto per componente. I 32 bit bassi per componente vengono inseriti in *destLO*. I 32 bit alti per componente vengono inseriti in *destHI*.

È possibile specificare *destHI* o *destLO* come NULL invece di specificare un registro se i 32 bit alti o bassi del risultato a 64 bit non sono necessari.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

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

 

 





