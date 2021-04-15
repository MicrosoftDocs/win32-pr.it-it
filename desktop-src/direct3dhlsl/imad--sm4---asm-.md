---
title: imad (SM4-ASM)
description: Intero con segno Multiply e Add.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992984"
---
# <a name="imad-sm4---asm"></a>imad (SM4-ASM)

Intero con segno Multiply e Add.



| imad dest \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle \] , \[ - \] src2 \[ . Swizzle |
|---------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nel \] risultato dell'operazione.<br/>                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] value per moltiplicare con *src1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] value per moltiplicare con *src0*.<br/>                    |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] valore da aggiungere al prodotto di *src0* e *src1*.<br/> |



 

## <a name="remarks"></a>Commenti

[IMUL](imul--sm4---asm-.md) a livello di componente degli operandi a 32 bit *src0* e *src1* (con segno), mantenendo i 32 bit (per componente) del risultato, seguiti da un [IAdd](iadd--sm4---asm-.md) di *src2*, producendo il risultato corretto a 32 bit (per componente). I risultati a 32 bit vengono posizionati in *dest*.

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

 

 





