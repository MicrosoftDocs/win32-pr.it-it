---
title: emitThenCut_stream (SM5-ASM)
description: Equivale a un comando Emit seguito da un comando Cut. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981210"
---
# <a name="emitthencut_stream-sm5---asm"></a>\_flusso emitThenCut (SM5-ASM)

Equivale a un comando [Emit](emit--sm4---asm-.md) seguito da un comando [Cut](cut--sm4---asm-.md) .



| \_flusso EmitThenCut streamIndex |
|---------------------------------|



 



| Elemento                                                                                                               | Descrizione                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[nell' \] indice del flusso.<br/> |



 

## <a name="remarks"></a>Commenti

Questa operazione è utile in caso di output noto dell'ultimo vertice di una topologia.

Se i flussi non sono stati dichiarati, è necessario usare [emitThenCut](emitthencut--sm4---asm-.md) anziché **emitThenCut \_ Stream**.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





