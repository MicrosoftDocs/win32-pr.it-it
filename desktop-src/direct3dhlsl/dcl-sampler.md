---
title: dcl_sampler (sm4 - asm)
description: Campionatore dcl \_ (sm4 - asm)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e0e04558c9ca1c10f89e924605c8999a7f7346d2278850d7cd6449968fd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515540"
---
# <a name="dcl_sampler-sm4---asm"></a>Campionatore dcl \_ (sm4 - asm)

Dichiara un registro del campionatore.



| dcl \_ sampler sN, modalità |
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
<td>[in] Registro sampler, dove <em>N</em> è un numero intero che indica il numero di registro.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>Modalità</em><br/></td>
<td>[in] Modalità di campionamento, che vincola gli stati del campionatore (elencati nei membri <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>di D3D10_SAMPLER_DESC</strong></a>) vengono rispettati. Le modalità e gli stati sono elencati nella tabella seguente.<br/> 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>Stati del campionatore rispettati</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>default</td>
<td><em>Filtro</em> (non può usare i valori _COMPARISON o _TEXT), <em>AddressU/V/W,</em> <em>MinLOD/MaxLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy,</em> <em>BorderColor[4]</em></td>
</tr>
<tr class="even">
<td>confronto</td>
<td><em>Filter,</em> <em>ComparisonFunction,</em> <em>AddressU/V/W,</em> <em>MinLOD,MaxLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy,</em> <em>BorderColor[4]</em></td>
</tr>
<tr class="odd">
<td>Mono</td>
<td><em>Filter</em> (deve essere uno dei valori _TEXT), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (questi due stati sono global device state), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

La modalità limita le istruzioni di esempio che è possibile usare. In questa tabella sono elencati i metodi dell'oggetto trama supportati per ogni modalità.



| Un campionatore che opera in questa modalità | È possibile usare questi Texture-Object seguenti                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| default                          | [Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| confronto                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| Mono                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x\*          |



 

\* - L'uso di un campionatore in modalità mono è supportato solo in un pixel shader.

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. Non è possibile creare uno shader in linguaggio assembly usando il modello shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_sampler s3, default
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

 

