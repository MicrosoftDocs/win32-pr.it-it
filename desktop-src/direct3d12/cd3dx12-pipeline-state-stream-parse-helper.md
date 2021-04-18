---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER (D3dx12. h)
description: Compila un \_ \_ \_ oggetto flusso di stato della pipeline CD3DX12 interno da dettagli di sottooggetti passati nelle funzioni membro corrispondenti. Questo struct implementa l'interfaccia ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322237"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a><span data-ttu-id="1f057-105">\_ \_ \_ \_ Struttura helper di analisi del flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="1f057-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_PARSE\_HELPER structure</span></span>

<span data-ttu-id="1f057-106">Compila un \_ \_ \_ oggetto flusso di stato della pipeline CD3DX12 interno da dettagli di sottooggetti passati nelle funzioni membro corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="1f057-106">Builds an internal CD3DX12\_PIPELINE\_STATE\_STREAM object from subobject details passed into the corresponding member functions.</span></span> <span data-ttu-id="1f057-107">Questo struct implementa l'interfaccia [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .</span><span class="sxs-lookup"><span data-stu-id="1f057-107">This struct implements the [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f057-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f057-108">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a><span data-ttu-id="1f057-109">Members</span><span class="sxs-lookup"><span data-stu-id="1f057-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f057-110">**PipelineStream**</span><span class="sxs-lookup"><span data-stu-id="1f057-110">**PipelineStream**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-111">Stato della [**pipeline CD3DX12 interno \_ \_ \_ stream1**](cd3dx12-pipeline-state-stream1.md).</span><span class="sxs-lookup"><span data-stu-id="1f057-111">The internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md).</span></span> <span data-ttu-id="1f057-112">Lo stato corrente rappresenta l'effetto cumulativo dei metodi di callback chiamati su questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="1f057-112">Its current state represents the cumulative effect of callback methods that have been called on this object.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-113">**FlagsCb ( \_ flag di stato della pipeline D3D12 \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="1f057-113">**FlagsCb(D3D12\_PIPELINE\_STATE\_FLAGS Flags)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-114">Inizializza il membro **Flags** di **PipelineStream** usando il valore del parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="1f057-114">Initializes the **Flags** member of **PipelineStream** using the value of the *Flags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-115">**NodeMaskCb (UINT node mask)**</span><span class="sxs-lookup"><span data-stu-id="1f057-115">**NodeMaskCb(UINT NodeMask)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-116">Inizializza il membro **node mask** di **PipelineStream** usando il valore del parametro *node mask* .</span><span class="sxs-lookup"><span data-stu-id="1f057-116">Initializes the **NodeMask** member of **PipelineStream** using the value of the *Nodemask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-117">**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**</span><span class="sxs-lookup"><span data-stu-id="1f057-117">**RootSignatureCb(ID3D12RootSignature\* pRootSignature)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-118">Inizializza il membro **pRootSignature** di **PipelineStream** usando il valore del parametro *pRootSignature* .</span><span class="sxs-lookup"><span data-stu-id="1f057-118">Initializes the **pRootSignature** member of **PipelineStream** using the value of the *pRootSignature* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-119">**InputLayoutCb (const D3D12 \_ input \_ LAYOUT \_ desc& InputLayout)**</span><span class="sxs-lookup"><span data-stu-id="1f057-119">**InputLayoutCb(const D3D12\_INPUT\_LAYOUT\_DESC& InputLayout)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-120">Inizializza il membro **InputLayout** di **PipelineStream** usando il valore del parametro *InputLayout* .</span><span class="sxs-lookup"><span data-stu-id="1f057-120">Initializes the **InputLayout** member of **PipelineStream** using the value of the *InputLayout* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-121">**IBStripCutValueCb (D3D12 \_ index \_ buffer \_ Strip \_ Cut \_ value IBStripCutValue)**</span><span class="sxs-lookup"><span data-stu-id="1f057-121">**IBStripCutValueCb(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE IBStripCutValue)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-122">Inizializza il membro **IBStripCutValue** di **PipelineStream** usando il valore del parametro *IBStripCutValue* .</span><span class="sxs-lookup"><span data-stu-id="1f057-122">Initializes the **IBStripCutValue** member of **PipelineStream** using the value of the *IBStripCutValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-123">**PrimitiveTopologyTypeCb ( \_ tipo di \_ topologia primitiva D3D12 \_ PrimitiveTopologyType)**</span><span class="sxs-lookup"><span data-stu-id="1f057-123">**PrimitiveTopologyTypeCb(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE PrimitiveTopologyType)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-124">Inizializza il membro **PrimitiveTopologyType** di **PipelineStream** usando il valore del parametro *PrimitiveTopologyType* .</span><span class="sxs-lookup"><span data-stu-id="1f057-124">Initializes the **PrimitiveTopologyType** member of **PipelineStream** using the value of the *PrimitiveTopologyType* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-125">**VSCb (const D3D12 \_ shader \_ BYTECODE& vs)**</span><span class="sxs-lookup"><span data-stu-id="1f057-125">**VSCb(const D3D12\_SHADER\_BYTECODE& VS)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-126">Inizializza il membro **vs** (Vertex shader) di **PipelineStream** usando il valore del parametro *vs* .</span><span class="sxs-lookup"><span data-stu-id="1f057-126">Initializes the **VS** (vertex shader) member of **PipelineStream** using the value of the *VS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-127">**GSCb (const D3D12 \_ shader \_ BYTECODE& GS)**</span><span class="sxs-lookup"><span data-stu-id="1f057-127">**GSCb(const D3D12\_SHADER\_BYTECODE& GS)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-128">Inizializza il membro **GS** (Geometry shader) di **PipelineStream** usando il valore del parametro *GS* .</span><span class="sxs-lookup"><span data-stu-id="1f057-128">Initializes the **GS** (geometry shader) member of **PipelineStream** using the value of the *GS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-129">**StreamOutputCb (const D3D12 \_ Stream \_ OUTPUT \_ desc& StreamOutput)**</span><span class="sxs-lookup"><span data-stu-id="1f057-129">**StreamOutputCb(const D3D12\_STREAM\_OUTPUT\_DESC& StreamOutput)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-130">Inizializza il membro **StreamOutput** di **PipelineStream** usando il valore del parametro *StreamOutput* .</span><span class="sxs-lookup"><span data-stu-id="1f057-130">Initializes the **StreamOutput** member of **PipelineStream** using the value of the *StreamOutput* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-131">**HSCb (const D3D12 \_ shader \_ BYTECODE& HS)**</span><span class="sxs-lookup"><span data-stu-id="1f057-131">**HSCb(const D3D12\_SHADER\_BYTECODE& HS)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-132">Inizializza il membro **HS** (Hull shader) di **PipelineStream** usando il valore del parametro *HS* .</span><span class="sxs-lookup"><span data-stu-id="1f057-132">Initializes the **HS** (hull shader) member of **PipelineStream** using the value of the *HS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-133">**DSCb (const D3D12 \_ shader \_ BYTECODE& DS)**</span><span class="sxs-lookup"><span data-stu-id="1f057-133">**DSCb(const D3D12\_SHADER\_BYTECODE& DS)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-134">Inizializza il membro **DS** (Domain shader) di **PipelineStream** usando il valore del parametro *DS* .</span><span class="sxs-lookup"><span data-stu-id="1f057-134">Initializes the **DS** (domain shader) member of **PipelineStream** using the value of the *DS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-135">**PSCb (const D3D12 \_ shader \_ BYTECODE& PS)**</span><span class="sxs-lookup"><span data-stu-id="1f057-135">**PSCb(const D3D12\_SHADER\_BYTECODE& PS)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-136">Inizializza il membro **PS** (pixel shader) di **PipelineStream** usando il valore del parametro *PS* .</span><span class="sxs-lookup"><span data-stu-id="1f057-136">Initializes the **PS** (pixel shader) member of **PipelineStream** using the value of the *PS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-137">**CSCb (const D3D12 \_ shader \_ BYTECODE& CS)**</span><span class="sxs-lookup"><span data-stu-id="1f057-137">**CSCb(const D3D12\_SHADER\_BYTECODE& CS)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-138">Inizializza il membro **CS** di **PipelineStream** usando il valore del parametro *CS* .</span><span class="sxs-lookup"><span data-stu-id="1f057-138">Initializes the **CS** member of **PipelineStream** using the value of the *CS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-139">**BlendStateCb (const D3D12 \_ Blend \_ desc& BlendState)**</span><span class="sxs-lookup"><span data-stu-id="1f057-139">**BlendStateCb(const D3D12\_BLEND\_DESC& BlendState)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-140">Inizializza il membro **BlendState** di **PipelineStream** usando il valore del parametro *BlendState* .</span><span class="sxs-lookup"><span data-stu-id="1f057-140">Initializes the **BlendState** member of **PipelineStream** using the value of the *BlendState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-141">**DepthStencilStateCb (const D3D12 \_ Depth \_ STENCIL \_ desc& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="1f057-141">**DepthStencilStateCb(const D3D12\_DEPTH\_STENCIL\_DESC& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-142">Inizializza il membro **DepthStencilState** di **PipelineStream** usando il valore del parametro *DepthStencilState* , una [**desc di D3D12 \_ Depth \_ stencil \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span><span class="sxs-lookup"><span data-stu-id="1f057-142">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span></span>

</dd> <dt>

<span data-ttu-id="1f057-143">**DepthStencilState1Cb (const D3D12 \_ Depth \_ STENCIL \_ DESC1& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="1f057-143">**DepthStencilState1Cb(const D3D12\_DEPTH\_STENCIL\_DESC1& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-144">Inizializza il membro **DepthStencilState** di **PipelineStream** usando il valore del parametro *DepthStencilState* , un [**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span><span class="sxs-lookup"><span data-stu-id="1f057-144">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span></span>

</dd> <dt>

<span data-ttu-id="1f057-145">**DSVFormatCb ( \_ formato DXGI DSVFormat)**</span><span class="sxs-lookup"><span data-stu-id="1f057-145">**DSVFormatCb(DXGI\_FORMAT DSVFormat)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-146">Inizializza il membro **DSVFormat** di **PipelineStream** usando il valore del parametro *DSVFormat* .</span><span class="sxs-lookup"><span data-stu-id="1f057-146">Initializes the **DSVFormat** member of **PipelineStream** using the value of the *DSVFormat* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-147">**RasterizerStateCb (const D3D12 \_ rasterizzatore \_ desc& RasterizerState)**</span><span class="sxs-lookup"><span data-stu-id="1f057-147">**RasterizerStateCb(const D3D12\_RASTERIZER\_DESC& RasterizerState)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-148">Inizializza il membro **RasterizerState** di **PipelineStream** usando il valore del parametro *RasterizerState* .</span><span class="sxs-lookup"><span data-stu-id="1f057-148">Initializes the **RasterizerState** member of **PipelineStream** using the value of the *RasterizerState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-149">**RTVFormatsCb (const D3D12 \_ RT \_ FORMAT \_ Array& RTVFormats)**</span><span class="sxs-lookup"><span data-stu-id="1f057-149">**RTVFormatsCb(const D3D12\_RT\_FORMAT\_ARRAY& RTVFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-150">Inizializza il membro **RTVFormats** di **PipelineStream** usando il valore del parametro *RTVFormats* .</span><span class="sxs-lookup"><span data-stu-id="1f057-150">Initializes the **RTVFormats** member of **PipelineStream** using the value of the *RTVFormats* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-151">**SampleDescCb (const DXGI \_ Sample \_ desc& SampleDesc)**</span><span class="sxs-lookup"><span data-stu-id="1f057-151">**SampleDescCb(const DXGI\_SAMPLE\_DESC& SampleDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-152">Inizializza il membro **SampleDesc** di **PipelineStream** usando il valore del parametro *SampleDesc* .</span><span class="sxs-lookup"><span data-stu-id="1f057-152">Initializes the **SampleDesc** member of **PipelineStream** using the value of the *SampleDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-153">**SampleMaskCb (UINT SampleMask)**</span><span class="sxs-lookup"><span data-stu-id="1f057-153">**SampleMaskCb(UINT SampleMask)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-154">Inizializza il membro **SampleMask** di **PipelineStream** usando il valore del parametro *SampleMask* .</span><span class="sxs-lookup"><span data-stu-id="1f057-154">Initializes the **SampleMask** member of **PipelineStream** using the value of the *SampleMask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-155">**ViewInstancingCb (const D3D12 \_ View \_ Instancing \_ desc& ViewInstancingDesc)**</span><span class="sxs-lookup"><span data-stu-id="1f057-155">**ViewInstancingCb(const D3D12\_VIEW\_INSTANCING\_DESC& ViewInstancingDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-156">Inizializza il membro **ViewInstancingDesc** di **PipelineStream** usando il valore del parametro *ViewInstancingDesc* .</span><span class="sxs-lookup"><span data-stu-id="1f057-156">Initializes the **ViewInstancingDesc** member of **PipelineStream** using the value of the *ViewInstancingDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-157">**CachedPSOCb (const D3D12- \_ stato della pipeline memorizzato nella cache \_ \_& CachedPSO)**</span><span class="sxs-lookup"><span data-stu-id="1f057-157">**CachedPSOCb(const D3D12\_CACHED\_PIPELINE\_STATE& CachedPSO)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-158">Inizializza il membro **CachedPSO** di **PipelineStream** usando il valore del parametro *CachedPSO* .</span><span class="sxs-lookup"><span data-stu-id="1f057-158">Initializes the **CachedPSO** member of **PipelineStream** using the value of the *CachedPSO* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-159">**ErrorBadInputParameter (UINT)**</span><span class="sxs-lookup"><span data-stu-id="1f057-159">**ErrorBadInputParameter(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-160">Non esegue operazioni.</span><span class="sxs-lookup"><span data-stu-id="1f057-160">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-161">**ErrorDuplicateSubobject ( \_ tipo di \_ sottooggetto stato della pipeline D3D12 \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="1f057-161">**ErrorDuplicateSubobject(D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-162">Non esegue operazioni.</span><span class="sxs-lookup"><span data-stu-id="1f057-162">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="1f057-163">**ErrorUnknownSubobject (UINT)**</span><span class="sxs-lookup"><span data-stu-id="1f057-163">**ErrorUnknownSubobject(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="1f057-164">Non esegue operazioni.</span><span class="sxs-lookup"><span data-stu-id="1f057-164">Does nothing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f057-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f057-165">Remarks</span></span>

<span data-ttu-id="1f057-166">Quando viene passato come secondo parametro alla funzione [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , i dettagli dell'oggetto [**\_ \_ \_ stream1 dello stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream1.md) interno vengono clonati dal [**del \_ \_ flusso di \_ stato \_ della pipeline D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passati come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="1f057-166">When passed as the second parameter to the [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) function, the details of the internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md) object are cloned from the [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passed as the first parameter.</span></span> <span data-ttu-id="1f057-167">Questo processo convalida la descrizione del flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="1f057-167">This process validates the source stream description.</span></span> <span data-ttu-id="1f057-168">Se D3DX12ParsePipelineStream restituisce **S \_ OK**, sia la descrizione del flusso di origine che lo **stato della pipeline CD3DX12 risultante \_ \_ \_ STREAM1PipelineStream** sono validi; in caso contrario, entrambi non sono validi.</span><span class="sxs-lookup"><span data-stu-id="1f057-168">If D3DX12ParsePipelineStream returns **S\_OK**, then both the source stream description and the resulting **CD3DX12\_PIPELINE\_STATE\_STREAM1PipelineStream** are valid; otherwise both are invalid.</span></span> <span data-ttu-id="1f057-169">I flussi non validi e altri errori vengono segnalati solo tramite il valore restituito di D3DX12ParsePipelineStream; Questa struttura implementa i callback di errore per non eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="1f057-169">Invalid streams and other errors are reported only through the return value of D3DX12ParsePipelineStream; this structure implements the error callbacks to do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f057-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f057-170">Requirements</span></span>



| <span data-ttu-id="1f057-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f057-171">Requirement</span></span> | <span data-ttu-id="1f057-172">Valore</span><span class="sxs-lookup"><span data-stu-id="1f057-172">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1f057-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f057-173">Header</span></span><br/> | <dl> <span data-ttu-id="1f057-174"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f057-174"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f057-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f057-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f057-176">Strutture helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1f057-176">Helper Structures for Direct3D 12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1f057-177">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="1f057-177">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





