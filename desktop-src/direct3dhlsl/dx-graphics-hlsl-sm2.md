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
# <a name="shader-model-2"></a><span data-ttu-id="1c388-103">Modello Shader 2</span><span class="sxs-lookup"><span data-stu-id="1c388-103">Shader Model 2</span></span>

<span data-ttu-id="1c388-104">Shader Model 2 ha aggiunto funzionalità aggiuntive al [modello di shader 1](dx-graphics-hlsl-sm1.md).</span><span class="sxs-lookup"><span data-stu-id="1c388-104">Shader Model 2 added additional capabilities to [shader model 1](dx-graphics-hlsl-sm1.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c388-105">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="1c388-105">Feature</span></span></td>
<td><span data-ttu-id="1c388-106">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="1c388-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c388-107">Set di istruzioni</span><span class="sxs-lookup"><span data-stu-id="1c388-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="1c388-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funzioni HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="1c388-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="1c388-109">Istruzioni per gli assembly (vedere <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">le istruzioni-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">istruzioni-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">istruzioni per ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x istruzioni</a>)</span><span class="sxs-lookup"><span data-stu-id="1c388-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Instructions - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">Instructions - vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 Instructions</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Instructions</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c388-110">Registra set</span><span class="sxs-lookup"><span data-stu-id="1c388-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="1c388-111">Registri pixel shader (vedere <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">registri ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">registri ps_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="1c388-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0 Registers</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Registers</a>)</span></span></li>
<li><span data-ttu-id="1c388-112">Registri vertex shader (vedere <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">registri-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registri-vs_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="1c388-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registers - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Registers - vs_2_x</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c388-113">Pixel shader max</span><span class="sxs-lookup"><span data-stu-id="1c388-113">Pixel Shader Max</span></span></td>
<td><ul>
<li><span data-ttu-id="1c388-114">trama ps_2_0-32 + aritmetica 64</span><span class="sxs-lookup"><span data-stu-id="1c388-114">ps_2_0 - 32 texture + 64 arithmetic</span></span></li>
<li><span data-ttu-id="1c388-115">ps_2_x-96 minimo e fino al numero di slot in D3DCAPS9. D3DPSHADERCAPS2_0. NumInstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="1c388-115">ps_2_x - 96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2_0.NumInstructionSlots.</span></span> <span data-ttu-id="1c388-116">Vedere D3DPSHADERCAPS2_0</span><span class="sxs-lookup"><span data-stu-id="1c388-116">See D3DPSHADERCAPS2_0</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c388-117">Vertex shader max</span><span class="sxs-lookup"><span data-stu-id="1c388-117">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="1c388-118">256 istruzioni</span><span class="sxs-lookup"><span data-stu-id="1c388-118">256 instructions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c388-119">Profili shader</span><span class="sxs-lookup"><span data-stu-id="1c388-119">Shader Profiles</span></span></td>
<td><span data-ttu-id="1c388-120">ps_2_0, ps_2_x, vs_2_0, vs_2_x</span><span class="sxs-lookup"><span data-stu-id="1c388-120">ps_2_0, ps_2_x, vs_2_0, vs_2_x</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1c388-121">Per ulteriori informazioni sul modello Shader 2, vedere:</span><span class="sxs-lookup"><span data-stu-id="1c388-121">For more details on shader model 2, see:</span></span>

-   <span data-ttu-id="1c388-122">[Pixel shader 2,0](dx9-graphics-reference-asm-ps-2-0.md), [pixel shader 2. x](dx9-graphics-reference-asm-ps-2-x.md)</span><span class="sxs-lookup"><span data-stu-id="1c388-122">[Pixel Shader 2.0](dx9-graphics-reference-asm-ps-2-0.md), [Pixel Shader 2.x](dx9-graphics-reference-asm-ps-2-x.md)</span></span>
-   <span data-ttu-id="1c388-123">[Vertex shader 2,0](dx9-graphics-reference-asm-vs-2-0.md), [vertex shader 2. x](dx9-graphics-reference-asm-vs-2-x.md)</span><span class="sxs-lookup"><span data-stu-id="1c388-123">[Vertex Shader 2.0](dx9-graphics-reference-asm-vs-2-0.md), [Vertex Shader 2.x](dx9-graphics-reference-asm-vs-2-x.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c388-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c388-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c388-125">Modelli shader rispetto ai profili shader</span><span class="sxs-lookup"><span data-stu-id="1c388-125">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




