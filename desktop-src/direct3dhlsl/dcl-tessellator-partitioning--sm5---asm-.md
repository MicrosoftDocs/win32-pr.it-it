---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Dichiarare il partizionamento mosaico in una sezione di dichiarazione Hull shader.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398294"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>\_ \_ partizionamento mosaico DCL (SM5-ASM)

Dichiarare il partizionamento mosaico in una sezione di dichiarazione Hull shader.



| \_partizionamento di mosaico di DCL \_ {Integer di partizionamento \_ \| partizionamento \_ pow2 \|suddivisione \_ frazionaria \_ dispari \| partizionamento \_ frazionario \_ pari} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Descrizione                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partizionamento di partizionamento Integer partizionamento del partizionamento del partizionamento \_ \| \_ pow2 \| \_ \_ \| \_ frazionario pari \_*<br/> | \[nel \] partizionamento mosaico.<br/> |



 

## <a name="remarks"></a>Commenti

Dal punto di vista dell'hardware, \_ pow2 si comporta esattamente come \_ Integer. Spetta all'autore dello shader HLSL e/o compilercode a arrotondare TessFactors a potenze di 2.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull                 | Dominio | Geometria | Pixel | Calcolo |
|--------|----------------------|--------|----------|-------|---------|
|        | Sezione delle dichiarazioni |        |          |       |         |



 

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

 

 





