---
title: ld_uav_typed (SM5-ASM)
description: Lettura ad accesso casuale di un elemento da una visualizzazione di accesso non ordinato (UAV) tipizzata.
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335535"
---
# <a name="ld_uav_typed-sm5---asm"></a><span data-ttu-id="454c2-103">LD \_ UAV \_ tipizzato (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="454c2-103">ld\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="454c2-104">Lettura ad accesso casuale di un elemento da una visualizzazione di accesso non ordinato (UAV) tipizzata.</span><span class="sxs-lookup"><span data-stu-id="454c2-104">Random-access read of an element from a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="454c2-105">LD \_ UAV \_ tipizzato dst0 \[ . mask \] , srcAddress \[ . Swizzle \] , srcUAV \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="454c2-105">ld\_uav\_typed dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="454c2-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="454c2-106">Item</span></span>                                                                                                           | <span data-ttu-id="454c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="454c2-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="454c2-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="454c2-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="454c2-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="454c2-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="454c2-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="454c2-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/> | <span data-ttu-id="454c2-111">\[in \] specifica l'indirizzo da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="454c2-111">\[in\] Specifies the address to read from.</span></span><br/>          |
| <span data-ttu-id="454c2-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span><span class="sxs-lookup"><span data-stu-id="454c2-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span></span><br/>                 | <span data-ttu-id="454c2-113">\[nell' \] origine da cui eseguire la lettura.</span><span class="sxs-lookup"><span data-stu-id="454c2-113">\[in\] The source to read from.</span></span> <br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="454c2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="454c2-114">Remarks</span></span>

<span data-ttu-id="454c2-115">Questa istruzione esegue un elemento a 4 componenti letto da *srcUAV* in corrispondenza dell'indirizzo Unsigned Integer in *srcAddress*, convertito a 32 bit per componente in base al formato, quindi scritto in *dst0* nello shader.</span><span class="sxs-lookup"><span data-stu-id="454c2-115">This instruction performs a 4-component element read from *srcUAV* at the unsigned integer address in *srcAddress*, converted to 32bit per component based on the format, then written to *dst0* in the shader.</span></span>

<span data-ttu-id="454c2-116">*srcUAV* è un UAV (u \# ) dichiarato come tipizzato.</span><span class="sxs-lookup"><span data-stu-id="454c2-116">*srcUAV* is a UAV (u\#) declared as typed.</span></span> <span data-ttu-id="454c2-117">Il tipo della risorsa associata, tuttavia, deve essere R32 \_ uint/Sint/float.</span><span class="sxs-lookup"><span data-stu-id="454c2-117">However, the type of the bound resource must be R32\_UINT/SINT/FLOAT.</span></span>

<span data-ttu-id="454c2-118">Il numero di componenti Unsigned Integer a 32 bit presi dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata in *srcUAV*.</span><span class="sxs-lookup"><span data-stu-id="454c2-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *srcUAV*.</span></span> <span data-ttu-id="454c2-119">L'indirizzamento è identico a quello dell'istruzione [LD](ld--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="454c2-119">Addressing is the same as the [ld](ld--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="454c2-120">L'indirizzamento fuori limite equivale all'istruzione **LD** .</span><span class="sxs-lookup"><span data-stu-id="454c2-120">Out of bounds addressing is the same as the **ld** instruction.</span></span>

<span data-ttu-id="454c2-121">Il comportamento di questa istruzione è identico all'istruzione **LD** se viene chiamato come **LD dst0 \[ . mask \] , srcAddress \[ . Swizzle \] , srcUAV \[ . \] swizzle**</span><span class="sxs-lookup"><span data-stu-id="454c2-121">The behavior of this instruction is identical to the **ld** instruction if called as **ld dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]**</span></span>

<span data-ttu-id="454c2-122">Non è valido e non è definito per usare questa istruzione in un UAV non dichiarato come tipizzato.</span><span class="sxs-lookup"><span data-stu-id="454c2-122">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="454c2-123">Questa operazione su un UAV strutturato o non di tipo non è valida.</span><span class="sxs-lookup"><span data-stu-id="454c2-123">Doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="454c2-124">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="454c2-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="454c2-125">Vertice</span><span class="sxs-lookup"><span data-stu-id="454c2-125">Vertex</span></span> | <span data-ttu-id="454c2-126">Hull</span><span class="sxs-lookup"><span data-stu-id="454c2-126">Hull</span></span> | <span data-ttu-id="454c2-127">Dominio</span><span class="sxs-lookup"><span data-stu-id="454c2-127">Domain</span></span> | <span data-ttu-id="454c2-128">Geometria</span><span class="sxs-lookup"><span data-stu-id="454c2-128">Geometry</span></span> | <span data-ttu-id="454c2-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="454c2-129">Pixel</span></span> | <span data-ttu-id="454c2-130">Calcolo</span><span class="sxs-lookup"><span data-stu-id="454c2-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="454c2-131">X</span><span class="sxs-lookup"><span data-stu-id="454c2-131">X</span></span>     | <span data-ttu-id="454c2-132">X</span><span class="sxs-lookup"><span data-stu-id="454c2-132">X</span></span>       |



 

<span data-ttu-id="454c2-133">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="454c2-133">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="454c2-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="454c2-134">Vertex</span></span> | <span data-ttu-id="454c2-135">Hull</span><span class="sxs-lookup"><span data-stu-id="454c2-135">Hull</span></span> | <span data-ttu-id="454c2-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="454c2-136">Domain</span></span> | <span data-ttu-id="454c2-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="454c2-137">Geometry</span></span> | <span data-ttu-id="454c2-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="454c2-138">Pixel</span></span> | <span data-ttu-id="454c2-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="454c2-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="454c2-140">X</span><span class="sxs-lookup"><span data-stu-id="454c2-140">X</span></span>      | <span data-ttu-id="454c2-141">X</span><span class="sxs-lookup"><span data-stu-id="454c2-141">X</span></span>    | <span data-ttu-id="454c2-142">X</span><span class="sxs-lookup"><span data-stu-id="454c2-142">X</span></span>      | <span data-ttu-id="454c2-143">X</span><span class="sxs-lookup"><span data-stu-id="454c2-143">X</span></span>        | <span data-ttu-id="454c2-144">X</span><span class="sxs-lookup"><span data-stu-id="454c2-144">X</span></span>     | <span data-ttu-id="454c2-145">X</span><span class="sxs-lookup"><span data-stu-id="454c2-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="454c2-146">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="454c2-146">Minimum Shader Model</span></span>

<span data-ttu-id="454c2-147">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="454c2-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="454c2-148">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="454c2-148">Shader Model</span></span>                                              | <span data-ttu-id="454c2-149">Supportato</span><span class="sxs-lookup"><span data-stu-id="454c2-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="454c2-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="454c2-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="454c2-151">sì</span><span class="sxs-lookup"><span data-stu-id="454c2-151">yes</span></span>       |
| [<span data-ttu-id="454c2-152">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="454c2-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="454c2-153">no</span><span class="sxs-lookup"><span data-stu-id="454c2-153">no</span></span>        |
| [<span data-ttu-id="454c2-154">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="454c2-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="454c2-155">no</span><span class="sxs-lookup"><span data-stu-id="454c2-155">no</span></span>        |
| [<span data-ttu-id="454c2-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="454c2-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="454c2-157">no</span><span class="sxs-lookup"><span data-stu-id="454c2-157">no</span></span>        |
| [<span data-ttu-id="454c2-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="454c2-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="454c2-159">no</span><span class="sxs-lookup"><span data-stu-id="454c2-159">no</span></span>        |
| [<span data-ttu-id="454c2-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="454c2-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="454c2-161">no</span><span class="sxs-lookup"><span data-stu-id="454c2-161">no</span></span>        |



 

<span data-ttu-id="454c2-162">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.</span><span class="sxs-lookup"><span data-stu-id="454c2-162">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="454c2-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="454c2-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="454c2-164">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="454c2-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





