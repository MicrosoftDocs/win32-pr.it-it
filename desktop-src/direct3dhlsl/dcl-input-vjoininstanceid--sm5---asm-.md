---
title: dcl_input vJoinInstanceID (SM5-ASM)
description: Dichiarare l'ID istanza in una fase di join Hull shader.
ms.assetid: 2EABB24A-7ED7-460D-A2AD-D2C40DCCB2DC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bae9351fc7183aa37cd660c265aab803f4661e9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956086"
---
# <a name="dcl_input-vjoininstanceid-sm5---asm"></a><span data-ttu-id="946d0-103">\_vJoinInstanceID di input DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="946d0-103">dcl\_input vJoinInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="946d0-104">Dichiarare l'ID istanza in una fase di join Hull shader.</span><span class="sxs-lookup"><span data-stu-id="946d0-104">Declare the instance ID in a hull shader join phase.</span></span>



| <span data-ttu-id="946d0-105">\_vJoinInstanceID di input DCL</span><span class="sxs-lookup"><span data-stu-id="946d0-105">dcl\_input vJoinInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="946d0-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="946d0-106">Item</span></span>                                                                                                                               | <span data-ttu-id="946d0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="946d0-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="946d0-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span><span class="sxs-lookup"><span data-stu-id="946d0-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span></span><br/> | <span data-ttu-id="946d0-109">\[nell' \] ID istanza.</span><span class="sxs-lookup"><span data-stu-id="946d0-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="946d0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="946d0-110">Remarks</span></span>

<span data-ttu-id="946d0-111">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="946d0-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="946d0-112">Vertice</span><span class="sxs-lookup"><span data-stu-id="946d0-112">Vertex</span></span> | <span data-ttu-id="946d0-113">Hull</span><span class="sxs-lookup"><span data-stu-id="946d0-113">Hull</span></span> | <span data-ttu-id="946d0-114">Dominio</span><span class="sxs-lookup"><span data-stu-id="946d0-114">Domain</span></span> | <span data-ttu-id="946d0-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="946d0-115">Geometry</span></span> | <span data-ttu-id="946d0-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="946d0-116">Pixel</span></span> | <span data-ttu-id="946d0-117">Calcolo</span><span class="sxs-lookup"><span data-stu-id="946d0-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="946d0-118">X</span><span class="sxs-lookup"><span data-stu-id="946d0-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="946d0-119">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="946d0-119">Minimum Shader Model</span></span>

<span data-ttu-id="946d0-120">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="946d0-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="946d0-121">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="946d0-121">Shader Model</span></span>                                              | <span data-ttu-id="946d0-122">Supportato</span><span class="sxs-lookup"><span data-stu-id="946d0-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="946d0-123">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="946d0-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="946d0-124">sì</span><span class="sxs-lookup"><span data-stu-id="946d0-124">yes</span></span>       |
| [<span data-ttu-id="946d0-125">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="946d0-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="946d0-126">no</span><span class="sxs-lookup"><span data-stu-id="946d0-126">no</span></span>        |
| [<span data-ttu-id="946d0-127">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="946d0-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="946d0-128">no</span><span class="sxs-lookup"><span data-stu-id="946d0-128">no</span></span>        |
| [<span data-ttu-id="946d0-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="946d0-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="946d0-130">no</span><span class="sxs-lookup"><span data-stu-id="946d0-130">no</span></span>        |
| [<span data-ttu-id="946d0-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="946d0-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="946d0-132">no</span><span class="sxs-lookup"><span data-stu-id="946d0-132">no</span></span>        |
| [<span data-ttu-id="946d0-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="946d0-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="946d0-134">no</span><span class="sxs-lookup"><span data-stu-id="946d0-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="946d0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="946d0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="946d0-136">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="946d0-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





