---
title: dcl_output oMask (SM5-ASM)
description: Dichiarare un registro di output che deve essere scritto dallo shader.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398301"
---
# <a name="dcl_output-omask-sm5---asm"></a><span data-ttu-id="26ae7-103">\_oMask di output di DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="26ae7-103">dcl\_output oMask (sm5 - asm)</span></span>

<span data-ttu-id="26ae7-104">Dichiarare un registro di output che deve essere scritto dallo shader.</span><span class="sxs-lookup"><span data-stu-id="26ae7-104">Declare an output register to be written by the shader.</span></span>



| <span data-ttu-id="26ae7-105">\_o \# \[ . mask output DCL\]</span><span class="sxs-lookup"><span data-stu-id="26ae7-105">dcl\_output o\#\[.mask\]</span></span> |
|--------------------------|



 



| <span data-ttu-id="26ae7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="26ae7-106">Item</span></span>                                                   | <span data-ttu-id="26ae7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26ae7-107">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="26ae7-108"><span id="o"></span><span id="O"></span>*o*</span><span class="sxs-lookup"><span data-stu-id="26ae7-108"><span id="o"></span><span id="O"></span>*o*</span></span><br/> | <span data-ttu-id="26ae7-109">\[nel \] Registro di output.</span><span class="sxs-lookup"><span data-stu-id="26ae7-109">\[in\] The output register.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="26ae7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="26ae7-110">Remarks</span></span>


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a><span data-ttu-id="26ae7-111">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="26ae7-111">Restrictions</span></span>

-   <span data-ttu-id="26ae7-112">Il componente mask può essere qualsiasi subset di \[ xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="26ae7-112">The component mask can be any subset of \[xyzw\].</span></span> <span data-ttu-id="26ae7-113">Tuttavia, lasciando vuoti tra i componenti, lo spazio viene sprecato.</span><span class="sxs-lookup"><span data-stu-id="26ae7-113">However, leaving gaps between components wastes space.</span></span>
-   <span data-ttu-id="26ae7-114">È lecito dichiarare un superset della maschera dei componenti dichiarata per l'input dalla fase successiva.</span><span class="sxs-lookup"><span data-stu-id="26ae7-114">It is legal to declare a superset of the component mask declared for input by the next stage.</span></span> <span data-ttu-id="26ae7-115">Non sono tuttavia consentite maschere che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="26ae7-115">However mutually exclusive masks are not allowed.</span></span> <span data-ttu-id="26ae7-116">Il vertex shader che ha output O3. XY significa che il pixel shader inserire V3. z non è valido, ma l'inserimento di V3. x o V3. y o V3. XY è valido.</span><span class="sxs-lookup"><span data-stu-id="26ae7-116">The vertex shader outputting o3.xy, means the pixel shader inputting v3.z is invalid, but inputting v3.x or v3.y or v3.xy is valid.</span></span>

<span data-ttu-id="26ae7-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="26ae7-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="26ae7-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="26ae7-118">Vertex</span></span> | <span data-ttu-id="26ae7-119">Hull</span><span class="sxs-lookup"><span data-stu-id="26ae7-119">Hull</span></span> | <span data-ttu-id="26ae7-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="26ae7-120">Domain</span></span> | <span data-ttu-id="26ae7-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="26ae7-121">Geometry</span></span> | <span data-ttu-id="26ae7-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="26ae7-122">Pixel</span></span> | <span data-ttu-id="26ae7-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="26ae7-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="26ae7-124">X</span><span class="sxs-lookup"><span data-stu-id="26ae7-124">X</span></span>      | <span data-ttu-id="26ae7-125">X</span><span class="sxs-lookup"><span data-stu-id="26ae7-125">X</span></span>    | <span data-ttu-id="26ae7-126">X</span><span class="sxs-lookup"><span data-stu-id="26ae7-126">X</span></span>      | <span data-ttu-id="26ae7-127">X</span><span class="sxs-lookup"><span data-stu-id="26ae7-127">X</span></span>        | <span data-ttu-id="26ae7-128">X</span><span class="sxs-lookup"><span data-stu-id="26ae7-128">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="26ae7-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="26ae7-129">Minimum Shader Model</span></span>

<span data-ttu-id="26ae7-130">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="26ae7-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="26ae7-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="26ae7-131">Shader Model</span></span>                                              | <span data-ttu-id="26ae7-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="26ae7-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="26ae7-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="26ae7-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="26ae7-134">sì</span><span class="sxs-lookup"><span data-stu-id="26ae7-134">yes</span></span>       |
| [<span data-ttu-id="26ae7-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="26ae7-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="26ae7-136">no</span><span class="sxs-lookup"><span data-stu-id="26ae7-136">no</span></span>        |
| [<span data-ttu-id="26ae7-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="26ae7-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="26ae7-138">no</span><span class="sxs-lookup"><span data-stu-id="26ae7-138">no</span></span>        |
| [<span data-ttu-id="26ae7-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26ae7-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="26ae7-140">no</span><span class="sxs-lookup"><span data-stu-id="26ae7-140">no</span></span>        |
| [<span data-ttu-id="26ae7-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26ae7-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="26ae7-142">no</span><span class="sxs-lookup"><span data-stu-id="26ae7-142">no</span></span>        |
| [<span data-ttu-id="26ae7-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26ae7-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="26ae7-144">no</span><span class="sxs-lookup"><span data-stu-id="26ae7-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="26ae7-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26ae7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ae7-146">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26ae7-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





