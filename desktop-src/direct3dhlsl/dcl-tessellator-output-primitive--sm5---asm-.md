---
title: dcl_tessellator_output_primitive (SM5-ASM)
description: Dichiarare il tipo primitivo di output mosaico in una sezione di dichiarazione Hull shader.
ms.assetid: 95F074C5-6012-4160-B78E-440C33C1ECC3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 390f22cdafe3b0d078bf8a502623a1c741e34e34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046120"
---
# <a name="dcl_tessellator_output_primitive-sm5---asm"></a><span data-ttu-id="65f52-103">\_ \_ \_ primitiva di output mosaico di DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="65f52-103">dcl\_tessellator\_output\_primitive (sm5 - asm)</span></span>

<span data-ttu-id="65f52-104">Dichiarare il tipo primitivo di output mosaico in una sezione di dichiarazione Hull shader.</span><span class="sxs-lookup"><span data-stu-id="65f52-104">Declare the tessellator output primitive type in a hull shader declaration section.</span></span>



| <span data-ttu-id="65f52-105">\_primitive di output mosaico di DCL \_ \_ {punto di output \_ </span><span class="sxs-lookup"><span data-stu-id="65f52-105">dcl\_tessellator\_output\_primitive {output\_point </span></span>\| <span data-ttu-id="65f52-106">riga di output \_ </span><span class="sxs-lookup"><span data-stu-id="65f52-106">output\_line </span></span>\| <span data-ttu-id="65f52-107">triangloutput \_ e \_ CW </span><span class="sxs-lookup"><span data-stu-id="65f52-107">triangloutput\_e\_cw </span></span>\| <span data-ttu-id="65f52-108">triangolo di output \_ \_ CCW}</span><span class="sxs-lookup"><span data-stu-id="65f52-108">output\_triangle\_ccw}</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="65f52-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="65f52-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="65f52-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65f52-110">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="65f52-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*linea di output del punto di output \_ \| \_ \| triangloutput \_ e \_ triangolo di \| output CW \_ \_ CCW*</span><span class="sxs-lookup"><span data-stu-id="65f52-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*output\_point \| output\_line \| triangloutput\_e\_cw \| output\_triangle\_ccw*</span></span><br/> | <span data-ttu-id="65f52-112">\[nel \] tipo primitivo di output.</span><span class="sxs-lookup"><span data-stu-id="65f52-112">\[in\] The output primitive type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65f52-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="65f52-113">Remarks</span></span>

<span data-ttu-id="65f52-114">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="65f52-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="65f52-115">Vertice</span><span class="sxs-lookup"><span data-stu-id="65f52-115">Vertex</span></span> | <span data-ttu-id="65f52-116">Hull</span><span class="sxs-lookup"><span data-stu-id="65f52-116">Hull</span></span>                 | <span data-ttu-id="65f52-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="65f52-117">Domain</span></span> | <span data-ttu-id="65f52-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="65f52-118">Geometry</span></span> | <span data-ttu-id="65f52-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="65f52-119">Pixel</span></span> | <span data-ttu-id="65f52-120">Calcolo</span><span class="sxs-lookup"><span data-stu-id="65f52-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="65f52-121">Sezione delle dichiarazioni</span><span class="sxs-lookup"><span data-stu-id="65f52-121">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65f52-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="65f52-122">Minimum Shader Model</span></span>

<span data-ttu-id="65f52-123">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="65f52-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="65f52-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="65f52-124">Shader Model</span></span>                                              | <span data-ttu-id="65f52-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="65f52-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="65f52-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="65f52-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="65f52-127">sì</span><span class="sxs-lookup"><span data-stu-id="65f52-127">yes</span></span>       |
| [<span data-ttu-id="65f52-128">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="65f52-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="65f52-129">no</span><span class="sxs-lookup"><span data-stu-id="65f52-129">no</span></span>        |
| [<span data-ttu-id="65f52-130">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="65f52-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="65f52-131">no</span><span class="sxs-lookup"><span data-stu-id="65f52-131">no</span></span>        |
| [<span data-ttu-id="65f52-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65f52-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="65f52-133">no</span><span class="sxs-lookup"><span data-stu-id="65f52-133">no</span></span>        |
| [<span data-ttu-id="65f52-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65f52-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="65f52-135">no</span><span class="sxs-lookup"><span data-stu-id="65f52-135">no</span></span>        |
| [<span data-ttu-id="65f52-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65f52-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="65f52-137">no</span><span class="sxs-lookup"><span data-stu-id="65f52-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="65f52-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65f52-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65f52-139">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65f52-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





