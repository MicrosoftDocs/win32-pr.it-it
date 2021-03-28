---
title: dcl_thread_group (SM5-ASM)
description: Dichiarare le dimensioni del gruppo di thread.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046112"
---
# <a name="dcl_thread_group-sm5---asm"></a>\_ \_ gruppo di thread DCL (SM5-ASM)

Dichiarare le dimensioni del gruppo di thread.



| \_ \_ gruppo di thread DCL x, y, z |
|----------------------------|



 



| Elemento                                                   | Descrizione                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[in \] un intero usigned a 32 bit. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[in \] un intero usigned a 32 bit. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*z*<br/> | \[in \] un intero usigned a 32 bit. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Commenti

x \* y \* z <= 1024

Questa dichiarazione del gruppo di thread deve essere visualizzata una sola volta in un compute shader.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





