---
title: Metodo ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12.h)
description: Chiama il callback del sottooggetto PSO (Pipeline State Object) memorizzato nella cache di un oggetto che implementa questa interfaccia.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Metodo CachedPSOCb
- Metodo CachedPSOCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo CachedPSOCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb585a3c82b7e85e6653efee6b3a1bf050051fec5cef0a2c82f0645fef542d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807498"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a>Metodo ID3DX12PipelineParserCallbacks::CachedPSOCb

Chiama il callback del sottooggetto PSO (Pipeline State Object) memorizzato nella cache di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CachedPSO* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ CACHED \_ PIPELINE \_ STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

Dettagli dell'oggetto secondario PSO (Pipeline State Object) memorizzato nella cache analizzato da un flusso di stato della pipeline.

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

[**STATO DELLA \_ PIPELINE MEMORIZZATA NELLA CACHE D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





