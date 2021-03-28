---
title: dcl_tessellator_domain (SM5-ASM)
description: Dichiarare il dominio mosaico in una sezione di dichiarazione Hull shader e il Domain shader.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398295"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a><span data-ttu-id="ae114-103">\_dominio mosaico \_ di DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ae114-103">dcl\_tessellator\_domain (sm5 - asm)</span></span>

<span data-ttu-id="ae114-104">Dichiarare il dominio mosaico in una sezione di dichiarazione Hull shader e il Domain shader.</span><span class="sxs-lookup"><span data-stu-id="ae114-104">Declare the tessellator domain in a hull shader declaration section, and the domain shader.</span></span>



| <span data-ttu-id="ae114-105">DCL \_ mosaico \_ dominio {dominio \_ oline </span><span class="sxs-lookup"><span data-stu-id="ae114-105">dcl\_tessellator\_domain {domain\_isoline </span></span>\| <span data-ttu-id="ae114-106">dominio \_ Tri </span><span class="sxs-lookup"><span data-stu-id="ae114-106">domain\_tri </span></span>\| <span data-ttu-id="ae114-107">Quad del dominio \_ }</span><span class="sxs-lookup"><span data-stu-id="ae114-107">domain\_quad}</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="ae114-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ae114-108">Item</span></span>                                                                                                                                                                                | <span data-ttu-id="ae114-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae114-109">Description</span></span>                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="ae114-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*dominio di dominio di dominio \_ \| \_ Tri \| Domain \_ quad*</span><span class="sxs-lookup"><span data-stu-id="ae114-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domain\_isoline \| domain\_tri \| domain\_quad*</span></span><br/> | <span data-ttu-id="ae114-111">\[nel \] dominio.</span><span class="sxs-lookup"><span data-stu-id="ae114-111">\[in\] The domain.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ae114-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae114-112">Remarks</span></span>

<span data-ttu-id="ae114-113">Il comportamento non è definito se Hull shader e Domain shader forniscono domini non corrispondenti o altri decalarations in conflitto.</span><span class="sxs-lookup"><span data-stu-id="ae114-113">Behavior is undefined if the hull shader and domain shader provide mismatching domains or any other conflicting decalarations.</span></span>

<span data-ttu-id="ae114-114">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae114-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ae114-115">Vertice</span><span class="sxs-lookup"><span data-stu-id="ae114-115">Vertex</span></span> | <span data-ttu-id="ae114-116">Hull</span><span class="sxs-lookup"><span data-stu-id="ae114-116">Hull</span></span>                 | <span data-ttu-id="ae114-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="ae114-117">Domain</span></span> | <span data-ttu-id="ae114-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="ae114-118">Geometry</span></span> | <span data-ttu-id="ae114-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="ae114-119">Pixel</span></span> | <span data-ttu-id="ae114-120">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ae114-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="ae114-121">Sezione delle dichiarazioni</span><span class="sxs-lookup"><span data-stu-id="ae114-121">Declarations Section</span></span> | <span data-ttu-id="ae114-122">X</span><span class="sxs-lookup"><span data-stu-id="ae114-122">X</span></span>      |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ae114-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ae114-123">Minimum Shader Model</span></span>

<span data-ttu-id="ae114-124">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae114-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ae114-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ae114-125">Shader Model</span></span>                                              | <span data-ttu-id="ae114-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="ae114-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ae114-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="ae114-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ae114-128">sì</span><span class="sxs-lookup"><span data-stu-id="ae114-128">yes</span></span>       |
| [<span data-ttu-id="ae114-129">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="ae114-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ae114-130">no</span><span class="sxs-lookup"><span data-stu-id="ae114-130">no</span></span>        |
| [<span data-ttu-id="ae114-131">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="ae114-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ae114-132">no</span><span class="sxs-lookup"><span data-stu-id="ae114-132">no</span></span>        |
| [<span data-ttu-id="ae114-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae114-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ae114-134">no</span><span class="sxs-lookup"><span data-stu-id="ae114-134">no</span></span>        |
| [<span data-ttu-id="ae114-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae114-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ae114-136">no</span><span class="sxs-lookup"><span data-stu-id="ae114-136">no</span></span>        |
| [<span data-ttu-id="ae114-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae114-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ae114-138">no</span><span class="sxs-lookup"><span data-stu-id="ae114-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ae114-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae114-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae114-140">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae114-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





