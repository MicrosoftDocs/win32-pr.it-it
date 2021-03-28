---
title: bfrev (SM5-ASM)
description: Invertire un numero a 32 bit.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993120"
---
# <a name="bfrev-sm5---asm"></a>bfrev (SM5-ASM)

Invertire un numero a 32 bit.



| bfrev dest \[ . mask \] , src0 \[ . Swizzle\] |
|---------------------------------------|



 



| Elemento                                                            | Descrizione                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo per *src0* con BITS invertito.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] numero a 32 bit da invertire.<br/>              |



 

## <a name="remarks"></a>Commenti

Se ad esempio si specifica 0x12345678., il risultato sarà 0x1e6a2c48.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





