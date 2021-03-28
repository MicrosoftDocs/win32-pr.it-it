---
title: dcl_constantBuffer (SM4-ASM)
description: '\_constantBuffer DCL (SM4-ASM)'
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117209"
---
# <a name="dcl_constantbuffer-sm4---asm"></a>\_constantBuffer DCL (SM4-ASM)

Dichiara un buffer costante dello shader.



| \_ *\[ dimensioni \] cbN* constantBuffer di DCL, *AccessPattern* |
|----------------------------------------------------|



 



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
<td><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [dimensioni]</em><br/></td>
<td>in Buffer costante dello shader dove N è un numero intero che denota il numero di registro constant-buffer e size è un numero intero che indica il numero di elementi nel buffer.<br/></td>
</tr>
<tr class="even">
<td><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em><br/></td>
<td>in Il modo in cui il buffer sarà accessibile dal codice dello shader, che è uno dei seguenti: <br/> 
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



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Questo esempio dichiara un buffer costante per Register CB0, che include 19 elementi. Questi elementi sono accessibili con un indice letterale.


```
dcl_constantbuffer  cb0[19], immediateIndexed
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

 

 





