---
title: Modello Shader 3
description: Shader Model 3 ha aggiunto funzionalità aggiuntive al modello Shader 2.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c53b8252f617c6ee3b95512a5d930a93f646479
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104399817"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader Model 3 (riferimento HLSL)

Shader Model 3 ha aggiunto funzionalità aggiuntive al [Modello Shader 2](dx-graphics-hlsl-sm2.md).



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
<li>Istruzioni per gli assembly (vedere <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">le istruzioni ps_3_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">istruzioni-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Registra set</td>
<td><ul>
<li>Registri pixel shader (vedere <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">Ps_3_0 registri</a>)</li>
<li>Registri vertex shader (vedere <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">registri-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Pixel shader max</td>
<td>512 minimo e fino al numero di slot in D3DCAPS9. MaxPixelShader30InstructionSlots (vedere <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</td>
</tr>
<tr class="odd">
<td>Vertex shader max</td>
<td>512 minimo e fino al numero di slot in D3DCAPS9. MaxVertexShader30InstructionSlots (vedere <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</td>
</tr>
<tr class="even">
<td>Profili shader</td>
<td>ps_3_0, vs_3_0</td>
</tr>
</tbody>
</table>



 

Per ulteriori informazioni sugli shader del modello 3, vedere:

-   [Pixel shader 3,0](dx9-graphics-reference-asm-ps-3-0.md)
-   [Vertex Shader 3,0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli shader rispetto ai profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 