---
title: dcl_uav_raw (SM5-ASM)
description: Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995453"
---
# <a name="dcl_uav_raw-sm5---asm"></a><span data-ttu-id="871ae-104">\_RAW UAV DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="871ae-104">dcl\_uav\_raw (sm5 - asm)</span></span>

<span data-ttu-id="871ae-105">Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader.</span><span class="sxs-lookup"><span data-stu-id="871ae-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="871ae-106">\_ \_ \[ \_ dstUAV GLC di DCL UAV RAW \]</span><span class="sxs-lookup"><span data-stu-id="871ae-106">dcl\_uav\_raw\[\_glc\] dstUAV</span></span> |
|-------------------------------|



 



| <span data-ttu-id="871ae-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="871ae-107">Item</span></span>                                                                                           | <span data-ttu-id="871ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="871ae-108">Description</span></span>                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="871ae-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="871ae-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="871ae-110">\[nel \] UAV.</span><span class="sxs-lookup"><span data-stu-id="871ae-110">\[in\] The UAV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="871ae-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="871ae-111">Remarks</span></span>

<span data-ttu-id="871ae-112">*dstUAV* è un \# registro u dichiarato come riferimento a un UnorderedAccessView di un buffer, in cui il buffer viene visualizzato come una semplice matrice 1D di voci non tipizzate a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="871ae-112">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a Buffer, where the buffer appears as a simple 1D array of 32-bit untyped entries.</span></span>

<span data-ttu-id="871ae-113">Le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come aventi un tipo.</span><span class="sxs-lookup"><span data-stu-id="871ae-113">Operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="871ae-114">Il \_ flag GLC significa "globalmente coerente".</span><span class="sxs-lookup"><span data-stu-id="871ae-114">The \_glc flag means "globally coherent".</span></span> <span data-ttu-id="871ae-115">L'assenza di \_ GLC significa che il UAV viene dichiarato solo come "gruppo coerente" nel compute shader o "coerente localmente" in una singola chiamata di pixel shader.</span><span class="sxs-lookup"><span data-stu-id="871ae-115">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="871ae-116">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="871ae-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="871ae-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="871ae-117">Vertex</span></span> | <span data-ttu-id="871ae-118">Hull</span><span class="sxs-lookup"><span data-stu-id="871ae-118">Hull</span></span> | <span data-ttu-id="871ae-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="871ae-119">Domain</span></span> | <span data-ttu-id="871ae-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="871ae-120">Geometry</span></span> | <span data-ttu-id="871ae-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="871ae-121">Pixel</span></span> | <span data-ttu-id="871ae-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="871ae-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="871ae-123">X</span><span class="sxs-lookup"><span data-stu-id="871ae-123">X</span></span>     | <span data-ttu-id="871ae-124">X</span><span class="sxs-lookup"><span data-stu-id="871ae-124">X</span></span>       |



 

<span data-ttu-id="871ae-125">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="871ae-125">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="871ae-126">Vertice</span><span class="sxs-lookup"><span data-stu-id="871ae-126">Vertex</span></span> | <span data-ttu-id="871ae-127">Hull</span><span class="sxs-lookup"><span data-stu-id="871ae-127">Hull</span></span> | <span data-ttu-id="871ae-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="871ae-128">Domain</span></span> | <span data-ttu-id="871ae-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="871ae-129">Geometry</span></span> | <span data-ttu-id="871ae-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="871ae-130">Pixel</span></span> | <span data-ttu-id="871ae-131">Calcolo</span><span class="sxs-lookup"><span data-stu-id="871ae-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="871ae-132">X</span><span class="sxs-lookup"><span data-stu-id="871ae-132">X</span></span>      | <span data-ttu-id="871ae-133">X</span><span class="sxs-lookup"><span data-stu-id="871ae-133">X</span></span>    | <span data-ttu-id="871ae-134">X</span><span class="sxs-lookup"><span data-stu-id="871ae-134">X</span></span>      | <span data-ttu-id="871ae-135">X</span><span class="sxs-lookup"><span data-stu-id="871ae-135">X</span></span>        | <span data-ttu-id="871ae-136">X</span><span class="sxs-lookup"><span data-stu-id="871ae-136">X</span></span>     | <span data-ttu-id="871ae-137">X</span><span class="sxs-lookup"><span data-stu-id="871ae-137">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="871ae-138">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="871ae-138">Minimum Shader Model</span></span>

<span data-ttu-id="871ae-139">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="871ae-139">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="871ae-140">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="871ae-140">Shader Model</span></span>                                              | <span data-ttu-id="871ae-141">Supportato</span><span class="sxs-lookup"><span data-stu-id="871ae-141">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="871ae-142">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="871ae-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="871ae-143">sì</span><span class="sxs-lookup"><span data-stu-id="871ae-143">yes</span></span>       |
| [<span data-ttu-id="871ae-144">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="871ae-144">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="871ae-145">no</span><span class="sxs-lookup"><span data-stu-id="871ae-145">no</span></span>        |
| [<span data-ttu-id="871ae-146">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="871ae-146">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="871ae-147">no</span><span class="sxs-lookup"><span data-stu-id="871ae-147">no</span></span>        |
| [<span data-ttu-id="871ae-148">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="871ae-148">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="871ae-149">no</span><span class="sxs-lookup"><span data-stu-id="871ae-149">no</span></span>        |
| [<span data-ttu-id="871ae-150">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="871ae-150">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="871ae-151">no</span><span class="sxs-lookup"><span data-stu-id="871ae-151">no</span></span>        |
| [<span data-ttu-id="871ae-152">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="871ae-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="871ae-153">no</span><span class="sxs-lookup"><span data-stu-id="871ae-153">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="871ae-154">Questa istruzione è supportata in cs \_ 4 \_ 0 e cs \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="871ae-154">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="871ae-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="871ae-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="871ae-156">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="871ae-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





