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
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>\_ \_ \_ \_ Struttura helper di analisi del flusso di stato della pipeline CD3DX12 \_

Compila un \_ \_ \_ oggetto flusso di stato della pipeline CD3DX12 interno da dettagli di sottooggetti passati nelle funzioni membro corrispondenti. Questo struct implementa l'interfaccia [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .

## <a name="syntax"></a>Sintassi


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



## <a name="members"></a>Members

<dl> <dt>

**PipelineStream**
</dt> <dd>

Stato della [**pipeline CD3DX12 interno \_ \_ \_ stream1**](cd3dx12-pipeline-state-stream1.md). Lo stato corrente rappresenta l'effetto cumulativo dei metodi di callback chiamati su questo oggetto.

</dd> <dt>

**FlagsCb ( \_ flag di stato della pipeline D3D12 \_ \_ )**
</dt> <dd>

Inizializza il membro **Flags** di **PipelineStream** usando il valore del parametro *Flags* .

</dd> <dt>

**NodeMaskCb (UINT node mask)**
</dt> <dd>

Inizializza il membro **node mask** di **PipelineStream** usando il valore del parametro *node mask* .

</dd> <dt>

**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

Inizializza il membro **pRootSignature** di **PipelineStream** usando il valore del parametro *pRootSignature* .

</dd> <dt>

**InputLayoutCb (const D3D12 \_ input \_ LAYOUT \_ desc& InputLayout)**
</dt> <dd>

Inizializza il membro **InputLayout** di **PipelineStream** usando il valore del parametro *InputLayout* .

</dd> <dt>

**IBStripCutValueCb (D3D12 \_ index \_ buffer \_ Strip \_ Cut \_ value IBStripCutValue)**
</dt> <dd>

Inizializza il membro **IBStripCutValue** di **PipelineStream** usando il valore del parametro *IBStripCutValue* .

</dd> <dt>

**PrimitiveTopologyTypeCb ( \_ tipo di \_ topologia primitiva D3D12 \_ PrimitiveTopologyType)**
</dt> <dd>

Inizializza il membro **PrimitiveTopologyType** di **PipelineStream** usando il valore del parametro *PrimitiveTopologyType* .

</dd> <dt>

**VSCb (const D3D12 \_ shader \_ BYTECODE& vs)**
</dt> <dd>

Inizializza il membro **vs** (Vertex shader) di **PipelineStream** usando il valore del parametro *vs* .

</dd> <dt>

**GSCb (const D3D12 \_ shader \_ BYTECODE& GS)**
</dt> <dd>

Inizializza il membro **GS** (Geometry shader) di **PipelineStream** usando il valore del parametro *GS* .

</dd> <dt>

**StreamOutputCb (const D3D12 \_ Stream \_ OUTPUT \_ desc& StreamOutput)**
</dt> <dd>

Inizializza il membro **StreamOutput** di **PipelineStream** usando il valore del parametro *StreamOutput* .

</dd> <dt>

**HSCb (const D3D12 \_ shader \_ BYTECODE& HS)**
</dt> <dd>

Inizializza il membro **HS** (Hull shader) di **PipelineStream** usando il valore del parametro *HS* .

</dd> <dt>

**DSCb (const D3D12 \_ shader \_ BYTECODE& DS)**
</dt> <dd>

Inizializza il membro **DS** (Domain shader) di **PipelineStream** usando il valore del parametro *DS* .

</dd> <dt>

**PSCb (const D3D12 \_ shader \_ BYTECODE& PS)**
</dt> <dd>

Inizializza il membro **PS** (pixel shader) di **PipelineStream** usando il valore del parametro *PS* .

</dd> <dt>

**CSCb (const D3D12 \_ shader \_ BYTECODE& CS)**
</dt> <dd>

Inizializza il membro **CS** di **PipelineStream** usando il valore del parametro *CS* .

</dd> <dt>

**BlendStateCb (const D3D12 \_ Blend \_ desc& BlendState)**
</dt> <dd>

Inizializza il membro **BlendState** di **PipelineStream** usando il valore del parametro *BlendState* .

</dd> <dt>

**DepthStencilStateCb (const D3D12 \_ Depth \_ STENCIL \_ desc& DepthStencilState)**
</dt> <dd>

Inizializza il membro **DepthStencilState** di **PipelineStream** usando il valore del parametro *DepthStencilState* , una [**desc di D3D12 \_ Depth \_ stencil \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).

</dd> <dt>

**DepthStencilState1Cb (const D3D12 \_ Depth \_ STENCIL \_ DESC1& DepthStencilState)**
</dt> <dd>

Inizializza il membro **DepthStencilState** di **PipelineStream** usando il valore del parametro *DepthStencilState* , un [**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).

</dd> <dt>

**DSVFormatCb ( \_ formato DXGI DSVFormat)**
</dt> <dd>

Inizializza il membro **DSVFormat** di **PipelineStream** usando il valore del parametro *DSVFormat* .

</dd> <dt>

**RasterizerStateCb (const D3D12 \_ rasterizzatore \_ desc& RasterizerState)**
</dt> <dd>

Inizializza il membro **RasterizerState** di **PipelineStream** usando il valore del parametro *RasterizerState* .

</dd> <dt>

**RTVFormatsCb (const D3D12 \_ RT \_ FORMAT \_ Array& RTVFormats)**
</dt> <dd>

Inizializza il membro **RTVFormats** di **PipelineStream** usando il valore del parametro *RTVFormats* .

</dd> <dt>

**SampleDescCb (const DXGI \_ Sample \_ desc& SampleDesc)**
</dt> <dd>

Inizializza il membro **SampleDesc** di **PipelineStream** usando il valore del parametro *SampleDesc* .

</dd> <dt>

**SampleMaskCb (UINT SampleMask)**
</dt> <dd>

Inizializza il membro **SampleMask** di **PipelineStream** usando il valore del parametro *SampleMask* .

</dd> <dt>

**ViewInstancingCb (const D3D12 \_ View \_ Instancing \_ desc& ViewInstancingDesc)**
</dt> <dd>

Inizializza il membro **ViewInstancingDesc** di **PipelineStream** usando il valore del parametro *ViewInstancingDesc* .

</dd> <dt>

**CachedPSOCb (const D3D12- \_ stato della pipeline memorizzato nella cache \_ \_& CachedPSO)**
</dt> <dd>

Inizializza il membro **CachedPSO** di **PipelineStream** usando il valore del parametro *CachedPSO* .

</dd> <dt>

**ErrorBadInputParameter (UINT)**
</dt> <dd>

Non esegue operazioni.

</dd> <dt>

**ErrorDuplicateSubobject ( \_ tipo di \_ sottooggetto stato della pipeline D3D12 \_ \_ )**
</dt> <dd>

Non esegue operazioni.

</dd> <dt>

**ErrorUnknownSubobject (UINT)**
</dt> <dd>

Non esegue operazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando viene passato come secondo parametro alla funzione [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , i dettagli dell'oggetto [**\_ \_ \_ stream1 dello stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream1.md) interno vengono clonati dal [**del \_ \_ flusso di \_ stato \_ della pipeline D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passati come primo parametro. Questo processo convalida la descrizione del flusso di origine. Se D3DX12ParsePipelineStream restituisce **S \_ OK**, sia la descrizione del flusso di origine che lo **stato della pipeline CD3DX12 risultante \_ \_ \_ STREAM1PipelineStream** sono validi; in caso contrario, entrambi non sono validi. I flussi non validi e altri errori vengono segnalati solo tramite il valore restituito di D3DX12ParsePipelineStream; Questa struttura implementa i callback di errore per non eseguire alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





