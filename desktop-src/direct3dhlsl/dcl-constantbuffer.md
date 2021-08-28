---
title: dcl_constantBuffer (sm4 - asm)
description: dcl \_ constantBuffer (sm4 - asm)
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0913e3ee84271b2f09681826513337d45a3e5c70
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626877"
---
# <a name="dcl_constantbuffer-sm4---asm"></a>dcl \_ constantBuffer (sm4 - asm)

Dichiara un buffer costante shader.



| dcl \_ constantBuffer *cbN \[ size \]*, *AccessPattern* |
|----------------------------------------------------|



 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N[size]</em><br/></td>
<td>[in] Buffer costante shader in cui N è un numero intero che indica il numero del registro constant-buffer e size è un numero intero che indica il numero di elementi nel buffer.<br/></td>
</tr>
<tr class="even">
<td><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em><br/></td>
<td>[in] Il modo in cui il buffer sarà accessibile dal codice shader, che è uno dei seguenti: <br/> 
<table>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>immediateIndexed</td>
<td>Indicizzare il buffer con un valore letterale.</td>
</tr>
<tr class="even">
<td>dynamic_indexed</td>
<td>Indicizzare il buffer con il risultato di un'espressione valutata.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader nel linguaggio di assembly usando Shader Model 4.

## <a name="example"></a>Esempio

In questo esempio viene dichiarato un buffer costante per il registro cb0, che include 19 elementi. Questi elementi sono accessibili con un indice letterale.


```
dcl_constantbuffer  cb0[19], immediateIndexed
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

 

 





