---
title: CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER struttura (D3dx12.h)
description: Compila un oggetto INTERNO CD3DX12 PIPELINE STATE STREAM dai \_ \_ dettagli del \_ sottooggetto passati alle funzioni membro corrispondenti. Questo struct implementa l'interfaccia ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER struttura
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
ms.openlocfilehash: d20c34fb2c32cc588a12ac820cd80083d3c3139fa85cbf36810379a21618e80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851251"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>Struttura HELPER DI ANALISI FLUSSO DELLO STATO DELLA PIPELINE CD3DX12 \_ \_ \_ \_ \_

Compila un oggetto INTERNO CD3DX12 PIPELINE STATE STREAM dai \_ \_ dettagli del \_ sottooggetto passati alle funzioni membro corrispondenti. Questo struct implementa [**l'interfaccia ID3DX12PipelineParserCallbacks.**](id3dx12pipelineparsercallbacks.md)

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

FLUSSO INTERNO [**DELLO STATO DELLA PIPELINE CD3DX1211 \_ \_ \_**](cd3dx12-pipeline-state-stream1.md). Lo stato corrente rappresenta l'effetto cumulativo dei metodi di callback chiamati su questo oggetto.

</dd> <dt>

**FlagsCb(D3D12 \_ PIPELINE \_ STATE \_ FLAGS Flags)**
</dt> <dd>

Inizializza il **membro Flags** di **PipelineStream** usando il valore del *parametro Flags.*

</dd> <dt>

**NodeMaskCb(UINT NodeMask)**
</dt> <dd>

Inizializza il **membro NodeMask** di **PipelineStream** usando il valore del *parametro Nodemask.*

</dd> <dt>

**RootSignatureCb(ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

Inizializza il **membro pRootSignature** di **PipelineStream** usando il valore del *parametro pRootSignature.*

</dd> <dt>

**InputLayoutCb(const D3D12 \_ INPUT \_ LAYOUT \_ DESC& InputLayout)**
</dt> <dd>

Inizializza il **membro InputLayout** di **PipelineStream** usando il valore del *parametro InputLayout.*

</dd> <dt>

**IBStripCutValueCb(D3D12 \_ INDEX \_ BUFFER \_ STRIP \_ CUT \_ VALUE IBStripCutValue)**
</dt> <dd>

Inizializza il **membro IBStripCutValue** di **PipelineStream** usando il valore del *parametro IBStripCutValue.*

</dd> <dt>

**PrimitiveTopologyTypeCb(D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE PrimitiveTopologyType)**
</dt> <dd>

Inizializza il **membro PrimitiveTopologyType** di **PipelineStream** usando il valore del *parametro PrimitiveTopologyType.*

</dd> <dt>

**VSCb(const D3D12 \_ SHADER \_ BYTECODE& VS)**
</dt> <dd>

Inizializza il **membro VS** (vertex shader) di **PipelineStream** usando il valore del *parametro VS.*

</dd> <dt>

**GSCb(const D3D12 \_ SHADER \_ BYTECODE& GS)**
</dt> <dd>

Inizializza il **membro GS** (geometry shader) di **PipelineStream** usando il valore del *parametro GS.*

</dd> <dt>

**StreamOutputCb(const D3D12 \_ STREAM \_ OUTPUT \_ DESC& StreamOutput)**
</dt> <dd>

Inizializza il **membro StreamOutput** di **PipelineStream** usando il valore del *parametro StreamOutput.*

</dd> <dt>

**HSCb(const D3D12 \_ SHADER \_ BYTECODE& HS)**
</dt> <dd>

Inizializza il **membro HS** (hull shader) di **PipelineStream** usando il valore del *parametro HS.*

</dd> <dt>

**DSCb(const D3D12 \_ SHADER \_ BYTECODE& DS)**
</dt> <dd>

Inizializza il **membro DS** (domain shader) di **PipelineStream** usando il valore del *parametro DS.*

</dd> <dt>

**PSCb(const D3D12 \_ SHADER \_ BYTECODE& PS)**
</dt> <dd>

Inizializza il **membro PS** (pixel shader) di **PipelineStream** usando il valore del *parametro PS.*

</dd> <dt>

**CSCb(const D3D12 \_ SHADER \_ BYTECODE& CS)**
</dt> <dd>

Inizializza il membro **CS** di **PipelineStream** usando il valore del *parametro CS.*

</dd> <dt>

**BlendStateCb(const D3D12 \_ BLEND \_ DESC& BlendState)**
</dt> <dd>

Inizializza il **membro BlendState** di **PipelineStream** usando il valore del *parametro BlendState.*

</dd> <dt>

**DepthStencilStateCb(const D3D12 \_ DEPTH \_ STENCIL \_ DESC& DepthStencilState)**
</dt> <dd>

Inizializza il membro **DepthStencilState** di **PipelineStream** usando il valore del *parametro DepthStencilState,* [**un D3D12 \_ DEPTH STENCIL \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

</dd> <dt>

**DepthStencilState1Cb(const D3D12 \_ DEPTH \_ STENCIL \_ DESC1& DepthStencilState)**
</dt> <dd>

Inizializza il membro **DepthStencilState** di **PipelineStream** usando il valore del *parametro DepthStencilState,* [**un D3D12 \_ DEPTH STENCIL \_ \_ DESC1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)

</dd> <dt>

**DSVFormatCb(DXGI \_ FORMAT DSVFormat)**
</dt> <dd>

Inizializza il **membro DSVFormat** di **PipelineStream** usando il valore del *parametro DSVFormat.*

</dd> <dt>

**RasterizerStateCb(const D3D12 \_ RASTERIZER \_ DESC& RasterizerState)**
</dt> <dd>

Inizializza il **membro RasterizerState** di **PipelineStream** usando il valore del *parametro RasterizerState.*

</dd> <dt>

**RTVFormatsCb(const D3D12 \_ RT \_ FORMAT \_ ARRAY& RTVFormats)**
</dt> <dd>

Inizializza il **membro RTVFormats** di **PipelineStream** usando il valore del *parametro RTVFormats.*

</dd> <dt>

**SampleDescCb(const DXGI \_ SAMPLE \_ DESC& SampleDesc)**
</dt> <dd>

Inizializza il **membro SampleDesc** di **PipelineStream** usando il valore del *parametro SampleDesc.*

</dd> <dt>

**SampleMaskCb(UINT SampleMask)**
</dt> <dd>

Inizializza il **membro SampleMask** di **PipelineStream** usando il valore del *parametro SampleMask.*

</dd> <dt>

**ViewInstancingCb(const D3D12 \_ VIEW \_ INSTANCING \_ DESC& ViewInstancingDesc)**
</dt> <dd>

Inizializza il **membro ViewInstancingDesc** di **PipelineStream** usando il valore *del parametro ViewInstancingDesc.*

</dd> <dt>

**CachedPSOCb(const D3D12 \_ CACHED \_ PIPELINE \_ STATE& CachedPSO)**
</dt> <dd>

Inizializza il **membro CachedPSO** di **PipelineStream** usando il valore del *parametro CachedPSO.*

</dd> <dt>

**ErrorBadInputParameter(UINT)**
</dt> <dd>

Non esegue operazioni.

</dd> <dt>

**ErrorDuplicateSubobject(D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE)**
</dt> <dd>

Non esegue operazioni.

</dd> <dt>

**ErrorUnknownSubobject(UINT)**
</dt> <dd>

Non esegue operazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando vengono passati come secondo parametro alla funzione [**D3DX12ParsePipelineStream,**](d3dx12parsepipelinestream.md) i dettagli dell'oggetto INTERNO [**CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md) vengono clonati dalla pipeline [**D3D12 \_ PIPELINE STATE STREAM \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passata come primo parametro. Questo processo convalida la descrizione del flusso di origine. Se D3DX12ParsePipelineStream restituisce **S \_ OK,** sono validi sia la descrizione del flusso di origine che l'oggetto **CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1PipelineStream** risultante; in caso contrario, entrambi non sono validi. I flussi non validi e altri errori vengono segnalati solo tramite il valore restituito di D3DX12ParsePipelineStream. questa struttura implementa i callback di errore per non eseguire alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





