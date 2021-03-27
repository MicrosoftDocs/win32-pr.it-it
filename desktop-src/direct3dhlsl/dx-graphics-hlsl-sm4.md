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
# <a name="shader-model-4"></a><span data-ttu-id="9156a-103">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9156a-103">Shader Model 4</span></span>

<span data-ttu-id="9156a-104">Shader Model 4 è un superset delle funzionalità del [Modello Shader 3](dx-graphics-hlsl-sm3.md), ad eccezione del fatto che Shader Model 4 non supporta le funzionalità del modello shader 1.</span><span class="sxs-lookup"><span data-stu-id="9156a-104">Shader Model 4 is a superset of the capabilities in [Shader Model 3](dx-graphics-hlsl-sm3.md), except that Shader Model 4 doesn't support the features in Shader Model 1.</span></span> <span data-ttu-id="9156a-105">È stato progettato usando un core di shader comune che fornisce un set comune di funzionalità a tutti gli shader programmabili, che possono essere programmati solo usando HLSL.</span><span class="sxs-lookup"><span data-stu-id="9156a-105">It has been designed using a common-shader core that gives a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9156a-106">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="9156a-106">Feature</span></span></th>
<th><span data-ttu-id="9156a-107">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="9156a-107">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9156a-108">Set di istruzioni</span><span class="sxs-lookup"><span data-stu-id="9156a-108">Instruction Set</span></span></td>
<td><span data-ttu-id="9156a-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funzioni HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="9156a-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9156a-110">Registra set</span><span class="sxs-lookup"><span data-stu-id="9156a-110">Register Set</span></span></td>
<td><span data-ttu-id="9156a-111">Il set di registri è accessibile tramite i membri nei buffer di costanti e trame usando la semantica HLSL per elementi come la compressione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="9156a-111">The register set is accessible through members in constant and texture buffers using HLSL semantics for things like component packing.</span></span>
<ul>
<li><span data-ttu-id="9156a-112">Registri pixel shader (vedere <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">registri-ps_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">registri-ps_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="9156a-112">Pixel shader registers (see <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers - ps_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Registers - ps_4_1</a>)</span></span></li>
<li><span data-ttu-id="9156a-113">Registri vertex shader (vedere <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">registri-vs_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">registri-vs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="9156a-113">Vertex shader registers (see <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers - vs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Registers - vs_4_1</a>)</span></span></li>
<li><span data-ttu-id="9156a-114">Registri di Geometry shader (vedere <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">registri-gs_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">registri-gs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="9156a-114">Geometry shader registers (see <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers - gs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Registers - gs_4_1</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9156a-115">Vertex shader max</span><span class="sxs-lookup"><span data-stu-id="9156a-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="9156a-116">Nessuna restrizione</span><span class="sxs-lookup"><span data-stu-id="9156a-116">No restriction</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9156a-117">Pixel shader max</span><span class="sxs-lookup"><span data-stu-id="9156a-117">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="9156a-118">Nessuna restrizione</span><span class="sxs-lookup"><span data-stu-id="9156a-118">No restriction</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9156a-119">Nuovi profili shader aggiunti</span><span class="sxs-lookup"><span data-stu-id="9156a-119">New Shader Profiles Added</span></span></td>
<td><span data-ttu-id="9156a-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="9156a-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1\*</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9156a-121">Nuovo profilo di Effect-Framework aggiunto</span><span class="sxs-lookup"><span data-stu-id="9156a-121">New Effect-Framework Profile Added</span></span></td>
<td><span data-ttu-id="9156a-122">fx_4_0, fx_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="9156a-122">fx_4_0, fx_4_1\*</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9156a-123">\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 e FX \_ 4 \_ 1 sono supportati in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9156a-123">\* - gs\_4\_1, ps\_4\_1, vs\_4\_1 and fx\_4\_1 are supported on Direct3D 10.1 or higher.</span></span>

<span data-ttu-id="9156a-124">Shader Model 4 supporta una nuova fase della pipeline, ovvero la fase geometry-shader, che può essere usata per creare o modificare la geometria esistente.</span><span class="sxs-lookup"><span data-stu-id="9156a-124">Shader Model 4 supports a new pipeline stage—the geometry-shader stage—which can be used to create or modify existing geometry.</span></span> <span data-ttu-id="9156a-125">Include anche due nuovi tipi di oggetto: un oggetto Stream-output progettato per il flusso dei dati fuori dalla fase Geometry e un oggetto trama basato su modelli che implementa funzioni di campionamento di trama.</span><span class="sxs-lookup"><span data-stu-id="9156a-125">It also includes two new object types: a stream-output object designed for streaming data out of the geometry stage, and a templated texture object that implements texture sampling functions.</span></span>

-   [<span data-ttu-id="9156a-126">Common shader Core</span><span class="sxs-lookup"><span data-stu-id="9156a-126">Common-Shader Core</span></span>](dx-graphics-hlsl-common-core.md)
-   [<span data-ttu-id="9156a-127">Costanti</span><span class="sxs-lookup"><span data-stu-id="9156a-127">Constants</span></span>](dx-graphics-hlsl-constants.md)
-   [<span data-ttu-id="9156a-128">Geometry-oggetto shader</span><span class="sxs-lookup"><span data-stu-id="9156a-128">Geometry-Shader Object</span></span>](dx-graphics-hlsl-geometry-shader.md)
-   [<span data-ttu-id="9156a-129">Stream-oggetto di output</span><span class="sxs-lookup"><span data-stu-id="9156a-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
-   [<span data-ttu-id="9156a-130">Texture (oggetto)</span><span class="sxs-lookup"><span data-stu-id="9156a-130">Texture Object</span></span>](dx-graphics-hlsl-to-type.md)

<span data-ttu-id="9156a-131">Shader Model 4 supporta le regole di compressione che stabiliscono la disposizione dei dati quando vengono archiviati.</span><span class="sxs-lookup"><span data-stu-id="9156a-131">Shader Model 4 supports packing rules that dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="9156a-132">Queste regole sono descritte in [regole di compressione per variabili costanti](dx-graphics-hlsl-packing-rules.md)</span><span class="sxs-lookup"><span data-stu-id="9156a-132">These rules are described in [Packing Rules for Constant Variables](dx-graphics-hlsl-packing-rules.md)</span></span>

<span data-ttu-id="9156a-133">La sezione di [assembly Shader Model 4](dx-graphics-hlsl-sm4-asm.md) descrive le istruzioni di assembly supportate dal modello Shader Model 4 e shader model 4,1.</span><span class="sxs-lookup"><span data-stu-id="9156a-133">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) section describes the assembly instructions that the Shader Model 4 and Shader Model 4.1 support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9156a-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9156a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9156a-135">Modelli shader rispetto ai profili shader</span><span class="sxs-lookup"><span data-stu-id="9156a-135">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




