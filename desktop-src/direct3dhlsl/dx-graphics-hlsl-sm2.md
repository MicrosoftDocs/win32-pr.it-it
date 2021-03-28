---
title: Modello Shader 2
description: Shader Model 2 ha aggiunto funzionalità aggiuntive al modello di shader 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88bd2f6292687c5387fadf65f8f43437904168cc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104993336"
---
# <a name="shader-model-2"></a>Modello Shader 2

Shader Model 2 ha aggiunto funzionalità aggiuntive al [modello di shader 1](dx-graphics-hlsl-sm1.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Caratteristica</td>
<td>Funzionalità</td>
</tr>
<tr class="even">
<td>Set di istruzioni</td>
<td><ul>
<li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funzioni HLSL</strong></a></li>
<li>Istruzioni per gli assembly (vedere <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">le istruzioni-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">istruzioni-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">istruzioni per ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x istruzioni</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Registra set</td>
<td><ul>
<li>Registri pixel shader (vedere <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">registri ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">registri ps_2_x</a>)</li>
<li>Registri vertex shader (vedere <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">registri-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registri-vs_2_x</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Pixel shader max</td>
<td><ul>
<li>trama ps_2_0-32 + aritmetica 64</li>
<li>ps_2_x-96 minimo e fino al numero di slot in D3DCAPS9. D3DPSHADERCAPS2_0. NumInstructionSlots. Vedere D3DPSHADERCAPS2_0</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vertex shader max</td>
<td>256 istruzioni</td>
</tr>
<tr class="even">
<td>Profili shader</td>
<td>ps_2_0, ps_2_x, vs_2_0, vs_2_x</td>
</tr>
</tbody>
</table>



 

Per ulteriori informazioni sul modello Shader 2, vedere:

-   [Pixel shader 2,0](dx9-graphics-reference-asm-ps-2-0.md), [pixel shader 2. x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Vertex shader 2,0](dx9-graphics-reference-asm-vs-2-0.md), [vertex shader 2. x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli shader rispetto ai profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




