---
title: dcl_function_body (SM5-ASM)
description: Dichiarare il corpo di una funzione.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117229"
---
# <a name="dcl_function_body-sm5---asm"></a><span data-ttu-id="742fc-103">\_corpo della funzione DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="742fc-103">dcl\_function\_body (sm5 - asm)</span></span>

<span data-ttu-id="742fc-104">Dichiarare il corpo di una funzione.</span><span class="sxs-lookup"><span data-stu-id="742fc-104">Declare a function body.</span></span>



| <span data-ttu-id="742fc-105">\_corpo della funzione DCL \_ FB\#</span><span class="sxs-lookup"><span data-stu-id="742fc-105">dcl\_function\_body fb\#</span></span> |
|--------------------------|



 



| <span data-ttu-id="742fc-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="742fc-106">Item</span></span>                                                          | <span data-ttu-id="742fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="742fc-107">Description</span></span>                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="742fc-108"><span id="fb_"></span><span id="FB_"></span>*FB\#*</span><span class="sxs-lookup"><span data-stu-id="742fc-108"><span id="fb_"></span><span id="FB_"></span>*fb\#*</span></span><br/> | <span data-ttu-id="742fc-109">\[nell' \] etichetta della posizione in cui verrà visualizzata la funzione.</span><span class="sxs-lookup"><span data-stu-id="742fc-109">\[in\] The label of the place where the function will appear.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="742fc-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="742fc-110">Remarks</span></span>

<span data-ttu-id="742fc-111">Questa istruzione dichiara un corpo della funzione univoco il cui codice verrà visualizzato in un secondo momento nel programma in corrispondenza dell'etichetta FB \# .</span><span class="sxs-lookup"><span data-stu-id="742fc-111">This instruction declares a unique function body whose code will appear later in the program at label fb\#.</span></span>

<span data-ttu-id="742fc-112">I corpi delle funzioni vengono usati nelle dichiarazioni di tabella di funzione.</span><span class="sxs-lookup"><span data-stu-id="742fc-112">Function bodies are used in function table declarations.</span></span> <span data-ttu-id="742fc-113">Per altre informazioni, vedere [ \_ \_ tabella delle funzioni DCL](dcl-function-table---sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="742fc-113">For more info, see [dcl\_function\_table](dcl-function-table---sm5---asm-.md).</span></span>

<span data-ttu-id="742fc-114">In Hull shader e Domain shader, in cui sono presenti più fasi (fase del punto di controllo, fase della divisione e fase di join), tutti i corpi delle funzioni (etichetta FB \# ) vengono visualizzati dopo tutte le fasi, anziché essere raggruppati per fase.</span><span class="sxs-lookup"><span data-stu-id="742fc-114">In the hull shader and domain shader, where there are multiple phases (control point phase, fork phase, and join phase), all function bodies (label fb\#) appear after all the phases, rather than being grouped by phase.</span></span>

<span data-ttu-id="742fc-115">Non esiste alcun limite al numero di corpi delle funzioni che possono essere presenti.</span><span class="sxs-lookup"><span data-stu-id="742fc-115">There is no limit to how many function bodies can be present.</span></span>

<span data-ttu-id="742fc-116">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="742fc-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="742fc-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="742fc-117">Vertex</span></span> | <span data-ttu-id="742fc-118">Hull</span><span class="sxs-lookup"><span data-stu-id="742fc-118">Hull</span></span> | <span data-ttu-id="742fc-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="742fc-119">Domain</span></span> | <span data-ttu-id="742fc-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="742fc-120">Geometry</span></span> | <span data-ttu-id="742fc-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="742fc-121">Pixel</span></span> | <span data-ttu-id="742fc-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="742fc-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="742fc-123">X</span><span class="sxs-lookup"><span data-stu-id="742fc-123">X</span></span>      | <span data-ttu-id="742fc-124">X</span><span class="sxs-lookup"><span data-stu-id="742fc-124">X</span></span>    | <span data-ttu-id="742fc-125">X</span><span class="sxs-lookup"><span data-stu-id="742fc-125">X</span></span>      | <span data-ttu-id="742fc-126">X</span><span class="sxs-lookup"><span data-stu-id="742fc-126">X</span></span>        | <span data-ttu-id="742fc-127">X</span><span class="sxs-lookup"><span data-stu-id="742fc-127">X</span></span>     | <span data-ttu-id="742fc-128">X</span><span class="sxs-lookup"><span data-stu-id="742fc-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="742fc-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="742fc-129">Minimum Shader Model</span></span>

<span data-ttu-id="742fc-130">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="742fc-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="742fc-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="742fc-131">Shader Model</span></span>                                              | <span data-ttu-id="742fc-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="742fc-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="742fc-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="742fc-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="742fc-134">sì</span><span class="sxs-lookup"><span data-stu-id="742fc-134">yes</span></span>       |
| [<span data-ttu-id="742fc-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="742fc-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="742fc-136">no</span><span class="sxs-lookup"><span data-stu-id="742fc-136">no</span></span>        |
| [<span data-ttu-id="742fc-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="742fc-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="742fc-138">no</span><span class="sxs-lookup"><span data-stu-id="742fc-138">no</span></span>        |
| [<span data-ttu-id="742fc-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="742fc-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="742fc-140">no</span><span class="sxs-lookup"><span data-stu-id="742fc-140">no</span></span>        |
| [<span data-ttu-id="742fc-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="742fc-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="742fc-142">no</span><span class="sxs-lookup"><span data-stu-id="742fc-142">no</span></span>        |
| [<span data-ttu-id="742fc-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="742fc-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="742fc-144">no</span><span class="sxs-lookup"><span data-stu-id="742fc-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="742fc-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="742fc-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="742fc-146">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="742fc-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





