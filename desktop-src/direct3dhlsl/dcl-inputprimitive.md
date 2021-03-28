---
title: dcl_inputPrimitive (SM4-ASM)
description: '\_inputPrimitive DCL (SM4-ASM)'
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 76c131b7c4225c0b30ad1183e4da1fe6c0561754
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956085"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>\_inputPrimitive DCL (SM4-ASM)

Dichiara il tipo primitivo per gli input dello shader di geometria.



| \_ *tipo* di inputPrimitive DCL |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="type"></span><span id="TYPE"></span><em>tipo</em><br/></td>
<td>in Input: tipo primitivo di dati, che è uno dei seguenti: <br/>
<ul>
<li><em>punto</em> - di Elenco punti</li>
<li><em>riga</em> - di elenco linee</li>
<li><em>triangolo</em> - elenco di triangolo</li>
<li><em>line_adj</em> - elenco linee con dati adiacenza</li>
<li><em>triangle_adj</em> - elenco di triangolo con dati adiacenza</li>
</ul></td>
</tr>
</tbody>
</table>



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_inputPrimitive triangle
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

 

 





