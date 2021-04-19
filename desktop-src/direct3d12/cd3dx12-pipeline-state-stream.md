---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
description: Struttura di supporto per la creazione e l'utilizzo degli Stati della pipeline di calcolo e di grafica tramite un'interfaccia combinata. Vedere D3D12 \_ Graphics \_ pipeline \_ state \_ DESC e D3D12 \_ Compute \_ pipeline \_ state \_ desc. | Struttura CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d52b9090fa1d3870027bbe360164627472c039e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322220"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a><span data-ttu-id="d15da-106">\_Struttura del \_ flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="d15da-106">CD3DX12\_PIPELINE\_STATE\_STREAM structure</span></span>

<span data-ttu-id="d15da-107">Struttura di supporto per la creazione e l'utilizzo degli Stati della pipeline di calcolo e di grafica tramite un'interfaccia combinata.</span><span class="sxs-lookup"><span data-stu-id="d15da-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="d15da-108">Vedere [**D3D12 \_ Graphics \_ pipeline \_ state \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12 \_ Compute \_ pipeline \_ state \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="d15da-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="d15da-109">\_ \_ \_ Il flusso di stato della pipeline CD3DX12 supporta Windows 10 Creators Update e versioni successive, ma non supporta le nuove funzionalità di Fall Creators Update, ad esempio Visualizza istanze.</span><span class="sxs-lookup"><span data-stu-id="d15da-109">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer but doesn't support new features of the Fall Creators update, such as view instancing.</span></span> <span data-ttu-id="d15da-110">Per supportare le funzionalità dell'aggiornamento Fall Creators, usare invece [**\_ lo stato della pipeline CD3DX12 \_ \_ stream1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .</span><span class="sxs-lookup"><span data-stu-id="d15da-110">To support features of the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="d15da-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d15da-111">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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



## <a name="members"></a><span data-ttu-id="d15da-112">Members</span><span class="sxs-lookup"><span data-stu-id="d15da-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="d15da-113">**\_Flusso di stato della pipeline CD3DX12 \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="d15da-113">**CD3DX12\_PIPELINE\_STATE\_STREAM()**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-114">Crea una nuova istanza non inizializzata di un \_ flusso di stato della pipeline CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d15da-114">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-115">**\_Flusso di stato della pipeline CD3DX12 \_ \_ (const D3D12 \_ GRAPHICS \_ pipeline \_ state \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="d15da-115">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-116">Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ \_ , inizializzata con i valori copiati da una struttura del flusso di **\_ stato della pipeline \_ \_ CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="d15da-116">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-117">**\_Flusso di stato della pipeline CD3DX12 \_ \_ (const D3D12 \_ compute \_ \_ state pipeline \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="d15da-117">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-118">Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ \_ , inizializzata con i valori copiati da una struttura del flusso di **\_ stato della pipeline \_ \_ CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="d15da-118">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-119">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="d15da-119">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-120">Restituisce il contenuto dell' \_ oggetto flusso di stato della pipeline CD3DX12 \_ \_ come \_ \_ struttura di stato della pipeline grafica D3D12 \_ \_ per valore.</span><span class="sxs-lookup"><span data-stu-id="d15da-120">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="d15da-121">Si noti che \_ lo \_ stato della pipeline grafica D3D12 \_ \_ DESC non include il membro **CS** , quindi questo valore viene perso nella conversione.</span><span class="sxs-lookup"><span data-stu-id="d15da-121">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-122">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="d15da-122">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-123">Restituisce il contenuto dell' \_ oggetto flusso di stato della pipeline CD3DX12 \_ \_ come \_ \_ \_ struttura desc di stato della pipeline di calcolo D3D12 \_ per valore.</span><span class="sxs-lookup"><span data-stu-id="d15da-123">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="d15da-124">Si noti che \_ \_ \_ la descrizione dello stato della pipeline di calcolo D3D12 \_ non include i membri **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** o **SampleMask** , quindi questi valori vengono persi nella conversione.</span><span class="sxs-lookup"><span data-stu-id="d15da-124">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-125">**Flag**</span><span class="sxs-lookup"><span data-stu-id="d15da-125">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-126">Vengono descritti i flag di stato della pipeline, che controllano le funzionalità di, ad esempio "strumento Debug".</span><span class="sxs-lookup"><span data-stu-id="d15da-126">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="d15da-127">**Node mask**</span><span class="sxs-lookup"><span data-stu-id="d15da-127">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-128">Viene descritta la maschera del nodo dello stato della pipeline, che consente di identificare i nodi (schede fisiche del dispositivo) a cui si applica il PSO negli scenari con più adapter. ogni bit nella maschera corrisponde a un singolo nodo.</span><span class="sxs-lookup"><span data-stu-id="d15da-128">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="d15da-129">Per gli scenari a singolo adattatore, impostare questo valore su 0.</span><span class="sxs-lookup"><span data-stu-id="d15da-129">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-130">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="d15da-130">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-131">Descrive la firma radice.</span><span class="sxs-lookup"><span data-stu-id="d15da-131">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-132">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="d15da-132">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-133">Descrive il formato del buffer di input per la fase input-assembler</span><span class="sxs-lookup"><span data-stu-id="d15da-133">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="d15da-134">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="d15da-134">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-135">Descrive il valore di indice speciale del buffer di input che indica una riduzione (discontinuità) quando si utilizza la topologia a strisce triangolare.</span><span class="sxs-lookup"><span data-stu-id="d15da-135">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-136">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="d15da-136">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-137">Descrive la topologia primitiva e il relativo ordine.</span><span class="sxs-lookup"><span data-stu-id="d15da-137">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-138">**VS**</span><span class="sxs-lookup"><span data-stu-id="d15da-138">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-139">Descrive il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="d15da-139">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-140">**GS**</span><span class="sxs-lookup"><span data-stu-id="d15da-140">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-141">Descrive il geometry shader.</span><span class="sxs-lookup"><span data-stu-id="d15da-141">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-142">**StreamOutput**</span><span class="sxs-lookup"><span data-stu-id="d15da-142">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-143">Descrive il buffer di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="d15da-143">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-144">**HS**</span><span class="sxs-lookup"><span data-stu-id="d15da-144">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-145">Descrive Hull shader.</span><span class="sxs-lookup"><span data-stu-id="d15da-145">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-146">**DS**</span><span class="sxs-lookup"><span data-stu-id="d15da-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-147">Descrive il Domain shader.</span><span class="sxs-lookup"><span data-stu-id="d15da-147">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-148">**PS**</span><span class="sxs-lookup"><span data-stu-id="d15da-148">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-149">Descrive il pixel shader.</span><span class="sxs-lookup"><span data-stu-id="d15da-149">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-150">**CS**</span><span class="sxs-lookup"><span data-stu-id="d15da-150">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-151">Descrive il compute shader.</span><span class="sxs-lookup"><span data-stu-id="d15da-151">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-152">**BlendState**</span><span class="sxs-lookup"><span data-stu-id="d15da-152">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-153">Descrive lo stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="d15da-153">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-154">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="d15da-154">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-155">Descrive lo stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="d15da-155">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-156">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="d15da-156">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-157">Descrive il formato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="d15da-157">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-158">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="d15da-158">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-159">Descrive lo stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15da-159">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-160">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="d15da-160">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-161">Descrive i formati della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d15da-161">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-162">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="d15da-162">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-163">Descrive il numero di campioni e la qualità.</span><span class="sxs-lookup"><span data-stu-id="d15da-163">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-164">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="d15da-164">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-165">Viene descritta la maschera di esempio utilizzata con lo stato Blend.</span><span class="sxs-lookup"><span data-stu-id="d15da-165">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-166">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="d15da-166">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="d15da-167">Descrive un oggetto PSO memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="d15da-167">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d15da-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="d15da-168">Remarks</span></span>

<span data-ttu-id="d15da-169">\_ \_ \_ Il flusso di stato della pipeline CD3DX12 supporta Windows 10 Creators Update e versioni successive, ma non supporta i tipi di sottooggetti aggiunti in Windows 10 Fall Creators Update, ad esempio per le istanze di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15da-169">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer, but doesn not support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="d15da-170">Per supportare i tipi di sottooggetti aggiunti nell'aggiornamento Fall Creators, usare [**invece \_ \_ lo stato \_ della pipeline CD3DX12 stream1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .</span><span class="sxs-lookup"><span data-stu-id="d15da-170">To support subobject types added in the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

<span data-ttu-id="d15da-171">Le variabili membro accessibili di questa struttura sono tutti typedef del \_ \_ modello di sottooggetto flusso di stato della pipeline CD3DX12 \_ \_ , che combina i dati del marcatore del tipo di sottooggetto e i dati di sottooggetto in un singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="d15da-171">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="d15da-172">Questi typedef sono:</span><span class="sxs-lookup"><span data-stu-id="d15da-172">Those typedefs are:</span></span>

<span data-ttu-id="d15da-173"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="d15da-173"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d15da-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d15da-174">Requirements</span></span>



| <span data-ttu-id="d15da-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="d15da-175">Requirement</span></span> | <span data-ttu-id="d15da-176">Valore</span><span class="sxs-lookup"><span data-stu-id="d15da-176">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d15da-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d15da-177">Header</span></span><br/> | <dl> <span data-ttu-id="d15da-178"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d15da-178"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d15da-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d15da-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d15da-180">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="d15da-180">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d15da-181">**\_ \_ Stream1 stato pipeline \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="d15da-181">**CD3DX12\_PIPELINE\_STATE\_STREAM1**</span></span>](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[<span data-ttu-id="d15da-182">**\_ \_ \_ Descrizione dello stato della pipeline grafica D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="d15da-182">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="d15da-183">**\_ \_ Desc stato della pipeline di calcolo \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="d15da-183">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





