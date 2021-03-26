---
title: def-vs
description: Definisce le costanti del vertex shader.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224015"
---
# <a name="def---vs"></a><span data-ttu-id="299dc-103">def-vs</span><span class="sxs-lookup"><span data-stu-id="299dc-103">def - vs</span></span>

<span data-ttu-id="299dc-104">Definisce le costanti del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="299dc-104">Defines vertex shader constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="299dc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="299dc-105">Syntax</span></span>



| <span data-ttu-id="299dc-106">def DST, float1, float2, float3, float4</span><span class="sxs-lookup"><span data-stu-id="299dc-106">def dst, float1, float2, float3, float4</span></span> |
|-----------------------------------------|



 

<span data-ttu-id="299dc-107">dove</span><span class="sxs-lookup"><span data-stu-id="299dc-107">where</span></span>

-   <span data-ttu-id="299dc-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="299dc-108">dst is the destination register.</span></span>
-   <span data-ttu-id="299dc-109">float1, float2, float3, float4 sono quattro numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="299dc-109">float1, float2, float3, float4 are four floating point numbers.</span></span>

## <a name="remarks"></a><span data-ttu-id="299dc-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="299dc-110">Remarks</span></span>



| <span data-ttu-id="299dc-111">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="299dc-111">Vertex shader versions</span></span> | <span data-ttu-id="299dc-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="299dc-112">1\_1</span></span> | <span data-ttu-id="299dc-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="299dc-113">2\_0</span></span> | <span data-ttu-id="299dc-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="299dc-114">2\_x</span></span> | <span data-ttu-id="299dc-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="299dc-115">2\_sw</span></span> | <span data-ttu-id="299dc-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="299dc-116">3\_0</span></span> | <span data-ttu-id="299dc-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="299dc-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="299dc-118">def</span><span class="sxs-lookup"><span data-stu-id="299dc-118">def</span></span>                    | <span data-ttu-id="299dc-119">x</span><span class="sxs-lookup"><span data-stu-id="299dc-119">x</span></span>    | <span data-ttu-id="299dc-120">x</span><span class="sxs-lookup"><span data-stu-id="299dc-120">x</span></span>    | <span data-ttu-id="299dc-121">x</span><span class="sxs-lookup"><span data-stu-id="299dc-121">x</span></span>    | <span data-ttu-id="299dc-122">x</span><span class="sxs-lookup"><span data-stu-id="299dc-122">x</span></span>     | <span data-ttu-id="299dc-123">x</span><span class="sxs-lookup"><span data-stu-id="299dc-123">x</span></span>    | <span data-ttu-id="299dc-124">x</span><span class="sxs-lookup"><span data-stu-id="299dc-124">x</span></span>     |



 

<span data-ttu-id="299dc-125">L'istruzione def definisce una costante dello shader il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="299dc-125">The def instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="299dc-126">Sono denominate costanti immediate.</span><span class="sxs-lookup"><span data-stu-id="299dc-126">These are called immediate constants.</span></span> <span data-ttu-id="299dc-127">Le costanti immediate hanno la precedenza sulle costanti impostate dai metodi API SetVertexShaderConstantF.</span><span class="sxs-lookup"><span data-stu-id="299dc-127">Immediate constants take precedence over constants set by API methods SetVertexShaderConstantF.</span></span>

<span data-ttu-id="299dc-128">Esistono due modi per impostare una costante in uno shader.</span><span class="sxs-lookup"><span data-stu-id="299dc-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="299dc-129">Usare def-vs per definire la costante direttamente all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="299dc-129">Use def - vs to define the constant directly inside a shader.</span></span>

    <span data-ttu-id="299dc-130">def-vs può definire solo costanti a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="299dc-130">def - vs can only define floating-point constants.</span></span>

2.  <span data-ttu-id="299dc-131">Usare i metodi API per impostare una costante.</span><span class="sxs-lookup"><span data-stu-id="299dc-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="299dc-132">Usare [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) per impostare una costante a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="299dc-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) to set a floating-point constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="299dc-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="299dc-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="299dc-134">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="299dc-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="299dc-135">defi-vs</span><span class="sxs-lookup"><span data-stu-id="299dc-135">defi - vs</span></span>](defi---vs.md)
</dt> <dt>

[<span data-ttu-id="299dc-136">defb-vs</span><span class="sxs-lookup"><span data-stu-id="299dc-136">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 