---
title: IMAX (SM4-ASM)
description: Numero intero a livello di componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc1bc6311573b1e7b39fbeaa93904203e7aae2ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117181"
---
# <a name="imax-sm4---asm"></a>IMAX (SM4-ASM)

Numero intero a livello di componente.



| dest \[ . mask IMAX \] , \[  - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nel \] risultato dell'operazione.<br/> *dest*  =  *src0*  >  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] valore da confrontare con *src1*.<br/>                                                       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nel \] valore da confrontare con *src0*.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Il modificatore negazioni facoltativo negli operandi di origine richiede il complemento di 2 prima di eseguire l'operazione.

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

 

 





