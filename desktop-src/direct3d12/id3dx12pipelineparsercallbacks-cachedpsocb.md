---
title: Metodo ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12. h)
description: Chiama il callback del sottooggetto PSO memorizzato nella cache (oggetto stato della pipeline) di un oggetto che implementa questa interfaccia.
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
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323121"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: CachedPSOCb

Chiama il callback del sottooggetto PSO memorizzato nella cache (oggetto stato della pipeline) di un oggetto che implementa questa interfaccia.

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

Tipo: **const [**D3D12- \_ \_ \_ stato della pipeline memorizzato nella cache**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

Dettagli del sottooggetto PSO memorizzato nella cache (oggetto stato della pipeline) analizzato da un flusso di stato della pipeline.

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

[**\_Stato della pipeline D3D12 memorizzato nella cache \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





