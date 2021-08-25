---
title: Metodo ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12.h)
description: Chiama il callback depth stencil oggetto secondario di stato di un oggetto che implementa questa interfaccia.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Metodo DepthStencilStateCb
- Metodo DepthStencilStateCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1086156fcaa6b8736c049c93bacc5dfd1f5e915ba8a7006b3c71e654ba65f52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894581"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>Metodo ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12.h)

Chiama il callback depth stencil oggetto secondario di stato di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DepthStencilState* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ DEPTH STENCIL \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**

Dettagli del sottooggetto depth stencil stato della pipeline analizzato da un flusso di stato della pipeline.

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

[**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





