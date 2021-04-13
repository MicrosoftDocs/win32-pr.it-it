---
title: dcl_sampler (SM4-ASM)
description: '\_campionatore DCL (SM4-ASM)'
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104399823"
---
# <a name="dcl_sampler-sm4---asm"></a>\_campionatore DCL (SM4-ASM)

Dichiara un registro del campionatore.



| \_sn campionatore DCL, modalità |
|-----------------------|



 



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
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em><br/></td>
<td>in Un registro campionatore, dove <em>N</em> è un numero intero che indica il numero di registro.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>modalità</em><br/></td>
<td>in Modalità campionatore, che vincola gli Stati del campionatore (elencati nei membri di <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) rispettati. Le modalità e gli Stati sono elencati nella tabella seguente.<br/> 
<table>
<thead>
<tr class="header">
<th>Modalità</th>
<th>Stati campionatore rispettati</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>default</td>
<td><em>Filter</em> (non può usare i valori _COMPARISON o _TEXT), <em>Addresse/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="even">
<td>confronto</td>
<td><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressList/V/W</em>, <em>MinLOD, MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="odd">
<td>mono</td>
<td><em>Filter</em> (deve essere uno dei valori _TEXT), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (questi due Stati sono lo stato globale del dispositivo), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

La modalità limita le istruzioni di esempio che è possibile utilizzare. Questa tabella elenca i metodi dell'oggetto texture supportati per ogni modalità.



| Campionatore che opera in questa modalità | Può usare questi metodi di Texture-Object                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| default                          | [Esempio](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| confronto                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| mono                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x\*          |



 

\* -L'uso di un campionatore in modalità mono è supportato solo in un pixel shader.

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_sampler s3, default
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

 

