---
title: Metodo ID3DX12PipelineParserCallbacks BlendStateCb (D3DX12. h)
description: Chiama il callback del sottooggetto Descrizione dello stato di Blend di un oggetto che implementa questa interfaccia.
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
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323122"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: BlendStateCb

Chiama il callback del sottooggetto Descrizione dello stato di Blend di un oggetto che implementa questa interfaccia.

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

Tipo: **const [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Dettagli del sottooggetto della descrizione dello stato di Blend analizzato da un flusso di stato della pipeline.

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

[**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





