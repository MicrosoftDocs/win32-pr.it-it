---
title: Modello shader 2
description: Shader Model 2 ha aggiunto funzionalità aggiuntive al modello shader 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23b4caa0e4da92e992eb0486f5a998ad7d21016dc691563f29589c5fc9ab5310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119975"
---
# <a name="shader-model-2"></a>Modello shader 2

Shader Model 2 ha aggiunto funzionalità aggiuntive al [modello shader 1.](dx-graphics-hlsl-sm1.md)



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
<li>Istruzioni per l'assembly <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">(vedere Instructions - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">Instructions - vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 Instructions</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Instructions</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Registra set</td>
<td><ul>
<li>Registri pixel shader (vedere Ps_2_0 <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">Registers</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Registers</a>)</li>
<li>Registri vertex shader (vedere <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registri - vs_2_0</a>, Registri - <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">vs_2_x</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Pixel Shader Max</td>
<td><ul>
<li>ps_2_0 - Trama 32 + 64 aritmetica</li>
<li>ps_2_x: almeno 96 e fino al numero di slot in D3DCAPS9. D3DPSHADERCAPS2_0.NumInstructionSlots. Vedere D3DPSHADERCAPS2_0</li>
</ul></td>
</tr>
<tr class="odd">
<td>Numero massimo di vertex shader</td>
<td>256 istruzioni</td>
</tr>
<tr class="even">
<td>Profili shader</td>
<td>ps_2_0, ps_2_x, vs_2_0, vs_2_x</td>
</tr>
</tbody>
</table>



 

Per altri dettagli sul modello shader 2, vedere:

-   [Pixel Shader 2.0](dx9-graphics-reference-asm-ps-2-0.md), [Pixel Shader 2.x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Vertex Shader 2.0](dx9-graphics-reference-asm-vs-2-0.md), [Vertex Shader 2.x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli shader e profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




