---
title: mov (sm4 - asm)
description: Spostamento per componente. | mov (sm4 - asm)
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247e3838841d63c3cadf2e075fd088b534bf56ea19b8869b7cffe91e9f75e6c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095371"
---
# <a name="mov-sm4---asm"></a>mov (sm4 - asm)

Spostamento per componente.



| Istruzione: mov \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|-------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> *dest*  =  *src0*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti da spostare.<br/>                                                |



 

## <a name="remarks"></a>Commenti

I modificatori, diversi da swizzle, presuppongono che i dati siano a virgola mobile. L'assenza di modificatori sposta semplicemente i dati senza modificare i bit.

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

 

 





