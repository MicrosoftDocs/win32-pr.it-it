---
title: Metodo ID3DX12PipelineParserCallbacks IBStripCutValueCb (D3DX12. h)
description: Chiama il callback del sottooggetto del valore della riduzione del buffer di indice di un oggetto che implementa questa interfaccia.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Metodo IBStripCutValueCb
- Metodo IBStripCutValueCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo IBStripCutValueCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323102"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: IBStripCutValueCb

Chiama il callback del sottooggetto del valore della riduzione del buffer di indice di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IBStripCutValue* 
</dt> <dd>

Tipo: **[ **D3D12 \_ index \_ buffer \_ \_ Cut Stripe \_ value**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**

Dettagli del sottooggetto del valore di strip-cut buffer index analizzato da un flusso di stato della pipeline.

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

[**\_ \_ \_ \_ Valore Cut Strip buffer index \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





