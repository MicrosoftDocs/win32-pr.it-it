---
title: CalculateLevelOfDetail (oggetto trama di DirectX HLSL)
description: Calcola il livello di dettaglio.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c59b8da97ff1cbe0bd88d6a49120a0a040cf3c30
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104976863"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a>CalculateLevelOfDetail (oggetto trama di DirectX HLSL)

Calcola il livello di dettaglio.



|                                                                 |
|-----------------------------------------------------------------|
| RET Object. CalculateLevelOfDetail (Sampler \_ state S, float x); |



 

## <a name="parameters"></a>Parametri



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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em><br/></td>
<td>Qualsiasi tipo <a href="dx-graphics-hlsl-to-type.md">di oggetto trama</a> (ad eccezione di Texture2DMS e Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>in <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Stato del campionatore</a>. Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.<br/></td>
</tr>
<tr class="odd">
<td><span id="x"></span><span id="X"></span><em>x</em><br/></td>
<td>in Valore o valori di interpolazione lineare, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusi. Il numero di componenti dipende dal tipo di oggetto trama. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo di Texture-Object</th>
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

Restituisce l'oggetto LOD calcolato, un singolo valore a virgola mobile.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | x         |          |           |



 

1.  TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.
2.  Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Texture-oggetto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

