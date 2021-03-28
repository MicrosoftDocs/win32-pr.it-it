---
title: RWByteAddressBuffer
description: Un buffer di lettura/scrittura che indicizza in byte.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- HLSL RWByteAddressBuffer
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399053"
---
# <a name="rwbyteaddressbuffer"></a><span data-ttu-id="724fc-104">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="724fc-104">RWByteAddressBuffer</span></span>

<span data-ttu-id="724fc-105">Un buffer di lettura/scrittura che indicizza in byte.</span><span class="sxs-lookup"><span data-stu-id="724fc-105">A read/write buffer that indexes in bytes.</span></span>



| <span data-ttu-id="724fc-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="724fc-106">Method</span></span>                                                                                          | <span data-ttu-id="724fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="724fc-107">Description</span></span>                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="724fc-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="724fc-108">**GetDimensions**</span></span>](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | <span data-ttu-id="724fc-109">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="724fc-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="724fc-110">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="724fc-110">**InterlockedAdd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | <span data-ttu-id="724fc-111">Aggiunge, in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="724fc-111">Adds, atomically.</span></span>                   |
| [<span data-ttu-id="724fc-112">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="724fc-112">**InterlockedAnd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | <span data-ttu-id="724fc-113">E, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="724fc-113">ANDs, atomically.</span></span>                   |
| [<span data-ttu-id="724fc-114">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="724fc-114">**InterlockedCompareExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | <span data-ttu-id="724fc-115">Confronta e scambia, in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="724fc-115">Compares and exchanges, atomically.</span></span> |
| [<span data-ttu-id="724fc-116">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="724fc-116">**InterlockedCompareStore**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | <span data-ttu-id="724fc-117">Confronta e archivia in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="724fc-117">Compares and stores, atomically.</span></span>    |
| [<span data-ttu-id="724fc-118">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="724fc-118">**InterlockedExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | <span data-ttu-id="724fc-119">Scambi, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="724fc-119">Exchanges, atomically.</span></span>              |
| [<span data-ttu-id="724fc-120">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="724fc-120">**InterlockedMax**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | <span data-ttu-id="724fc-121">Trova il valore massimo, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="724fc-121">Finds the max, atomically.</span></span>          |
| [<span data-ttu-id="724fc-122">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="724fc-122">**InterlockedMin**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | <span data-ttu-id="724fc-123">Trovare il minimo, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="724fc-123">Find the min, atomically.</span></span>           |
| [<span data-ttu-id="724fc-124">**Interblocco**</span><span class="sxs-lookup"><span data-stu-id="724fc-124">**InterlockedOr**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | <span data-ttu-id="724fc-125">ORs, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="724fc-125">ORs, atomically.</span></span>                    |
| [<span data-ttu-id="724fc-126">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="724fc-126">**InterlockedXor**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | <span data-ttu-id="724fc-127">XOR, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="724fc-127">XORs, atomically.</span></span>                   |
| [<span data-ttu-id="724fc-128">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="724fc-128">**Load**</span></span>](rwbyteaddressbuffer-load.md)                                                        | <span data-ttu-id="724fc-129">Ottiene un valore.</span><span class="sxs-lookup"><span data-stu-id="724fc-129">Gets one value.</span></span>                     |
| [<span data-ttu-id="724fc-130">**Load2**</span><span class="sxs-lookup"><span data-stu-id="724fc-130">**Load2**</span></span>](rwbyteaddressbuffer-load2.md)                                                      | <span data-ttu-id="724fc-131">Ottiene due valori.</span><span class="sxs-lookup"><span data-stu-id="724fc-131">Gets two values.</span></span>                    |
| [<span data-ttu-id="724fc-132">**Load3**</span><span class="sxs-lookup"><span data-stu-id="724fc-132">**Load3**</span></span>](rwbyteaddressbuffer-load3.md)                                                      | <span data-ttu-id="724fc-133">Ottiene tre valori.</span><span class="sxs-lookup"><span data-stu-id="724fc-133">Gets three values.</span></span>                  |
| [<span data-ttu-id="724fc-134">**Load4**</span><span class="sxs-lookup"><span data-stu-id="724fc-134">**Load4**</span></span>](rwbyteaddressbuffer-load4.md)                                                      | <span data-ttu-id="724fc-135">Ottiene quattro valori.</span><span class="sxs-lookup"><span data-stu-id="724fc-135">Gets four values.</span></span>                   |
| [<span data-ttu-id="724fc-136">**Store**</span><span class="sxs-lookup"><span data-stu-id="724fc-136">**Store**</span></span>](sm5-object-rwbyteaddressbuffer-store.md)                                           | <span data-ttu-id="724fc-137">Imposta un valore.</span><span class="sxs-lookup"><span data-stu-id="724fc-137">Sets one value.</span></span>                     |
| [<span data-ttu-id="724fc-138">**Archivio2**</span><span class="sxs-lookup"><span data-stu-id="724fc-138">**Store2**</span></span>](sm5-object-rwbyteaddressbuffer-store2.md)                                         | <span data-ttu-id="724fc-139">Imposta due valori.</span><span class="sxs-lookup"><span data-stu-id="724fc-139">Sets two values.</span></span>                    |
| [<span data-ttu-id="724fc-140">**Store3**</span><span class="sxs-lookup"><span data-stu-id="724fc-140">**Store3**</span></span>](sm5-object-rwbyteaddressbuffer-store3.md)                                         | <span data-ttu-id="724fc-141">Imposta tre valori.</span><span class="sxs-lookup"><span data-stu-id="724fc-141">Sets three values.</span></span>                  |
| [<span data-ttu-id="724fc-142">**Store4**</span><span class="sxs-lookup"><span data-stu-id="724fc-142">**Store4**</span></span>](sm5-object-rwbyteaddressbuffer-store4.md)                                         | <span data-ttu-id="724fc-143">Imposta quattro valori.</span><span class="sxs-lookup"><span data-stu-id="724fc-143">Sets four values.</span></span>                   |



 

<span data-ttu-id="724fc-144">Gli oggetti RWByteAddressBuffer possono essere preceduti dalla classe di archiviazione **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="724fc-144">RWByteAddressBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="724fc-145">Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture.</span><span class="sxs-lookup"><span data-stu-id="724fc-145">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="724fc-146">Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica un UAV solo all'interno del gruppo corrente.</span><span class="sxs-lookup"><span data-stu-id="724fc-146">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="724fc-147">Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ R32 formato senza \_ \_ tipo.</span><span class="sxs-lookup"><span data-stu-id="724fc-147">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_R32\_TYPELESS format.</span></span>

<span data-ttu-id="724fc-148">Il UAV associato a questa risorsa deve essere stato creato con il [**\_ flag UAV del buffer D3D11 \_ \_ \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="724fc-148">The UAV bound to this resource must have been created with the [**D3D11\_BUFFER\_UAV\_FLAG\_RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="724fc-149">È possibile utilizzare il tipo di oggetto **RWByteAddressBuffer** quando si utilizzano buffer non elaborati.</span><span class="sxs-lookup"><span data-stu-id="724fc-149">You can use the **RWByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="724fc-150">Per altre informazioni sulla visualizzazione non elaborata dei buffer, vedere [visualizzazioni non elaborate dei buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="724fc-150">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="724fc-151">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="724fc-151">Minimum Shader Model</span></span>

<span data-ttu-id="724fc-152">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="724fc-152">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="724fc-153">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="724fc-153">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="724fc-154">Supportato</span><span class="sxs-lookup"><span data-stu-id="724fc-154">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="724fc-155">[Shader Model 5](d3d11-graphics-reference-sm5.md) e High shader Models Shader Model [4](dx-graphics-hlsl-sm4.md) (disponibile tramite l'API Direct3D 11 usando il livello di funzionalità 10,0 o 10,1 ([**D3D \_ feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sui dispositivi che supportano compute shader.</span><span class="sxs-lookup"><span data-stu-id="724fc-155">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="724fc-156">Per ulteriori informazioni sul supporto di compute shader nell'hardware di livello inferiore, vedere [Compute Shaders su hardware di livello inferiore](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).</span><span class="sxs-lookup"><span data-stu-id="724fc-156">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="724fc-157">sì</span><span class="sxs-lookup"><span data-stu-id="724fc-157">yes</span></span>       |



 

<span data-ttu-id="724fc-158">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="724fc-158">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="724fc-159">Vertice</span><span class="sxs-lookup"><span data-stu-id="724fc-159">Vertex</span></span> | <span data-ttu-id="724fc-160">Hull</span><span class="sxs-lookup"><span data-stu-id="724fc-160">Hull</span></span> | <span data-ttu-id="724fc-161">Dominio</span><span class="sxs-lookup"><span data-stu-id="724fc-161">Domain</span></span> | <span data-ttu-id="724fc-162">Geometria</span><span class="sxs-lookup"><span data-stu-id="724fc-162">Geometry</span></span> | <span data-ttu-id="724fc-163">Pixel</span><span class="sxs-lookup"><span data-stu-id="724fc-163">Pixel</span></span> | <span data-ttu-id="724fc-164">Calcolo</span><span class="sxs-lookup"><span data-stu-id="724fc-164">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="724fc-165">x</span><span class="sxs-lookup"><span data-stu-id="724fc-165">x</span></span>     | <span data-ttu-id="724fc-166">x</span><span class="sxs-lookup"><span data-stu-id="724fc-166">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="724fc-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="724fc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724fc-168">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="724fc-168">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

