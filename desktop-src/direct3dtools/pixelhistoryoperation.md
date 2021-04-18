---
description: Rappresenta le informazioni sulla cronologia dei pixel.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixelHistoryOperation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304046"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span data-ttu-id="323ad-103"><span id="vspixengine.pixelhistoryoperation"></span>Struttura PixelHistoryOperation</span><span class="sxs-lookup"><span data-stu-id="323ad-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation structure</span></span>

<span data-ttu-id="323ad-104">Rappresenta le informazioni sulla cronologia dei pixel.</span><span class="sxs-lookup"><span data-stu-id="323ad-104">Represents information about pixel history.</span></span>

## <a name="syntax"></a><span data-ttu-id="323ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="323ad-105">Syntax</span></span>


```C++
} PixelHistoryOperation;
```

## <a name="members"></a><span data-ttu-id="323ad-106">Members</span><span class="sxs-lookup"><span data-stu-id="323ad-106">Members</span></span>

<span data-ttu-id="323ad-107">**Eid**</span><span class="sxs-lookup"><span data-stu-id="323ad-107">**eid**</span></span>  
<span data-ttu-id="323ad-108">ID dell'evento di grafica associato a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="323ad-108">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="323ad-109">**PCP**</span><span class="sxs-lookup"><span data-stu-id="323ad-109">**PCP**</span></span>  
<span data-ttu-id="323ad-110">Chiamate compresse associate a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="323ad-110">Packed calls associated with this operation.</span></span>

<span data-ttu-id="323ad-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="323ad-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="323ad-112">Destinazione di rendering originariamente associata (all'interno dell'applicazione acquisita) con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="323ad-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="323ad-113">**iPrim**</span><span class="sxs-lookup"><span data-stu-id="323ad-113">**iPrim**</span></span>  
<span data-ttu-id="323ad-114">Indice della primitiva effettiva associata all'operazione.</span><span class="sxs-lookup"><span data-stu-id="323ad-114">The index of the actual primitive associated witht his operation.</span></span>

<span data-ttu-id="323ad-115">**numPrims**</span><span class="sxs-lookup"><span data-stu-id="323ad-115">**numPrims**</span></span>  
<span data-ttu-id="323ad-116">Numero totale di primitive associate a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="323ad-116">The total number of primitives associated with this operation.</span></span>

<span data-ttu-id="323ad-117">**numVertsPerPrim**</span><span class="sxs-lookup"><span data-stu-id="323ad-117">**numVertsPerPrim**</span></span>  
<span data-ttu-id="323ad-118">Numero di vertici per primitive.</span><span class="sxs-lookup"><span data-stu-id="323ad-118">The number of vertices per primitive.</span></span>

<span data-ttu-id="323ad-119">**iInstance**</span><span class="sxs-lookup"><span data-stu-id="323ad-119">**iInstance**</span></span>  
<span data-ttu-id="323ad-120">Quando si esegue il rendering di istanze, il numero di istanza dell'istanza effettiva associata a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="323ad-120">When rendering instances, the instance number of the actual instance associated with this operation.</span></span>

<span data-ttu-id="323ad-121">**iInstanceCount**</span><span class="sxs-lookup"><span data-stu-id="323ad-121">**iInstanceCount**</span></span>  
<span data-ttu-id="323ad-122">Quando si esegue il rendering di istanze, il numero totale di istanze associate a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="323ad-122">When rendering instances, the total number of instances associated with this operation.</span></span>

<span data-ttu-id="323ad-123">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="323ad-123">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="323ad-124">true se l'assembler di input genera gli ID istanza; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="323ad-124">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="323ad-125">**flags**</span><span class="sxs-lookup"><span data-stu-id="323ad-125">**flags**</span></span>  
<span data-ttu-id="323ad-126">Combinazione di valori PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="323ad-126">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="323ad-127">Per ulteriori informazioni, vedere l'enumerazione PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="323ad-127">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="323ad-128">**pVSFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-128">**pVSFile**</span></span>  
<span data-ttu-id="323ad-129">FILEPTR per il flusso di byte pixel shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-129">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="323ad-130">Questa operazione viene passata di nuovo per eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="323ad-130">This is passed back in order to debug.</span></span>

<span data-ttu-id="323ad-131">**pGSFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-131">**pGSFile**</span></span>  
<span data-ttu-id="323ad-132">FILEPTR per il flusso di byte geometry shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-132">A FILEPTR for the geometry shader byte stream.</span></span> <span data-ttu-id="323ad-133">Questa operazione viene passata di nuovo per eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="323ad-133">This is passed back in order to debug.</span></span>

<span data-ttu-id="323ad-134">**pPSFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-134">**pPSFile**</span></span>  
<span data-ttu-id="323ad-135">FILEPTR per il flusso di byte pixel shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-135">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="323ad-136">Questa operazione viene passata di nuovo per eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="323ad-136">This is passed back in order to debug.</span></span>

<span data-ttu-id="323ad-137">**pHSFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-137">**pHSFile**</span></span>  
<span data-ttu-id="323ad-138">FILEPTR per il flusso di byte Hull shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-138">A FILEPTR for the hull shader byte stream.</span></span> <span data-ttu-id="323ad-139">Questa operazione viene passata di nuovo per eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="323ad-139">This is passed back in order to debug.</span></span>

<span data-ttu-id="323ad-140">**pDSFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-140">**pDSFile**</span></span>  
<span data-ttu-id="323ad-141">FILEPTR per il flusso di byte del dominio shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-141">A FILEPTR for the domain shader byte stream.</span></span> <span data-ttu-id="323ad-142">Questa operazione viene passata di nuovo per eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="323ad-142">This is passed back in order to debug.</span></span>

<span data-ttu-id="323ad-143">**pCSFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-143">**pCSFile**</span></span>  
<span data-ttu-id="323ad-144">FILEPTR per il flusso di byte compute shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-144">A FILEPTR for the compute shader byte stream.</span></span> <span data-ttu-id="323ad-145">Questa operazione viene passata di nuovo per eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="323ad-145">This is passed back in order to debug.</span></span>

<span data-ttu-id="323ad-146">**VertexShaderFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-146">**VertexShaderFile**</span></span>  
<span data-ttu-id="323ad-147">Stringa COM contenente il percorso del file di origine del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-147">A COM string containing the filepath of the vertex shader source file.</span></span>

<span data-ttu-id="323ad-148">**PixelShaderFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-148">**PixelShaderFile**</span></span>  
<span data-ttu-id="323ad-149">Stringa COM contenente il percorso del file di origine del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-149">A COM string containing the filepath of the pixel shader source file.</span></span>

<span data-ttu-id="323ad-150">**GeometryShaderFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-150">**GeometryShaderFile**</span></span>  
<span data-ttu-id="323ad-151">Stringa COM contenente il percorso del file di origine geometry shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-151">A COM string containing the filepath of the geometry shader source file.</span></span>

<span data-ttu-id="323ad-152">**HullShaderFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-152">**HullShaderFile**</span></span>  
<span data-ttu-id="323ad-153">Stringa COM contenente il percorso del file di origine Hull shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-153">A COM string containing the filepath of the hull shader source file.</span></span>

<span data-ttu-id="323ad-154">**DomainShaderFile**</span><span class="sxs-lookup"><span data-stu-id="323ad-154">**DomainShaderFile**</span></span>  
<span data-ttu-id="323ad-155">Stringa COM contenente il percorso del file di origine del Domain shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-155">A COM string containing the filepath of the domain shader source file.</span></span>

<span data-ttu-id="323ad-156">**psRed**</span><span class="sxs-lookup"><span data-stu-id="323ad-156">**psRed**</span></span>  
<span data-ttu-id="323ad-157">Output pixel shader: valore del componente colore rosso.</span><span class="sxs-lookup"><span data-stu-id="323ad-157">Pixel shader output: value of red color component.</span></span>

<span data-ttu-id="323ad-158">**psGreen**</span><span class="sxs-lookup"><span data-stu-id="323ad-158">**psGreen**</span></span>  
<span data-ttu-id="323ad-159">Output pixel shader: valore del componente colore verde.</span><span class="sxs-lookup"><span data-stu-id="323ad-159">Pixel shader output: value of green color component.</span></span>

<span data-ttu-id="323ad-160">**psBlue**</span><span class="sxs-lookup"><span data-stu-id="323ad-160">**psBlue**</span></span>  
<span data-ttu-id="323ad-161">Output pixel shader: valore del componente colore blu</span><span class="sxs-lookup"><span data-stu-id="323ad-161">Pixel shader output: value of blue color component</span></span>

<span data-ttu-id="323ad-162">**psAlpha**</span><span class="sxs-lookup"><span data-stu-id="323ad-162">**psAlpha**</span></span>  
<span data-ttu-id="323ad-163">Output pixel shader: valore del componente colore alfa</span><span class="sxs-lookup"><span data-stu-id="323ad-163">Pixel shader output: value of alpha color component</span></span>

<span data-ttu-id="323ad-164">**LabelPSRed**</span><span class="sxs-lookup"><span data-stu-id="323ad-164">**LabelPSRed**</span></span>  
<span data-ttu-id="323ad-165">Stringa COM contenente il nome dell'etichetta associata al componente colore rosso dell'output del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-165">A COM string containing the name of the label associated with the red color component of the pixel shader output.</span></span>

<span data-ttu-id="323ad-166">**LabelPSGreen**</span><span class="sxs-lookup"><span data-stu-id="323ad-166">**LabelPSGreen**</span></span>  
<span data-ttu-id="323ad-167">Stringa COM contenente il nome dell'etichetta associata al componente colore verde dell'output del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-167">A COM string containing the name of the label associated with the green color component of the pixel shader output.</span></span>

<span data-ttu-id="323ad-168">**LabelPSBlue**</span><span class="sxs-lookup"><span data-stu-id="323ad-168">**LabelPSBlue**</span></span>  
<span data-ttu-id="323ad-169">Stringa COM contenente il nome dell'etichetta associata al componente colore blu dell'output del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-169">A COM string containing the name of the label associated with the blue color component of the pixel shader output.</span></span>

<span data-ttu-id="323ad-170">**LabelPSAlpha**</span><span class="sxs-lookup"><span data-stu-id="323ad-170">**LabelPSAlpha**</span></span>  
<span data-ttu-id="323ad-171">Stringa COM contenente il nome dell'etichetta associata al componente colore alfa dell'output del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="323ad-171">A COM string containing the name of the label associated with the alpha color component of the pixel shader output.</span></span>

<span data-ttu-id="323ad-172">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="323ad-172">**pixelKillReason**</span></span>  
<span data-ttu-id="323ad-173">Output pixel shader: motivo per cui l'output del pixel è stato terminato.</span><span class="sxs-lookup"><span data-stu-id="323ad-173">Pixel shader output: reason the pixel output was killed.</span></span>

<span data-ttu-id="323ad-174">**pixelOccluded**</span><span class="sxs-lookup"><span data-stu-id="323ad-174">**pixelOccluded**</span></span>  
<span data-ttu-id="323ad-175">true se il pixel è nascosto; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="323ad-175">true if the pixel is occluded; otherwise, false.</span></span>

<span data-ttu-id="323ad-176">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="323ad-176">**fbRed**</span></span>  
<span data-ttu-id="323ad-177">Framebuffer: valore del componente colore rosso del framebuffer prima che venga eseguito il merge pixel shader output.</span><span class="sxs-lookup"><span data-stu-id="323ad-177">Framebuffer: value of red color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="323ad-178">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="323ad-178">**fbGreen**</span></span>  
<span data-ttu-id="323ad-179">Framebuffer: valore del componente colore verde del framebuffer prima che venga eseguito il merge pixel shader output.</span><span class="sxs-lookup"><span data-stu-id="323ad-179">Framebuffer: value of green color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="323ad-180">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="323ad-180">**fbBlue**</span></span>  
<span data-ttu-id="323ad-181">Framebuffer: valore del componente colore blu del framebuffer prima che venga eseguito il merge pixel shader output.</span><span class="sxs-lookup"><span data-stu-id="323ad-181">Framebuffer: value of blue color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="323ad-182">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="323ad-182">**fbAlpha**</span></span>  
<span data-ttu-id="323ad-183">Framebuffer: valore del componente a colori alfa del framebuffer prima del merge pixel shader output.</span><span class="sxs-lookup"><span data-stu-id="323ad-183">Framebuffer: value of alpha color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="323ad-184">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="323ad-184">**LabelFBRed**</span></span>  
<span data-ttu-id="323ad-185">Stringa COM contenente il nome dell'etichetta associata al componente colore rosso del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="323ad-185">A COM string containing the name of the label associated with the red color component of the framebuffer.</span></span>

<span data-ttu-id="323ad-186">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="323ad-186">**LabelFBGreen**</span></span>  
<span data-ttu-id="323ad-187">Stringa COM contenente il nome dell'etichetta associata al componente colore verde del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="323ad-187">A COM string containing the name of the label associated with the green color component of the framebuffer.</span></span>

<span data-ttu-id="323ad-188">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="323ad-188">**LabelFBBlue**</span></span>  
<span data-ttu-id="323ad-189">Stringa COM contenente il nome dell'etichetta associata al componente colore blu del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="323ad-189">A COM string containing the name of the label associated with the blue color component of the framebuffer.</span></span>

<span data-ttu-id="323ad-190">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="323ad-190">**LabelFBAlpha**</span></span>  
<span data-ttu-id="323ad-191">Stringa COM contenente il nome dell'etichetta associata al componente colore alfa del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="323ad-191">A COM string containing the name of the label associated with the alpha color component of the framebuffer.</span></span>

<span data-ttu-id="323ad-192">**topologia**</span><span class="sxs-lookup"><span data-stu-id="323ad-192">**topology**</span></span>  
<span data-ttu-id="323ad-193">Topologia dei vertici delle chiamate di richiamo (elenco di triangolo, striscia del triangolo e così via).</span><span class="sxs-lookup"><span data-stu-id="323ad-193">The vertex topology of the draw calls (triangle list, triangle strip, etc).</span></span>

<span data-ttu-id="323ad-194">**vertici**</span><span class="sxs-lookup"><span data-stu-id="323ad-194">**vertices**</span></span>  
<span data-ttu-id="323ad-195">Stringa COM contenente il buffer dei vertici a partire da questa primitiva.</span><span class="sxs-lookup"><span data-stu-id="323ad-195">A COM string containing the vertex buffer starting at this primitive.</span></span> <span data-ttu-id="323ad-196">Il buffer dei vertici segue il formato di layout di input specificato nella fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="323ad-196">The vertex buffer follows the input layout format specified in the pipeline stage.</span></span>

<span data-ttu-id="323ad-197">**vertexSize**</span><span class="sxs-lookup"><span data-stu-id="323ad-197">**vertexSize**</span></span>  
<span data-ttu-id="323ad-198">Dimensioni in byte di un singolo vertice.</span><span class="sxs-lookup"><span data-stu-id="323ad-198">The size of a single vertex in bytes.</span></span>

<span data-ttu-id="323ad-199">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="323ad-199">**InputLayout**</span></span>  
<span data-ttu-id="323ad-200">Stringa COM contenente una sequenza di strutture InputLayoutStruct associate alla chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="323ad-200">A COM string containing a sequence of InputLayoutStruct structures associated with the draw call.</span></span>

<span data-ttu-id="323ad-201">**HResult**</span><span class="sxs-lookup"><span data-stu-id="323ad-201">**HResult**</span></span>  
<span data-ttu-id="323ad-202">HRESULT DirectX.</span><span class="sxs-lookup"><span data-stu-id="323ad-202">The DirectX Hresult.</span></span> <span data-ttu-id="323ad-203">In caso di problemi, questo può essere usato per visualizzare l'errore.</span><span class="sxs-lookup"><span data-stu-id="323ad-203">In the event of a problem this can be used to display the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="323ad-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="323ad-204">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="323ad-205">Intestazione</span><span class="sxs-lookup"><span data-stu-id="323ad-205">Header</span></span></p></td><td><span data-ttu-id="323ad-206">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="323ad-206">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



