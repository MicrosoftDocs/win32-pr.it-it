---
title: store_uav_typed (SM5-ASM)
description: Scrittura ad accesso casuale di un elemento in una visualizzazione di accesso non ordinato (UAV) tipizzata.
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046074"
---
# <a name="store_uav_typed-sm5---asm"></a><span data-ttu-id="365a9-103">archivio \_ UAV \_ tipizzato (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="365a9-103">store\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="365a9-104">Scrittura ad accesso casuale di un elemento in una visualizzazione di accesso non ordinato (UAV) tipizzata.</span><span class="sxs-lookup"><span data-stu-id="365a9-104">Random-access write of an element into a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="365a9-105">archivio \_ UAV \_ tipizzato dstUAV. xyzw, dstAddress \[ . Swizzle \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="365a9-105">store\_uav\_typed dstUAV.xyzw, dstAddress\[.swizzle\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="365a9-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="365a9-106">Item</span></span>                                                                                                           | <span data-ttu-id="365a9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="365a9-107">Description</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="365a9-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="365a9-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                 | <span data-ttu-id="365a9-109">\[in \] contiene il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="365a9-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="365a9-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="365a9-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="365a9-111">\[nell' \] indirizzo in cui scrivere.</span><span class="sxs-lookup"><span data-stu-id="365a9-111">\[in\] The address at which to write.</span></span><br/>        |
| <span data-ttu-id="365a9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="365a9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="365a9-113">\[nei \] componenti da scrivere.</span><span class="sxs-lookup"><span data-stu-id="365a9-113">\[in\] The components to write.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="365a9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="365a9-114">Remarks</span></span>

<span data-ttu-id="365a9-115">Questa istruzione esegue un elemento a \* 32 bit a 4 componenti scritto da *Src0* in *DstUAV* all'indirizzo in *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="365a9-115">This instruction performs a 4 component \*32-bit element written from *src0* to *dstUAV* at the address in *dstAddress*.</span></span> <span data-ttu-id="365a9-116">*dstUAV* è un UAV tipizzato (u \# ).</span><span class="sxs-lookup"><span data-stu-id="365a9-116">*dstUAV* is a typed UAV (u\#).</span></span>

<span data-ttu-id="365a9-117">Il formato del UAV determina la conversione del formato.</span><span class="sxs-lookup"><span data-stu-id="365a9-117">The format of the UAV determines format conversion.</span></span>

<span data-ttu-id="365a9-118">Il numero di componenti Unsigned Integer a 32 bit presi dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata in *dstUAV*.</span><span class="sxs-lookup"><span data-stu-id="365a9-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *dstUAV*.</span></span> <span data-ttu-id="365a9-119">Questo indirizzo si trova in elementi.</span><span class="sxs-lookup"><span data-stu-id="365a9-119">This address is in elements.</span></span>

<span data-ttu-id="365a9-120">L'indirizzamento fuori limite indica che non viene scritto alcun elemento nella memoria.</span><span class="sxs-lookup"><span data-stu-id="365a9-120">Out of bounds addressing means nothing gets written to memory.</span></span>

<span data-ttu-id="365a9-121">*dstUAV* ha sempre una maschera di scrittura xyzw.</span><span class="sxs-lookup"><span data-stu-id="365a9-121">*dstUAV* always has a .xyzw write mask.</span></span> <span data-ttu-id="365a9-122">È necessario scrivere tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="365a9-122">All components must be written.</span></span>

<span data-ttu-id="365a9-123">Non è valido e non è definito per usare questa istruzione in un UAV non dichiarato come tipizzato.</span><span class="sxs-lookup"><span data-stu-id="365a9-123">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="365a9-124">Ovvero, l'operazione su un UAV strutturato o non di tipo non è valida.</span><span class="sxs-lookup"><span data-stu-id="365a9-124">That is, doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="365a9-125">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="365a9-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="365a9-126">Vertice</span><span class="sxs-lookup"><span data-stu-id="365a9-126">Vertex</span></span> | <span data-ttu-id="365a9-127">Hull</span><span class="sxs-lookup"><span data-stu-id="365a9-127">Hull</span></span> | <span data-ttu-id="365a9-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="365a9-128">Domain</span></span> | <span data-ttu-id="365a9-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="365a9-129">Geometry</span></span> | <span data-ttu-id="365a9-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="365a9-130">Pixel</span></span> | <span data-ttu-id="365a9-131">Calcolo</span><span class="sxs-lookup"><span data-stu-id="365a9-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="365a9-132">X</span><span class="sxs-lookup"><span data-stu-id="365a9-132">X</span></span>     | <span data-ttu-id="365a9-133">X</span><span class="sxs-lookup"><span data-stu-id="365a9-133">X</span></span>       |



 

<span data-ttu-id="365a9-134">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="365a9-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="365a9-135">Vertice</span><span class="sxs-lookup"><span data-stu-id="365a9-135">Vertex</span></span> | <span data-ttu-id="365a9-136">Hull</span><span class="sxs-lookup"><span data-stu-id="365a9-136">Hull</span></span> | <span data-ttu-id="365a9-137">Dominio</span><span class="sxs-lookup"><span data-stu-id="365a9-137">Domain</span></span> | <span data-ttu-id="365a9-138">Geometria</span><span class="sxs-lookup"><span data-stu-id="365a9-138">Geometry</span></span> | <span data-ttu-id="365a9-139">Pixel</span><span class="sxs-lookup"><span data-stu-id="365a9-139">Pixel</span></span> | <span data-ttu-id="365a9-140">Calcolo</span><span class="sxs-lookup"><span data-stu-id="365a9-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="365a9-141">X</span><span class="sxs-lookup"><span data-stu-id="365a9-141">X</span></span>      | <span data-ttu-id="365a9-142">X</span><span class="sxs-lookup"><span data-stu-id="365a9-142">X</span></span>    | <span data-ttu-id="365a9-143">X</span><span class="sxs-lookup"><span data-stu-id="365a9-143">X</span></span>      | <span data-ttu-id="365a9-144">X</span><span class="sxs-lookup"><span data-stu-id="365a9-144">X</span></span>        | <span data-ttu-id="365a9-145">X</span><span class="sxs-lookup"><span data-stu-id="365a9-145">X</span></span>     | <span data-ttu-id="365a9-146">X</span><span class="sxs-lookup"><span data-stu-id="365a9-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="365a9-147">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="365a9-147">Minimum Shader Model</span></span>

<span data-ttu-id="365a9-148">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="365a9-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="365a9-149">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="365a9-149">Shader Model</span></span>                                              | <span data-ttu-id="365a9-150">Supportato</span><span class="sxs-lookup"><span data-stu-id="365a9-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="365a9-151">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="365a9-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="365a9-152">sì</span><span class="sxs-lookup"><span data-stu-id="365a9-152">yes</span></span>       |
| [<span data-ttu-id="365a9-153">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="365a9-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="365a9-154">no</span><span class="sxs-lookup"><span data-stu-id="365a9-154">no</span></span>        |
| [<span data-ttu-id="365a9-155">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="365a9-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="365a9-156">no</span><span class="sxs-lookup"><span data-stu-id="365a9-156">no</span></span>        |
| [<span data-ttu-id="365a9-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="365a9-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="365a9-158">no</span><span class="sxs-lookup"><span data-stu-id="365a9-158">no</span></span>        |
| [<span data-ttu-id="365a9-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="365a9-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="365a9-160">no</span><span class="sxs-lookup"><span data-stu-id="365a9-160">no</span></span>        |
| [<span data-ttu-id="365a9-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="365a9-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="365a9-162">no</span><span class="sxs-lookup"><span data-stu-id="365a9-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="365a9-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="365a9-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="365a9-164">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="365a9-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





