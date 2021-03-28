---
title: dcl_indexRange (SM4-ASM)
description: '\_indexRange DCL (SM4-ASM)'
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976498"
---
# <a name="dcl_indexrange-sm4---asm"></a>\_indexRange DCL (SM4-ASM)

Dichiara un intervallo di registri a cui sarà possibile accedere dall'indice (un Integer calcolato nello shader).



| DCL \_ IndexRange *minRegisterM*, *maxRegisterN* |
|------------------------------------------------|



 



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
<td><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br/></td>
<td>in Primo registro a cui accedere in base all'indice. <br/>
<ul>
<li><em>minRegister</em> è <strong>v</strong> per un vertice o pixel shader registro di input oppure <strong>o</strong> per un registro di output del vertex shader.</li>
<li><em>M</em> è un numero intero che indica il numero di registro.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>in Ultimo registro a cui accedere in base all'indice. Lo stesso formato di <em>minRegister</em> ad eccezione di <em>N</em> è il numero di registro.<br/></td>
</tr>
</tbody>
</table>



 

A tutti i registri si applicano le restrizioni seguenti:

-   I registri min e Max devono essere dello stesso tipo e avere le stesse maschere dei componenti (se le maschere sono dichiarate).
-   Un registro può avere più intervalli di indice, purché non si sovrappongano.
-   Il numero di registro minimo deve essere minore del numero massimo di registro.
-   Un registro di indice non può contenere un [valore di sistema](dx-graphics-hlsl-semantics.md).
-   L'indicizzazione di un registro al di fuori della dichiarazione di indice max produce risultati non definiti.

I registri di input dei pixel shader devono usare la stessa modalità di interpolazione; i registri di output pixel shader non sono indicizzabili.

Un registro di input geometry shader è costituito da due dimensioni (asse del vertice, asse degli attributi); l'intervallo di indici si applica solo all'asse degli attributi perché l'asse dei vertici è sempre completamente indicizzabile.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
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

 

 





