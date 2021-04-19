---
title: Interfaccia ID3DX12PipelineParserCallbacks (D3DX12. h)
description: Interfaccia che rappresenta una raccolta di callback del parser e degli errori utilizzati dalla funzione di supporto D3DX12parsePipelineStream.
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- Interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, descritta
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0061746da589c30e4745dfa3e4dc573f7b5d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323091"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>Interfaccia ID3DX12PipelineParserCallbacks

Interfaccia che rappresenta una raccolta di callback del parser e degli errori utilizzati dalla funzione di supporto [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) .

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX12PipelineParserCallbacks** dispone di questi metodi.



| Metodo                                                                                    | Descrizione                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | Chiama il callback del sottooggetto Descrizione dello stato di Blend di un oggetto che implementa questa interfaccia.<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | Chiama il callback del sottooggetto PSO memorizzato nella cache (oggetto stato della pipeline) di un oggetto che implementa questa interfaccia.<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | Chiama il callback del sottooggetto compute shader di un oggetto che implementa questa interfaccia.<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | Chiama lo stato depth stencil ([**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) callback di un oggetto che implementa questa interfaccia.<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | Chiama il callback del sottooggetto del formato del valore depth stencil di un oggetto che implementa questa interfaccia.<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | Chiama il callback del sottooggetto stato depth stencil di un oggetto che implementa questa interfaccia.<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | Chiama il callback del sottooggetto del Domain shader di un oggetto che implementa questa interfaccia.<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | Chiama il callback di errore del parametro di input errato di un oggetto che implementa questa interfaccia.<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | Chiama il callback di errore del sottooggetto duplicato di un oggetto che implementa questa interfaccia.<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | Chiama il callback di errore del sottooggetto sconosciuto di un oggetto che implementa questa interfaccia.<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | Chiama il callback del sottooggetto Flags di un oggetto che implementa questa interfaccia.<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | Chiama il callback del sottooggetto geometry shader di un oggetto che implementa questa interfaccia.<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | Chiama il callback del sottooggetto Hull shader di un oggetto che implementa questa interfaccia.<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | Chiama il callback del sottooggetto del valore della riduzione del buffer di indice di un oggetto che implementa questa interfaccia.<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | Chiama il callback del sottooggetto layout di input di un oggetto che implementa questa interfaccia.<br/>                                                                            |
| [**NodemaskCb**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | Chiama il callback del sottooggetto node mask di un oggetto che implementa questa interfaccia.<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | Chiama il callback del sottooggetto del tipo di topologia primitivo di un oggetto che implementa questa interfaccia.<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | Chiama il callback pixel shader sottooggetto di un oggetto che implementa questa interfaccia.<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | Chiama il callback del sottooggetto della descrizione dello stato di rasterizzazione di un oggetto che implementa questa interfaccia.<br/>                                                            |
| [**RootSignatureCB**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | Chiama il callback del sottooggetto della firma radice di un oggetto che implementa questa interfaccia.<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | Chiama il callback del sottooggetto della matrice del formato della destinazione di rendering di un oggetto che implementa questa interfaccia.<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | Chiama il callback di esempio della descrizione del sottooggetto di un oggetto che implementa questa interfaccia.<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | Chiama il callback del sottooggetto maschera di esempio di un oggetto che implementa questa interfaccia.<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | Chiama il callback del sottooggetto della descrizione di output del flusso di un oggetto che implementa questa interfaccia.<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | Chiama il callback del sottooggetto vertex shader di un oggetto che implementa questa interfaccia.<br/>                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce helper per Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





