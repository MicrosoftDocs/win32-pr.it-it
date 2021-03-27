---
title: Martina (SM4-ASM)
description: Integer senza segno, moltiplicazione e aggiunta.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719393"
---
# <a name="umad-sm4---asm"></a>Martina (SM4-ASM)

Integer senza segno, moltiplicazione e aggiunta.



| Martina dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] valore da moltiplicare per *src1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nel \] valore da moltiplicare per *src1*.<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[nel \] valore da aggiungere al prodotto di *src0* e *src1*.<br/> |



 

## <a name="remarks"></a>Commenti

[Umul](umul--sm4---asm-.md) di elementi a 32 bit *src0* e *src1* senza segno, mantenendo i 32 bit bassi, per componente, del risultato. Questa istruzione esegue quindi un [IAdd](iadd--sm4---asm-.md) di *src2*, producendo il risultato corretto a 32 bit (per componente). I risultati a 32 bit vengono posizionati in *dest*.

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

 

 





