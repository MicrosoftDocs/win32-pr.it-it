---
title: dcl_output (SM4-ASM)
description: '\_output di DCL (SM4-ASM)'
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4391a30e172ef28133b8fe09a99bae7f77c971af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976490"
---
# <a name="dcl_output-sm4---asm"></a>\_output di DCL (SM4-ASM)

Dichiara un registro di output shader.



| output di DCL \_ o *N \[ . \] mask* |
|---------------------------|



 



| Elemento                                                                           | Descrizione                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/> | \[in \] un registro dei dati di output; *N* è un numero intero che indica il numero di registro.<br/>               |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[. mask\]*<br/>     | \[in \] facoltativo. Maschera di componenti (con estensione xyzw) che specifica quale dei componenti del registro utilizzare.<br/> |



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi.


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
```



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

 

 





