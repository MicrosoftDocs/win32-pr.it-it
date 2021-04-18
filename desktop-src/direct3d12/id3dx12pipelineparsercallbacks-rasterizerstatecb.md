---
title: Metodo ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12. h)
description: Chiama il callback del sottooggetto della descrizione dello stato di rasterizzazione di un oggetto che implementa questa interfaccia.
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
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323095"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: RasterizerStateCb

Chiama il callback del sottooggetto della descrizione dello stato di rasterizzazione di un oggetto che implementa questa interfaccia.

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

Tipo: **const [**D3D12 \_ rasterizzatore \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Dettagli del sottooggetto della descrizione dello stato di rasterizzazione analizzato da un flusso di stato della pipeline.

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

[**D3D12 \_ rasterizzatore \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





