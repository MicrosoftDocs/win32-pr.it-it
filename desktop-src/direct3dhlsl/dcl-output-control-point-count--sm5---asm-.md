---
title: dcl_output_control_point_count (SM5-ASM)
description: Dichiara il conteggio dei punti di controllo dell'output di Hull shader.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046124"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>\_ \_ \_ conteggio punti di controllo output DCL \_ (SM5-ASM)

Dichiara il conteggio dei punti di controllo dell'output di Hull shader.



| \_ \_ conteggio punti di controllo output DCL \_ \_ N |
|--------------------------------------|



 



| Elemento                                                   | Descrizione                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[in \] un valore intero compreso tra 0 e 32 che specifica il conteggio dei punti di controllo di output.<br/> |



 

## <a name="remarks"></a>Commenti

Se non sono necessari, Hull shader può restituire 0 punti di controllo.

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

 

 





