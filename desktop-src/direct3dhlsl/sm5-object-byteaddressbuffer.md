---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- HLSL ByteAddressBuffer
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976826"
---
# <a name="byteaddressbuffer"></a><span data-ttu-id="c4f03-104">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="c4f03-104">ByteAddressBuffer</span></span>

<span data-ttu-id="c4f03-105">Buffer di sola lettura indicizzato in byte.</span><span class="sxs-lookup"><span data-stu-id="c4f03-105">A read-only buffer that is indexed in bytes.</span></span>



| <span data-ttu-id="c4f03-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="c4f03-106">Method</span></span>                                                              | <span data-ttu-id="c4f03-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4f03-107">Description</span></span>                   |
|---------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="c4f03-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="c4f03-108">**GetDimensions**</span></span>](sm5-object-byteaddressbuffer-getdimensions.md) | <span data-ttu-id="c4f03-109">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4f03-109">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="c4f03-110">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="c4f03-110">**Load**</span></span>](byteaddressbuffer-load.md)                              | <span data-ttu-id="c4f03-111">Ottiene un valore.</span><span class="sxs-lookup"><span data-stu-id="c4f03-111">Gets one value.</span></span>               |
| [<span data-ttu-id="c4f03-112">**Load2**</span><span class="sxs-lookup"><span data-stu-id="c4f03-112">**Load2**</span></span>](byteaddressbuffer-load2.md)                            | <span data-ttu-id="c4f03-113">Ottiene due valori.</span><span class="sxs-lookup"><span data-stu-id="c4f03-113">Gets two values.</span></span>              |
| [<span data-ttu-id="c4f03-114">**Load3**</span><span class="sxs-lookup"><span data-stu-id="c4f03-114">**Load3**</span></span>](byteaddressbuffer-load3.md)                            | <span data-ttu-id="c4f03-115">Ottiene tre valori.</span><span class="sxs-lookup"><span data-stu-id="c4f03-115">Gets three values.</span></span>            |
| [<span data-ttu-id="c4f03-116">**Load4**</span><span class="sxs-lookup"><span data-stu-id="c4f03-116">**Load4**</span></span>](byteaddressbuffer-load4.md)                            | <span data-ttu-id="c4f03-117">Ottiene quattro valori.</span><span class="sxs-lookup"><span data-stu-id="c4f03-117">Gets four values.</span></span>             |



 

<span data-ttu-id="c4f03-118">È possibile utilizzare il tipo di oggetto **ByteAddressBuffer** quando si utilizzano buffer non elaborati.</span><span class="sxs-lookup"><span data-stu-id="c4f03-118">You can use the **ByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="c4f03-119">Per altre informazioni sulla visualizzazione non elaborata dei buffer, vedere [visualizzazioni non elaborate dei buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="c4f03-119">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c4f03-120">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c4f03-120">Minimum Shader Model</span></span>

<span data-ttu-id="c4f03-121">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c4f03-121">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="c4f03-122">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c4f03-122">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="c4f03-123">Supportato</span><span class="sxs-lookup"><span data-stu-id="c4f03-123">Supported</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c4f03-124">[Shader Model 5](d3d11-graphics-reference-sm5.md) e High shader Models Shader Model [4](dx-graphics-hlsl-sm4.md) (disponibile tramite l'API Direct3D 11 usando il livello di funzionalità 10,0 o 10,1 ([**D3D \_ feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sui dispositivi che supportano compute shader.</span><span class="sxs-lookup"><span data-stu-id="c4f03-124">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="c4f03-125">Per altre informazioni sul supporto di compute shader nell'hardware di livello inferiore, vedere [Compute Shaders su hardware di livello inferiore](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).</span><span class="sxs-lookup"><span data-stu-id="c4f03-125">For more info about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="c4f03-126">sì</span><span class="sxs-lookup"><span data-stu-id="c4f03-126">yes</span></span>       |



 

<span data-ttu-id="c4f03-127">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4f03-127">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c4f03-128">Vertice</span><span class="sxs-lookup"><span data-stu-id="c4f03-128">Vertex</span></span> | <span data-ttu-id="c4f03-129">Hull</span><span class="sxs-lookup"><span data-stu-id="c4f03-129">Hull</span></span> | <span data-ttu-id="c4f03-130">Dominio</span><span class="sxs-lookup"><span data-stu-id="c4f03-130">Domain</span></span> | <span data-ttu-id="c4f03-131">Geometria</span><span class="sxs-lookup"><span data-stu-id="c4f03-131">Geometry</span></span> | <span data-ttu-id="c4f03-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="c4f03-132">Pixel</span></span> | <span data-ttu-id="c4f03-133">Calcolo</span><span class="sxs-lookup"><span data-stu-id="c4f03-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c4f03-134">x</span><span class="sxs-lookup"><span data-stu-id="c4f03-134">x</span></span>      | <span data-ttu-id="c4f03-135">x</span><span class="sxs-lookup"><span data-stu-id="c4f03-135">x</span></span>    | <span data-ttu-id="c4f03-136">x</span><span class="sxs-lookup"><span data-stu-id="c4f03-136">x</span></span>      | <span data-ttu-id="c4f03-137">x</span><span class="sxs-lookup"><span data-stu-id="c4f03-137">x</span></span>        | <span data-ttu-id="c4f03-138">x</span><span class="sxs-lookup"><span data-stu-id="c4f03-138">x</span></span>     | <span data-ttu-id="c4f03-139">x</span><span class="sxs-lookup"><span data-stu-id="c4f03-139">x</span></span>       |



 

<span data-ttu-id="c4f03-140">Per ulteriori informazioni su un buffer degli indirizzi byte, vedere il [tipo di risorsa indirizzabile di byte](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="c4f03-140">For more info about a byte address buffer, see the [byte addressable resource type](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

<span data-ttu-id="c4f03-141">Shader Model 5 implementa anche un [buffer di indirizzi byte di lettura e scrittura](sm5-object-rwbyteaddressbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c4f03-141">Shader Model 5 also implements a [read-write byte address buffer](sm5-object-rwbyteaddressbuffer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c4f03-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4f03-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f03-143">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="c4f03-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

