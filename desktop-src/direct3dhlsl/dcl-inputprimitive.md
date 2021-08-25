---
title: dcl_inputPrimitive (sm4 - asm)
description: dcl \_ inputPrimitive (sm4 - asm)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0660fe4da14a20f074e4f04de8891fc0848f2597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479897"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>dcl \_ inputPrimitive (sm4 - asm)

Dichiara il tipo primitivo per gli input geometry-shader.



| dcl \_ inputPrimitive *type* |
|----------------------------|



 




| Elemento | Descrizione | 
|------|-------------|
| <span id="type"></span><span id="TYPE"></span><em>digitare</em><br /> | [in] Tipo primitivo input-data, che è uno dei seguenti: <br /><ul><li><em>point</em> - elenco di punti</li><li><em>line</em> - line list</li><li><em>triangolo</em> - elenco triangolo</li><li><em>line_adj</em> - elenco di righe con dati di adicenza</li><li><em>triangle_adj</em> - Elenco triangolo con dati di adienza</li></ul> | 




 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader nel linguaggio di assembly usando Shader Model 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_inputPrimitive triangle
```



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

 

 





