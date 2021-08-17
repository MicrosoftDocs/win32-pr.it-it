---
title: dcl_thread_group (sm5 - asm)
description: Dichiarare le dimensioni del gruppo di thread.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5402e53e2252d8019ba553c6a8ff449200625b1469ee923f3c26234f1faa292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515479"
---
# <a name="dcl_thread_group-sm5---asm"></a>dcl \_ thread \_ group (sm5 - asm)

Dichiarare le dimensioni del gruppo di thread.



| dcl \_ thread \_ group x, y, z |
|----------------------------|



 



| Elemento                                                   | Descrizione                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Un intero a 32 bit con segno. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Un intero a 32 bit con segno. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*Z*<br/> | \[in \] Un intero a 32 bit con segno. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Commenti

x \* y z <= \* 1024

Questa dichiarazione del gruppo di thread deve essere visualizzata una sola volta in un compute shader.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





