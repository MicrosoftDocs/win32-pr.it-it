---
title: dcl_input_sv (SM4-ASM)
description: '\_input DCL \_ SV (SM4-ASM)'
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719486"
---
# <a name="dcl_input_sv-sm4---asm"></a>\_input DCL \_ SV (SM4-ASM)

Dichiara un registro di input shader che prevede che un valore di [sistema](dx-graphics-hlsl-semantics.md) venga fornito da una fase precedente.



| \_input DCL \_ SV v *N \[ . mask \]*, *systemValueName \[ , interpolationMode \]* |
|------------------------------------------------------------------------|



 



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
<td><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em><br/></td>
<td>in Nome del valore di sistema che è una stringa (vedere <a href="dx-graphics-hlsl-semantics.md">semantica del valore di sistema</a>) senza &quot; il &quot; prefisso SV_.<br/></td>
</tr>
<tr class="odd">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br/></td>
<td>[in] Facoltativo. La modalità di interpolazione che influiscono sulle modalità di calcolo dei valori durante la rasterizzazione; la modalità viene utilizzata solo da un pixel shader. Può essere uno dei valori seguenti: <br/>
<ul>
<li>Constant: non esegue l'interpolazione tra valori di registro.</li>
<li>lineare: esegue l'interpolazione lineare tra i valori di registro.</li>
<li>linearCentroid: uguale a lineare, ma al centro quando viene premuto il multicampionamento.</li>
<li>linearNoperspective: uguale a lineare, ma senza correzione della prospettiva.</li>
<li>linearNoperspectiveCentroid: uguale a lineare, ma senza correzione della prospettiva e centro per il multicampionamento.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Una maschera di componente per una dichiarazione di valore di sistema può essere qualsiasi subset appropriato di \[ xyzw \] ; le dichiarazioni non possono sovrapporsi (ogni dichiarazione deve seguire la sequenza xyzw). Quando si dichiarano valori di sistema scalari (ad esempio distanza di ritaglio e distanza di abbattimento), è possibile dichiarare più valori di sistema in un unico registro. In tal caso, assicurarsi che altri modificatori come le modalità di interpolazione corrispondano.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Ecco alcuni esempi:


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
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

 

 





