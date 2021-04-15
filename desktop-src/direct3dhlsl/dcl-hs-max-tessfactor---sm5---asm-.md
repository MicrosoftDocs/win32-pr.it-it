---
title: dcl_hs_max_tessfactor (SM5-ASM)
description: Dichiarare il maxTessFactor per la patch.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993245"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a>\_ \_ Max \_ tessfactor di DCL HS (SM5-ASM)

Dichiarare il maxTessFactor per la patch.



| \_tessfactor max di DCL HS \_ \_ n |
|----------------------------|



 



| Elemento                                                   | Descrizione                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="n"></span><span id="N"></span>*n*<br/> | \[in \] maxTessFactor.<br/> |



 

## <a name="remarks"></a>Commenti

MaxTessFactor è un valore float32 compreso nell'intervallo {1,0... 64,0}.

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

 

 





