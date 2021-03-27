---
title: countbits (SM5-ASM)
description: Conta il numero di bit impostati in un numero.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857774"
---
# <a name="countbits-sm5---asm"></a>countbits (SM5-ASM)

Conta il numero di bit impostati in un numero.



| countbits dest \[ . mask \] , src0 \[ . Swizzle\] |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei risultati.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] numero di input a 32 bit.<br/>    |



 

## <a name="remarks"></a>Commenti

Questa istruzione può essere utilizzata per calcolare la percentuale di code coverage input di shader.

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

 

 





