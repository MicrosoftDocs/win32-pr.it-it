---
title: Modello Shader 5,1
description: Questa sezione contiene le pagine di riferimento per il modello HLSL shader 5,1, introdotto con D3D12.
ms.assetid: 814FAC95-7FD5-450F-964B-18E687DBCC56
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5fd2f2a2f4ebe86a090ebade8ebf8a033a7c612
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993048"
---
# <a name="shader-model-51"></a><span data-ttu-id="c3daa-103">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="c3daa-103">Shader Model 5.1</span></span>

<span data-ttu-id="c3daa-104">Questa sezione contiene le pagine di riferimento per il modello HLSL shader 5,1, introdotto con D3D12.</span><span class="sxs-lookup"><span data-stu-id="c3daa-104">This section contains the reference pages for HLSL Shader Model 5.1, introduced with D3D12.</span></span>

<span data-ttu-id="c3daa-105">Il modello di shader 5,1 è funzionalmente molto simile al [modello di shader 5](d3d11-graphics-reference-sm5.md). la modifica principale è più flessibile nella selezione delle risorse, consentendo l'indicizzazione di matrici di descrittori dall'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="c3daa-105">Shader Model 5.1 is functionally very similar to [Shader Model 5](d3d11-graphics-reference-sm5.md), the main change is more flexibility in resource selection by allowing indexing of arrays of descriptors from within a shader.</span></span>



| <span data-ttu-id="c3daa-106">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="c3daa-106">Feature</span></span>                   | <span data-ttu-id="c3daa-107">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="c3daa-107">Capability</span></span>                                                                |
|---------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c3daa-108">Set di istruzioni</span><span class="sxs-lookup"><span data-stu-id="c3daa-108">Instruction Set</span></span>           | [<span data-ttu-id="c3daa-109">**Funzioni intrinseche HLSL**</span><span class="sxs-lookup"><span data-stu-id="c3daa-109">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)  |
| <span data-ttu-id="c3daa-110">Vertex shader max</span><span class="sxs-lookup"><span data-stu-id="c3daa-110">Vertex Shader Max</span></span>         | <span data-ttu-id="c3daa-111">Nessuna restrizione</span><span class="sxs-lookup"><span data-stu-id="c3daa-111">No restriction</span></span>                                                            |
| <span data-ttu-id="c3daa-112">Pixel shader max</span><span class="sxs-lookup"><span data-stu-id="c3daa-112">Pixel Shader Max</span></span>          | <span data-ttu-id="c3daa-113">Nessuna restrizione</span><span class="sxs-lookup"><span data-stu-id="c3daa-113">No restriction</span></span>                                                            |
| <span data-ttu-id="c3daa-114">Nuovi profili shader aggiunti</span><span class="sxs-lookup"><span data-stu-id="c3daa-114">New Shader Profiles Added</span></span> | <span data-ttu-id="c3daa-115">cs \_ 5 \_ 1, DS \_ 5 \_ 1, GS \_ 5 \_ 1, HS \_ 5 \_ 1, PS \_ 5 \_ 1, vs \_ 5 \_ 1, rootsig \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c3daa-115">cs\_5\_1, ds\_5\_1, gs\_5\_1, hs\_5\_1, ps\_5\_1, vs\_5\_1, rootsig\_1\_0</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="c3daa-116">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c3daa-116">In this section</span></span>



| <span data-ttu-id="c3daa-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="c3daa-117">Topic</span></span>                                                                           | <span data-ttu-id="c3daa-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3daa-118">Description</span></span>                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c3daa-119">Oggetti modello shader 5,1</span><span class="sxs-lookup"><span data-stu-id="c3daa-119">Shader Model 5.1 Objects</span></span>](shader-model-5-1-objects.md)<br/>             | <span data-ttu-id="c3daa-120">Al modello di shader 5,1 sono stati aggiunti gli oggetti seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3daa-120">The following objects have been added to shader model 5.1.</span></span><br/> |
| [<span data-ttu-id="c3daa-121">Valori di sistema del modello shader 5,1</span><span class="sxs-lookup"><span data-stu-id="c3daa-121">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)<br/> | <span data-ttu-id="c3daa-122">Il modello di shader 5,1 aggiunge i nuovi valori di sistema seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3daa-122">Shader Model 5.1 adds the following new system values.</span></span><br/>     |



 

## <a name="related-topics"></a><span data-ttu-id="c3daa-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3daa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3daa-124">Modelli shader rispetto ai profili shader</span><span class="sxs-lookup"><span data-stu-id="c3daa-124">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> <dt>

[<span data-ttu-id="c3daa-125">Funzionalità del modello HLSL shader 5,1 per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c3daa-125">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 





