---
title: Ultimate (SM4-ASM)
description: Il confronto con il vettore a livello di componente Unsigned Integer meno di.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993032"
---
# <a name="ult-sm4---asm"></a>Ultimate (SM4-ASM)

Il confronto con il vettore a livello di componente Unsigned Integer meno di.



| Ultimate dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] valore da confrontare con *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nel \] valore da confrontare con *src1*.<br/>             |



 

## <a name="remarks"></a>Commenti

Esegue il confronto unsigned integer (*src0*  <  *src1*) per ogni componente e scrive il risultato in *dest*.

Se il confronto è true, questa istruzione restituisce 0xFFFFFFFF per quel componente. In caso contrario, restituisce 0x0000000.

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

 

 





