---
title: imin (sm4 - asm)
description: Numero intero minimo per componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0188b23700393034ad2187636d8d5bf846b8b8523b5336699443475c094fd26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982391"
---
# <a name="imin-sm4---asm"></a>imin (sm4 - asm)

Numero intero minimo per componente.



| imin dest \[ \] .mask, \[  - \] src0 \[ .swizzle, \] \[ - \] src1 \[ .swizzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Risultato dell'operazione.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valore da confrontare con *src1*.<br/>                                                       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Valore da confrontare con *src0*.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Il modificatore di negazione facoltativo sugli operandi di origine accetta il complemento 2 prima di eseguire l'operazione.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





