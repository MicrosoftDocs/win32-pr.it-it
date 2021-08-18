---
title: Interfaccia ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Interfaccia che rappresenta una raccolta di callback di parser e di errore usati dalla funzione helper D3DX12parsePipelineStream.
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
ms.openlocfilehash: f83e0987009e60d5e207a9531cc4809f6cfcfbd5b50360a583df8cb0c01898f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733744"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>Interfaccia ID3DX12PipelineParserCallbacks

Interfaccia che rappresenta una raccolta di callback di parser ed errori usati dalla funzione helper [**D3DX12parsePipelineStream.**](d3dx12parsepipelinestream.md)

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX12PipelineParserCallbacks** include questi metodi.



| Metodo                                                                                    | Descrizione                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | Chiama il callback del sottooggetto della descrizione dello stato di blend di un oggetto che implementa questa interfaccia.<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | Chiama il callback del sottooggetto PSO (Pipeline State Object) memorizzato nella cache di un oggetto che implementa questa interfaccia.<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | Chiama il callback del sottooggetto compute shader di un oggetto che implementa questa interfaccia.<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | Chiama il callback depth stencil dell'oggetto secondario [**D3D12 \_ DEPTH \_ STENCIL \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)di un oggetto che implementa questa interfaccia.<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | Chiama il depth stencil di sottooggetto in formato valore di un oggetto che implementa questa interfaccia.<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | Chiama il depth stencil del sottooggetto di stato di un oggetto che implementa questa interfaccia.<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | Chiama il callback del sottooggetto dello shader di dominio di un oggetto che implementa questa interfaccia.<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | Chiama il callback di errore del parametro di input non valido di un oggetto che implementa questa interfaccia.<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | Chiama il callback di errore del sottooggetto duplicato di un oggetto che implementa questa interfaccia.<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | Chiama il callback di errore del sottooggetto sconosciuto di un oggetto che implementa questa interfaccia.<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | Chiama il callback del sottooggetto flags di un oggetto che implementa questa interfaccia.<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | Chiama il callback del sottooggetto geometry shader di un oggetto che implementa questa interfaccia.<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | Chiama il callback del sottooggetto hull shader di un oggetto che implementa questa interfaccia.<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | Chiama il index buffer di sottooggetto del valore strip-cut di un oggetto che implementa questa interfaccia.<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | Chiama il callback del sottooggetto di layout di input di un oggetto che implementa questa interfaccia.<br/>                                                                            |
| [**NodemaskCb**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | Chiama il callback del sottooggetto nodemask di un oggetto che implementa questa interfaccia.<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | Chiama il callback del sottooggetto del tipo di topologia primitiva di un oggetto che implementa questa interfaccia.<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | Chiama il pixel shader di sottooggetto di un oggetto che implementa questa interfaccia.<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | Chiama il callback del sottooggetto della descrizione dello stato del rasterizzatore di un oggetto che implementa questa interfaccia.<br/>                                                            |
| [**RootSignatureCB**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | Chiama il callback del sottooggetto della firma radice di un oggetto che implementa questa interfaccia.<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | Chiama il callback del sottooggetto della matrice di formato di destinazione di rendering di un oggetto che implementa questa interfaccia.<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | Chiama il callback del sottooggetto di descrizione di esempio di un oggetto che implementa questa interfaccia.<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | Chiama il callback del sottooggetto maschera di esempio di un oggetto che implementa questa interfaccia.<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | Chiama il callback del sottooggetto di descrizione dell'output del flusso di un oggetto che implementa questa interfaccia.<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | Chiama il callback del sottooggetto vertex shader di un oggetto che implementa questa interfaccia.<br/>                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce helper per Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





