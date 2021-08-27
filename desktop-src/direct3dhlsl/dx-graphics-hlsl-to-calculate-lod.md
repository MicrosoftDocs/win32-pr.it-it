---
title: CalculateLevelOfDetail (oggetto trama DirectX HLSL)
description: Calcola il livello di dettaglio.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 44d71469cf5fd3246a0bb038cf369227cb3a3017
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625827"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a>CalculateLevelOfDetail (oggetto trama DirectX HLSL)

Calcola il livello di dettaglio.

ret Object.CalculateLevelOfDetail( sampler \_ state S, float x );



 

## <a name="parameters"></a>Parametri



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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em><br/></td>
<td>Qualsiasi <a href="dx-graphics-hlsl-to-type.md">tipo di oggetto</a> trama (ad eccezione di Texture2DMS e Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>[in] Stato <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">del campionatore.</a> Si tratta di un oggetto dichiarato in un file di effetti che contiene assegnazioni di stato.<br/></td>
</tr>
<tr class="odd">
<td><span id="x"></span><span id="X"></span><em>X</em><br/></td>
<td>[in] Valore o valori di interpolazione lineare, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusi. Il numero di componenti dipende dal tipo texture-object. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object tipo</th>
<th>Tipo di parametro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float1</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valore restituito

Restituisce il lod calcolato, un singolo valore a virgola mobile.

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | x         |          |           |



 

1.  TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.
2.  Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

