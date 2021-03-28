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
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="2b573-103">Shader Model 3 (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b573-103">Shader Model 3 (HLSL reference)</span></span>

<span data-ttu-id="2b573-104">Shader Model 3 ha aggiunto funzionalità aggiuntive al [Modello Shader 2](dx-graphics-hlsl-sm2.md).</span><span class="sxs-lookup"><span data-stu-id="2b573-104">Shader Model 3 added additional capabilities to [shader model 2](dx-graphics-hlsl-sm2.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b573-105">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="2b573-105">Feature</span></span></td>
<td><span data-ttu-id="2b573-106">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="2b573-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b573-107">Set di istruzioni</span><span class="sxs-lookup"><span data-stu-id="2b573-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="2b573-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funzioni HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b573-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="2b573-109">Istruzioni per gli assembly (vedere <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">le istruzioni ps_3_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">istruzioni-vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="2b573-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Instructions</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Instructions - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b573-110">Registra set</span><span class="sxs-lookup"><span data-stu-id="2b573-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="2b573-111">Registri pixel shader (vedere <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">Ps_3_0 registri</a>)</span><span class="sxs-lookup"><span data-stu-id="2b573-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Registers</a>)</span></span></li>
<li><span data-ttu-id="2b573-112">Registri vertex shader (vedere <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">registri-vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="2b573-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registers - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b573-113">Pixel shader max</span><span class="sxs-lookup"><span data-stu-id="2b573-113">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="2b573-114">512 minimo e fino al numero di slot in D3DCAPS9. MaxPixelShader30InstructionSlots (vedere <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="2b573-114">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b573-115">Vertex shader max</span><span class="sxs-lookup"><span data-stu-id="2b573-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="2b573-116">512 minimo e fino al numero di slot in D3DCAPS9. MaxVertexShader30InstructionSlots (vedere <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="2b573-116">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b573-117">Profili shader</span><span class="sxs-lookup"><span data-stu-id="2b573-117">Shader Profiles</span></span></td>
<td><span data-ttu-id="2b573-118">ps_3_0, vs_3_0</span><span class="sxs-lookup"><span data-stu-id="2b573-118">ps_3_0, vs_3_0</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2b573-119">Per ulteriori informazioni sugli shader del modello 3, vedere:</span><span class="sxs-lookup"><span data-stu-id="2b573-119">For more details on model 3 shaders, see:</span></span>

-   [<span data-ttu-id="2b573-120">Pixel shader 3,0</span><span class="sxs-lookup"><span data-stu-id="2b573-120">Pixel Shader 3.0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)
-   [<span data-ttu-id="2b573-121">Vertex Shader 3,0</span><span class="sxs-lookup"><span data-stu-id="2b573-121">Vertex Shader 3.0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a><span data-ttu-id="2b573-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b573-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b573-123">Modelli shader rispetto ai profili shader</span><span class="sxs-lookup"><span data-stu-id="2b573-123">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 