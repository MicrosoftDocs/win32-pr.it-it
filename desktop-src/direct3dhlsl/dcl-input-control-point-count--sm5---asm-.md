---
title: dcl_input_control_point_count (SM5-ASM)
description: Dichiarare il numero di punti di controllo di input di Hull shader nella sezione relativa alla dichiarazione di Hull shader.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398306"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>\_ \_ \_ conteggio punti di controllo input DCL \_ (SM5-ASM)

Dichiarare il numero di punti di controllo di input di Hull shader nella sezione relativa alla dichiarazione di Hull shader.



| \_ \_ conteggio punti di controllo input DCL \_ \_ {1.32} |
|-------------------------------------------|



 



| Elemento                                                   | Descrizione                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[nel \] conteggio dei punti di controllo di input.<br/> |



 

## <a name="remarks"></a>Commenti

È necessario almeno un punto di controllo di input. Se non è necessario, può essere vuoto.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

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

 

 





