---
title: Metodo ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12.h)
description: Chiama il callback del sottooggetto di descrizione dello stato del rasterizzatore di un oggetto che implementa questa interfaccia.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Metodo RasterizerStateCb
- Metodo RasterizerStateCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo RasterizerStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39a179f26d88f25027eb9ffc2b4b3712ac963b65179334fff1bfa4d6103ef76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528621"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a>Metodo ID3DX12PipelineParserCallbacks::RasterizerStateCb

Chiama il callback del sottooggetto di descrizione dello stato del rasterizzatore di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RasterizerState* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Dettagli del sottooggetto di descrizione dello stato del rasterizzatore analizzato da un flusso di stato della pipeline.

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

[**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





