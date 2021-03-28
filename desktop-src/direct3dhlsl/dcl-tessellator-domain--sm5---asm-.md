---
title: dcl_tessellator_domain (SM5-ASM)
description: Dichiarare il dominio mosaico in una sezione di dichiarazione Hull shader e il Domain shader.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398295"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>\_dominio mosaico \_ di DCL (SM5-ASM)

Dichiarare il dominio mosaico in una sezione di dichiarazione Hull shader e il Domain shader.



| DCL \_ mosaico \_ dominio {dominio \_ oline \| dominio \_ Tri \| Quad del dominio \_ } |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                | Descrizione                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*dominio di dominio di dominio \_ \| \_ Tri \| Domain \_ quad*<br/> | \[nel \] dominio.<br/> |



 

## <a name="remarks"></a>Commenti

Il comportamento non è definito se Hull shader e Domain shader forniscono domini non corrispondenti o altri decalarations in conflitto.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull                 | Dominio | Geometria | Pixel | Calcolo |
|--------|----------------------|--------|----------|-------|---------|
|        | Sezione delle dichiarazioni | X      |          |       |         |



 

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

 

 





