---
title: Modello Shader 4
description: Shader Model 4 è un superset delle funzionalità del modello Shader 3, ad eccezione del fatto che Shader Model 4 non supporta le funzionalità del modello shader 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398486"
---
# <a name="shader-model-4"></a>Modello Shader 4

Shader Model 4 è un superset delle funzionalità del [Modello Shader 3](dx-graphics-hlsl-sm3.md), ad eccezione del fatto che Shader Model 4 non supporta le funzionalità del modello shader 1. È stato progettato usando un core di shader comune che fornisce un set comune di funzionalità a tutti gli shader programmabili, che possono essere programmati solo usando HLSL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Caratteristica</th>
<th>Funzionalità</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Set di istruzioni</td>
<td><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funzioni HLSL</strong></a></td>
</tr>
<tr class="even">
<td>Registra set</td>
<td>Il set di registri è accessibile tramite i membri nei buffer di costanti e trame usando la semantica HLSL per elementi come la compressione dei componenti.
<ul>
<li>Registri pixel shader (vedere <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">registri-ps_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">registri-ps_4_1</a>)</li>
<li>Registri vertex shader (vedere <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">registri-vs_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">registri-vs_4_1</a>)</li>
<li>Registri di Geometry shader (vedere <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">registri-gs_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">registri-gs_4_1</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vertex shader max</td>
<td>Nessuna restrizione</td>
</tr>
<tr class="even">
<td>Pixel shader max</td>
<td>Nessuna restrizione</td>
</tr>
<tr class="odd">
<td>Nuovi profili shader aggiunti</td>
<td>gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 *</td>
</tr>
<tr class="even">
<td>Nuovo profilo di Effect-Framework aggiunto</td>
<td>fx_4_0, fx_4_1 *</td>
</tr>
</tbody>
</table>



 

\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 e FX \_ 4 \_ 1 sono supportati in Direct3D 10,1 o versione successiva.

Shader Model 4 supporta una nuova fase della pipeline, ovvero la fase geometry-shader, che può essere usata per creare o modificare la geometria esistente. Include anche due nuovi tipi di oggetto: un oggetto Stream-output progettato per il flusso dei dati fuori dalla fase Geometry e un oggetto trama basato su modelli che implementa funzioni di campionamento di trama.

-   [Common shader Core](dx-graphics-hlsl-common-core.md)
-   [Costanti](dx-graphics-hlsl-constants.md)
-   [Geometry-oggetto shader](dx-graphics-hlsl-geometry-shader.md)
-   [Stream-oggetto di output](dx-graphics-hlsl-so-type.md)
-   [Texture (oggetto)](dx-graphics-hlsl-to-type.md)

Shader Model 4 supporta le regole di compressione che stabiliscono la disposizione dei dati quando vengono archiviati. Queste regole sono descritte in [regole di compressione per variabili costanti](dx-graphics-hlsl-packing-rules.md)

La sezione di [assembly Shader Model 4](dx-graphics-hlsl-sm4-asm.md) descrive le istruzioni di assembly supportate dal modello Shader Model 4 e shader model 4,1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli shader rispetto ai profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




