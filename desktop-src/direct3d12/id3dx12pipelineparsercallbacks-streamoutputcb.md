---
title: Metodo ID3DX12PipelineParserCallbacks StreamOutputCb (D3DX12.h)
description: Chiama il callback del sottooggetto della descrizione dell'output del flusso di un oggetto che implementa questa interfaccia.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Metodo StreamOutputCb
- Metodo StreamOutputCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo StreamOutputCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1e484d044bc4de2be3d40c6080e77b62aa57b59f0161c2021b8696316970542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632351"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a>Metodo ID3DX12PipelineParserCallbacks::StreamOutputCb

Chiama il callback del sottooggetto della descrizione dell'output del flusso di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StreamOutput* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ STREAM OUTPUT \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**

Dettagli dell'oggetto secondario della descrizione dell'output del flusso analizzato da un flusso di stato della pipeline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non restituisce alcun valore.

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

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**D3D12 \_ STREAM \_ OUTPUT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





