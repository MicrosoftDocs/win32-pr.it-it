---
title: dcl_indexableTemp (SM4-ASM)
description: '\_indexableTemp DCL (SM4-ASM)'
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993240"
---
# <a name="dcl_indexabletemp-sm4---asm"></a>\_indexableTemp DCL (SM4-ASM)

Dichiara un registro temporaneo indicizzabile.



| \_dimensioni indexableTemp di DCL x *N \[ \] , ComponentCount* |
|-------------------------------------------------|



 



| Elemento                                                                                                                           | Descrizione                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/>                                                                         | \[in \] un Integer che indica il numero di registro.<br/>                              |
| <span id="_size_"></span><span id="_SIZE_"></span>*\[dimensioni\]*<br/>                                                        | \[in \] un valore integer facoltativo. Numero di elementi nella matrice di registro.<br/>  |
| <span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*<br/> | \[in \] un valore integer facoltativo. Numero di componenti nella matrice di registro.<br/> |



 

Un registro contiene spazio sufficiente per un valore a quattro componenti a 32 bit. il numero di elementi nella matrice di registri temporanei (indicizzabile e [non indicizzabile](dcl-temps.md)) non può essere maggiore di 4096.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi del codice generato per i registri indicizzabili.


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
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

 

 





