---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
description: Struttura di supporto per la creazione e l'utilizzo degli Stati della pipeline di calcolo e di grafica tramite un'interfaccia combinata. Vedere D3D12 \_ Graphics \_ pipeline \_ state \_ DESC e D3D12 \_ Compute \_ pipeline \_ state \_ desc. | Struttura CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd04f58f4f123850c60b67ff9358f6f1f934373
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322219"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a><span data-ttu-id="1e43e-106">\_ \_ Struttura stream1 dello stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="1e43e-106">CD3DX12\_PIPELINE\_STATE\_STREAM1 structure</span></span>

<span data-ttu-id="1e43e-107">Struttura di supporto per la creazione e l'utilizzo degli Stati della pipeline di calcolo e di grafica tramite un'interfaccia combinata.</span><span class="sxs-lookup"><span data-stu-id="1e43e-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="1e43e-108">Vedere [**D3D12 \_ Graphics \_ pipeline \_ state \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12 \_ Compute \_ pipeline \_ state \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="1e43e-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="1e43e-109">\_ \_ Lo stato della pipeline CD3DX12 \_ stream1 supporta Windows 10 Fall Creators Update con nuove funzionalità, ad esempio Visualizza istanze.</span><span class="sxs-lookup"><span data-stu-id="1e43e-109">CD3DX12\_PIPELINE\_STATE\_STREAM1 supports the Windows 10 Fall Creators Update with new features such as view instancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e43e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e43e-110">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a><span data-ttu-id="1e43e-111">Members</span><span class="sxs-lookup"><span data-stu-id="1e43e-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e43e-112">**\_Stato della pipeline CD3DX12 \_ \_ stream1 ()**</span><span class="sxs-lookup"><span data-stu-id="1e43e-112">**CD3DX12\_PIPELINE\_STATE\_STREAM1()**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-113">Crea una nuova istanza non inizializzata di uno \_ stato della pipeline CD3DX12 \_ \_ stream1.</span><span class="sxs-lookup"><span data-stu-id="1e43e-113">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-114">**CD3DX12 \_ pipeline \_ state \_ stream1 (const D3D12 \_ GRAPHICS \_ pipeline \_ state \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="1e43e-114">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-115">Crea una nuova istanza di uno \_ stato della pipeline CD3DX12 \_ \_ stream1, inizializzata con i valori copiati da una struttura **CD3DX12 di stato della \_ pipeline \_ \_ stream1** .</span><span class="sxs-lookup"><span data-stu-id="1e43e-115">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-116">**\_Stato della pipeline CD3DX12 \_ \_ stream1 (const D3D12 \_ compute \_ pipeline \_ state \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="1e43e-116">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-117">Crea una nuova istanza di uno \_ stato della pipeline CD3DX12 \_ \_ stream1, inizializzata con i valori copiati da una struttura **CD3DX12 di stato della \_ pipeline \_ \_ stream1** .</span><span class="sxs-lookup"><span data-stu-id="1e43e-117">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-118">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="1e43e-118">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-119">Restituisce il contenuto dell' \_ \_ oggetto stream1 dello stato della pipeline CD3DX12 \_ come \_ \_ \_ struttura desc di stato della pipeline grafica D3D12 \_ per valore.</span><span class="sxs-lookup"><span data-stu-id="1e43e-119">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="1e43e-120">Si noti che \_ lo \_ stato della pipeline grafica D3D12 \_ \_ DESC non include il membro **CS** , quindi questo valore viene perso nella conversione.</span><span class="sxs-lookup"><span data-stu-id="1e43e-120">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-121">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="1e43e-121">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-122">Restituisce il contenuto dell' \_ \_ oggetto stream1 dello stato della pipeline CD3DX12 \_ come \_ \_ \_ struttura desc di stato della pipeline di calcolo D3D12 \_ per valore.</span><span class="sxs-lookup"><span data-stu-id="1e43e-122">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="1e43e-123">Si noti che \_ \_ \_ la descrizione dello stato della pipeline di calcolo D3D12 \_ non include i membri **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** o **SampleMask** , quindi questi valori vengono persi nella conversione.</span><span class="sxs-lookup"><span data-stu-id="1e43e-123">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-124">**Flag**</span><span class="sxs-lookup"><span data-stu-id="1e43e-124">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-125">Vengono descritti i flag di stato della pipeline, che controllano le funzionalità di, ad esempio "strumento Debug".</span><span class="sxs-lookup"><span data-stu-id="1e43e-125">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-126">**Node mask**</span><span class="sxs-lookup"><span data-stu-id="1e43e-126">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-127">Viene descritta la maschera del nodo dello stato della pipeline, che consente di identificare i nodi (schede fisiche del dispositivo) a cui si applica il PSO negli scenari con più adapter. ogni bit nella maschera corrisponde a un singolo nodo.</span><span class="sxs-lookup"><span data-stu-id="1e43e-127">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="1e43e-128">Per gli scenari a singolo adattatore, impostare questo valore su 0.</span><span class="sxs-lookup"><span data-stu-id="1e43e-128">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-129">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="1e43e-129">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-130">Descrive la firma radice.</span><span class="sxs-lookup"><span data-stu-id="1e43e-130">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-131">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="1e43e-131">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-132">Descrive il formato del buffer di input per la fase input-assembler</span><span class="sxs-lookup"><span data-stu-id="1e43e-132">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-133">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="1e43e-133">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-134">Descrive il valore di indice speciale del buffer di input che indica una riduzione (discontinuità) quando si utilizza la topologia a strisce triangolare.</span><span class="sxs-lookup"><span data-stu-id="1e43e-134">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-135">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="1e43e-135">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-136">Descrive la topologia primitiva e il relativo ordine.</span><span class="sxs-lookup"><span data-stu-id="1e43e-136">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-137">**VS**</span><span class="sxs-lookup"><span data-stu-id="1e43e-137">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-138">Descrive il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="1e43e-138">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-139">**GS**</span><span class="sxs-lookup"><span data-stu-id="1e43e-139">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-140">Descrive il geometry shader.</span><span class="sxs-lookup"><span data-stu-id="1e43e-140">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-141">**StreamOutput**</span><span class="sxs-lookup"><span data-stu-id="1e43e-141">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-142">Descrive il buffer di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="1e43e-142">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-143">**HS**</span><span class="sxs-lookup"><span data-stu-id="1e43e-143">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-144">Descrive Hull shader.</span><span class="sxs-lookup"><span data-stu-id="1e43e-144">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-145">**DS**</span><span class="sxs-lookup"><span data-stu-id="1e43e-145">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-146">Descrive il Domain shader.</span><span class="sxs-lookup"><span data-stu-id="1e43e-146">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-147">**PS**</span><span class="sxs-lookup"><span data-stu-id="1e43e-147">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-148">Descrive il pixel shader.</span><span class="sxs-lookup"><span data-stu-id="1e43e-148">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-149">**CS**</span><span class="sxs-lookup"><span data-stu-id="1e43e-149">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-150">Descrive il compute shader.</span><span class="sxs-lookup"><span data-stu-id="1e43e-150">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-151">**BlendState**</span><span class="sxs-lookup"><span data-stu-id="1e43e-151">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-152">Descrive lo stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="1e43e-152">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-153">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="1e43e-153">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-154">Descrive lo stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="1e43e-154">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-155">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="1e43e-155">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-156">Descrive il formato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="1e43e-156">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-157">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="1e43e-157">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-158">Descrive lo stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="1e43e-158">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-159">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="1e43e-159">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-160">Descrive i formati della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="1e43e-160">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-161">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="1e43e-161">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-162">Descrive il numero di campioni e la qualità.</span><span class="sxs-lookup"><span data-stu-id="1e43e-162">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-163">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="1e43e-163">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-164">Viene descritta la maschera di esempio utilizzata con lo stato Blend.</span><span class="sxs-lookup"><span data-stu-id="1e43e-164">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="1e43e-165">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="1e43e-165">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="1e43e-166">Descrive un oggetto PSO memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="1e43e-166">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e43e-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e43e-167">Remarks</span></span>

<span data-ttu-id="1e43e-168">[**CD3DX12 \_ Il \_ \_ flusso di stato della pipeline**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) supporta Windows 10 Fall Creators Update, ma non supporta i tipi di sottooggetti aggiunti in Windows 10 Fall Creators Update, ad esempio per le istanze di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1e43e-168">[**CD3DX12\_PIPELINE\_STATE\_STREAM**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) supports the Windows 10 Fall Creators Update, but doesn't support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="1e43e-169">Per supportare i nuovi tipi di sottooggetti, usare \_ \_ invece lo stato della pipeline CD3DX12 \_ stream1.</span><span class="sxs-lookup"><span data-stu-id="1e43e-169">To support the new subobject types, use CD3DX12\_PIPELINE\_STATE\_STREAM1 instead.</span></span>

<span data-ttu-id="1e43e-170">Le variabili membro accessibili di questa struttura sono tutti typedef del \_ \_ modello di sottooggetto flusso di stato della pipeline CD3DX12 \_ \_ , che combina i dati del marcatore del tipo di sottooggetto e i dati di sottooggetto in un singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="1e43e-170">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="1e43e-171">Questi typedef sono:</span><span class="sxs-lookup"><span data-stu-id="1e43e-171">Those typedefs are:</span></span>

<span data-ttu-id="1e43e-172"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="1e43e-172"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1e43e-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e43e-173">Requirements</span></span>



| <span data-ttu-id="1e43e-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e43e-174">Requirement</span></span> | <span data-ttu-id="1e43e-175">Valore</span><span class="sxs-lookup"><span data-stu-id="1e43e-175">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1e43e-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e43e-176">Header</span></span><br/> | <dl> <span data-ttu-id="1e43e-177"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e43e-177"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e43e-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e43e-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e43e-179">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="1e43e-179">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1e43e-180">**\_Flusso di \_ stato della pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="1e43e-180">**CD3DX12\_PIPELINE\_STATE\_STREAM**</span></span>](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[<span data-ttu-id="1e43e-181">**\_ \_ \_ Descrizione dello stato della pipeline grafica D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="1e43e-181">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="1e43e-182">**\_ \_ Desc stato della pipeline di calcolo \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="1e43e-182">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





