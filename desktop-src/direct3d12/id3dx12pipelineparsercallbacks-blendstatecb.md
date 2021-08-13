---
title: Metodo ID3DX12PipelineParserCallbacks BlendStateCb (D3DX12.h)
description: Chiama il callback del sottooggetto della descrizione dello stato di blend di un oggetto che implementa questa interfaccia.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Metodo BlendStateCb
- Metodo BlendStateCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo BlendStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a9d84e3648a54668211b8b9e590c653111c93553115aba43b5353f9549bfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528979"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a>Metodo ID3DX12PipelineParserCallbacks::BlendStateCb

Chiama il callback del sottooggetto della descrizione dello stato di blend di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BlendState* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Dettagli del sottooggetto di descrizione dello stato di blend analizzato da un flusso di stato della pipeline.

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

[**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





