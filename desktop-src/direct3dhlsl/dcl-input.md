---
title: dcl_input (SM4-ASM)
description: '\_input DCL (SM4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993229"
---
# <a name="dcl_input-sm4---asm"></a>\_input DCL (SM4-ASM)

Dichiara un registro di input shader.



| \_input DCL v *N \[ . mask \] \[ , interpolationMode \]* |
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
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. mask]</em><br/></td>
<td>in Registro dei dati dei vertici. <br/>
<ul>
<li><em>N</em> è un intero che identifica il numero di registro.</li>
<li><em>[. mask]</em> è una maschera di componenti facoltativa (con estensione xyzw) che specifica quale dei componenti del registro utilizzare.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br/></td>
<td>[in] Facoltativo. La modalità di interpolazione, che viene rispettata solo nei registri di input pixel shader. Può essere uno dei valori seguenti: <br/>
<ul>
<li>Constant: non esegue l'interpolazione tra valori di registro.</li>
<li>lineare: esegue l'interpolazione lineare tra i valori di registro.</li>
<li>linearCentroid: uguale a lineare, ma al centro quando viene premuto il multicampionamento.</li>
<li>linearNoperspective: uguale a lineare, ma senza correzione della prospettiva.</li>
<li>linearNoperspectiveCentroid: uguale a lineare, al centro quando si verifica il multicampionamento, senza correzione della prospettiva.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a>Note di interpolazione

Per impostazione predefinita, gli attributi dei vertici vengono interpolati da un pixel Center quando si esegue l'anti-aliasing multicampionamento. Se non viene analizzato un pixel Center, un attributo viene estrapolato in un centro pixel prima dell'interpolazione.

Per un pixel non completamente coperto o un attributo che non copre un pixel Center, è possibile specificare il campionamento del baricentro che forza il campionamento in un punto qualsiasi all'interno dell'area coperta del pixel. Poiché una maschera di esempio (se utilizzata) viene applicata prima che il baricentro venga calcolato, qualsiasi percorso di esempio mascherato dalla maschera di esempio non può essere scelto come posizione del centro.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Per identificare l'input come valore di sistema, usare [l' \_ input DCL \_ SV (SM4-ASM)](dcl-input-sv.md).

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
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

 

 





