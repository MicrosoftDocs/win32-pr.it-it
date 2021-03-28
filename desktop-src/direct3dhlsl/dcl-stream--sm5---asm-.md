---
title: dcl_stream (SM5-ASM)
description: Dichiarare un flusso di output di Geometry shader.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398297"
---
# <a name="dcl_stream-sm5---asm"></a>\_flusso DCL (SM5-ASM)

Dichiarare un flusso di output di Geometry shader.



| \_flusso DCL m\# |
|-----------------|



 



| Elemento                                                       | Descrizione                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*m\#*<br/> | \[nel \] flusso 0.. 3 (M0.. m3).<br/> |



 

## <a name="remarks"></a>Commenti

Un flusso specificato può essere dichiarato una sola volta.

Se non viene dichiarato alcun flusso, si presuppone che le dichiarazioni di topologia di output e output siano per il flusso 0.

Il primo **\_ flusso di DCL** non può comparire dopo le istruzioni di **\_ output** di DCL o di **DCL \_ outputTopology** .

Tutte le istruzioni di **\_ output** o **DCL \_ outputToplogy** di DCL dopo un'istruzione del **\_ flusso DCL** m \# definiscono gli output per il flusso m \# .

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

 

 





