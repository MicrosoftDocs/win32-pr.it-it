---
title: dcl_indexRange (sm4 - asm)
description: dcl \_ indexRange (sm4 - asm)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a652d200a211eb5528f6e7ecdedf2cc20579817d1f0148d59855d1e864de55de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727191"
---
# <a name="dcl_indexrange-sm4---asm"></a>dcl \_ indexRange (sm4 - asm)

Dichiara un intervallo di registri a cui sarà possibile accedere in base all'indice (un numero intero calcolato nello shader).



| dcl \_ indexRange *minRegisterM*, *maxRegisterN* |
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
<td>[in] Primo registro a cui accedere in base all'indice. <br/>
<ul>
<li><em>minRegister</em> è <strong>v</strong> per un vertice o un pixel shader di input oppure <strong>o per</strong> un registro di output del vertex shader.</li>
<li><em>M</em> è un numero intero che indica il numero di registro.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>[in] Ultimo registro a cui accedere in base all'indice. Lo stesso formato di <em>minRegister, ad</em> eccezione <em>di N</em> è il numero di registro.<br/></td>
</tr>
</tbody>
</table>



 

A tutti i registri si applicano le restrizioni seguenti:

-   I registri min e max devono essere dello stesso tipo e avere le stesse maschere componenti (se le maschere sono dichiarate).
-   Un registro può avere più intervalli di indici, purché non si sovrappongano.
-   Il numero minimo di registri deve essere minore del numero massimo di registri.
-   Un registro di indice non può contenere [un valore di sistema](dx-graphics-hlsl-semantics.md).
-   L'indicizzazione di un registro all'esterno della dichiarazione max index produce risultati non definiti.

I registri di input del pixel shader devono usare la stessa modalità di interpolazione. pixel shader i registri di output non sono indicizzabili.

Un registro di input geometry shader ha due dimensioni (asse dei vertici, asse degli attributi); L'intervallo di indici si applica solo all'asse dell'attributo perché l'asse dei vertici è sempre completamente indicizzabile.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. Non è possibile creare uno shader in linguaggio assembly usando il modello shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





