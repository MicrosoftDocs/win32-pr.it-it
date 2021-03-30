---
title: o (SM4-ASM)
description: OR bit per bit.
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993152"
---
# <a name="or-sm4---asm"></a>o (SM4-ASM)

OR bit per bit.



| o dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nel \] risultato dell'operazione.<br/>      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti a o con *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] componenti a o con *src0*.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un'operazione logica di componente o di ogni coppia di valori a 32 bit da *src0* e *src1*. I risultati a 32 bit vengono posizionati in *dest*.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





