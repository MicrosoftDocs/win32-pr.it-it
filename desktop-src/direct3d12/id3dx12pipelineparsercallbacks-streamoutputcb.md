---
title: Metodo ID3DX12PipelineParserCallbacks StreamOutputCb (D3DX12. h)
description: Chiama il callback del sottooggetto della descrizione di output del flusso di un oggetto che implementa questa interfaccia.
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
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322149"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: StreamOutputCb

Chiama il callback del sottooggetto della descrizione di output del flusso di un oggetto che implementa questa interfaccia.

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

Tipo: **const [**D3D12 \_ Stream \_ output \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**

Dettagli del sottooggetto della descrizione di output del flusso analizzato da un flusso di stato della pipeline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non restituisce alcun elemento.

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

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**\_Desc di \_ output \_ flusso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





