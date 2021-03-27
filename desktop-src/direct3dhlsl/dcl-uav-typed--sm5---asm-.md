---
title: dcl_uav_typed (SM5-ASM)
description: Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995744"
---
# <a name="dcl_uav_typed-sm5---asm"></a><span data-ttu-id="2c7af-104">DCL \_ UAV \_ tipizzato (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2c7af-104">dcl\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="2c7af-105">Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader.</span><span class="sxs-lookup"><span data-stu-id="2c7af-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="2c7af-106">\_ \_ \[ \_ GLC \] dstUAV, dimensione, tipo di DCL UAV</span><span class="sxs-lookup"><span data-stu-id="2c7af-106">dcl\_uav\_typed\[\_glc\] dstUAV, dimension, type</span></span> |
|--------------------------------------------------|



 



| <span data-ttu-id="2c7af-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c7af-107">Item</span></span>                                                                                           | <span data-ttu-id="2c7af-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c7af-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7af-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="2c7af-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="2c7af-110">\[nel \] UAV.</span><span class="sxs-lookup"><span data-stu-id="2c7af-110">\[in\] The UAV.</span></span><br/>                                                                        |
| <span data-ttu-id="2c7af-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimensione*</span><span class="sxs-lookup"><span data-stu-id="2c7af-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimension*</span></span><br/>                 | <span data-ttu-id="2c7af-112">\[in \] specifica il numero di dimensioni fornite dalle istruzioni che accedono al UAV.</span><span class="sxs-lookup"><span data-stu-id="2c7af-112">\[in\] Specifies how many dimensions the instructions accessing the UAV are providing.</span></span><br/> |
| <span data-ttu-id="2c7af-113"><span id="type"></span><span id="TYPE"></span>*tipo*</span><span class="sxs-lookup"><span data-stu-id="2c7af-113"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                                | <span data-ttu-id="2c7af-114">\[nel \] tipo di UAV.</span><span class="sxs-lookup"><span data-stu-id="2c7af-114">\[in\] The type of the UAV.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="2c7af-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c7af-115">Remarks</span></span>

<span data-ttu-id="2c7af-116">*dstUAV* è un \# registro u dichiarato come riferimento a un UnorderedAccessView che deve essere associato allo slot UAV nell' \# API.</span><span class="sxs-lookup"><span data-stu-id="2c7af-116">*dstUAV* is a u\# register being declared as a reference to an UnorderedAccessView that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="2c7af-117">La dimensione deve essere buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray o Texture3D.</span><span class="sxs-lookup"><span data-stu-id="2c7af-117">The dimension must be buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray, or Texture3D.</span></span> <span data-ttu-id="2c7af-118">Questo indica il numero di dimensioni delle istruzioni che accedono al UAV che forniscono: 1 (Texture1D, buffer), 2 (Texture1DArray, Texture2D) o 3 (Texture2DArray, Texture3D).</span><span class="sxs-lookup"><span data-stu-id="2c7af-118">This indicates how many dimensions any instructions accessing the UAV are providing: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) or 3 (Texture2DArray, Texture3D).</span></span>

<span data-ttu-id="2c7af-119">Il tipo è {UNORM, RUSSAr, UINT, SINT, FLOAT}.</span><span class="sxs-lookup"><span data-stu-id="2c7af-119">Type is {UNORM,SNORM,UINT,SINT,FLOAT}.</span></span> <span data-ttu-id="2c7af-120">Le operazioni eseguite con l'u dichiarata \# devono essere compatibili con il tipo dichiarato qui e l'UAV associato allo slot \# deve avere lo stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="2c7af-120">Operations done with the declared u\# must be compatible with the type declared here, and the UAV bound to slot \# must also have the same type.</span></span>

<span data-ttu-id="2c7af-121">Il \_ flag GLC si basa su "globalmente coerente".</span><span class="sxs-lookup"><span data-stu-id="2c7af-121">The \_glc flag stands for "globally coherent".</span></span> <span data-ttu-id="2c7af-122">L'assenza di \_ GLC significa che il UAV viene dichiarato solo come "gruppo coerente" nel compute shader o "coerente localmente" in una singola chiamata di pixel shader.</span><span class="sxs-lookup"><span data-stu-id="2c7af-122">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="2c7af-123">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c7af-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c7af-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="2c7af-124">Vertex</span></span> | <span data-ttu-id="2c7af-125">Hull</span><span class="sxs-lookup"><span data-stu-id="2c7af-125">Hull</span></span> | <span data-ttu-id="2c7af-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="2c7af-126">Domain</span></span> | <span data-ttu-id="2c7af-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="2c7af-127">Geometry</span></span> | <span data-ttu-id="2c7af-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="2c7af-128">Pixel</span></span> | <span data-ttu-id="2c7af-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2c7af-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2c7af-130">X</span><span class="sxs-lookup"><span data-stu-id="2c7af-130">X</span></span>     | <span data-ttu-id="2c7af-131">X</span><span class="sxs-lookup"><span data-stu-id="2c7af-131">X</span></span>       |



 

<span data-ttu-id="2c7af-132">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2c7af-132">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="2c7af-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="2c7af-133">Vertex</span></span> | <span data-ttu-id="2c7af-134">Hull</span><span class="sxs-lookup"><span data-stu-id="2c7af-134">Hull</span></span> | <span data-ttu-id="2c7af-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="2c7af-135">Domain</span></span> | <span data-ttu-id="2c7af-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="2c7af-136">Geometry</span></span> | <span data-ttu-id="2c7af-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="2c7af-137">Pixel</span></span> | <span data-ttu-id="2c7af-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2c7af-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2c7af-139">X</span><span class="sxs-lookup"><span data-stu-id="2c7af-139">X</span></span>      | <span data-ttu-id="2c7af-140">X</span><span class="sxs-lookup"><span data-stu-id="2c7af-140">X</span></span>    | <span data-ttu-id="2c7af-141">X</span><span class="sxs-lookup"><span data-stu-id="2c7af-141">X</span></span>      | <span data-ttu-id="2c7af-142">X</span><span class="sxs-lookup"><span data-stu-id="2c7af-142">X</span></span>        | <span data-ttu-id="2c7af-143">X</span><span class="sxs-lookup"><span data-stu-id="2c7af-143">X</span></span>     | <span data-ttu-id="2c7af-144">X</span><span class="sxs-lookup"><span data-stu-id="2c7af-144">X</span></span>       |



 

> [!Note]  
> <span data-ttu-id="2c7af-145">Questa istruzione non è supportata in Compute Shader 4. x.</span><span class="sxs-lookup"><span data-stu-id="2c7af-145">This instruction is not supported in compute shader 4.x.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c7af-146">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2c7af-146">Minimum Shader Model</span></span>

<span data-ttu-id="2c7af-147">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c7af-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2c7af-148">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2c7af-148">Shader Model</span></span>                                              | <span data-ttu-id="2c7af-149">Supportato</span><span class="sxs-lookup"><span data-stu-id="2c7af-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c7af-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2c7af-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c7af-151">sì</span><span class="sxs-lookup"><span data-stu-id="2c7af-151">yes</span></span>       |
| [<span data-ttu-id="2c7af-152">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2c7af-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c7af-153">no</span><span class="sxs-lookup"><span data-stu-id="2c7af-153">no</span></span>        |
| [<span data-ttu-id="2c7af-154">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2c7af-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c7af-155">no</span><span class="sxs-lookup"><span data-stu-id="2c7af-155">no</span></span>        |
| [<span data-ttu-id="2c7af-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c7af-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c7af-157">no</span><span class="sxs-lookup"><span data-stu-id="2c7af-157">no</span></span>        |
| [<span data-ttu-id="2c7af-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c7af-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c7af-159">no</span><span class="sxs-lookup"><span data-stu-id="2c7af-159">no</span></span>        |
| [<span data-ttu-id="2c7af-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c7af-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c7af-161">no</span><span class="sxs-lookup"><span data-stu-id="2c7af-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2c7af-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c7af-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c7af-163">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c7af-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





