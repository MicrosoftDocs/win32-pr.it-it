---
title: dcl_input (sm4 - asm)
description: Input dcl \_ (sm4 - asm)
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3242c2f1e753407d239057fdc4af0a6f04d6d83a66e2a22ffb1be929583c21c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986741"
---
# <a name="dcl_input-sm4---asm"></a>Input dcl \_ (sm4 - asm)

Dichiara un registro di input shader.



| dcl \_ input v N *\[ .mask , \] \[ interpolationMode \]* |
|-------------------------------------------------|



 



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
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em><br/></td>
<td>[in] Registro dei dati dei vertici. <br/>
<ul>
<li><em>N</em> è un numero intero che identifica il numero di registro.</li>
<li><em>[.mask]</em> è una maschera componente facoltativa (.xyzw) che specifica quale dei componenti del registro usare.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolazioneMode</em><br/></td>
<td>[in] Facoltativo. Modalità di interpolazione, che viene rispettata solo pixel shader di input. Può essere uno dei valori seguenti: <br/>
<ul>
<li>constant: non eseguire l'interpolazione tra i valori del registro.</li>
<li>linear : interpolazione lineare tra i valori del registro.</li>
<li>linearCentroid: uguale a lineare ma a centroide con blocco durante il multicampionamento.</li>
<li>linearNoperspective: uguale a lineare ma senza correzione prospettica.</li>
<li>linearNoperspectiveCentroid: come lineare, con chiusura al centro durante il multicampionamento, senza correzione della prospettiva.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a>Note sull'interpolazione

Per impostazione predefinita, gli attributi dei vertici vengono interpolati da un centro pixel quando si esegue l'antialiasing multicampione. Se un centro pixel non è coperto, un attributo viene estrapolato in un centro pixel prima dell'interpolazione.

Per un pixel non completamente coperto o un attributo che non copre un centro pixel, è possibile specificare il campionamento centroide che forza il campionamento in un punto qualsiasi all'interno dell'area coperta del pixel. Poiché una maschera di esempio (se usata) viene applicata prima del calcolo del centroid, non è possibile scegliere come posizione centrale qualsiasi posizione del campione mascherata dalla maschera di esempio.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Per identificare l'input come valore di sistema, usare [dcl \_ input \_ sv (sm4 - asm)](dcl-input-sv.md).

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader nel linguaggio di assembly usando Shader Model 4.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
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

 

 





