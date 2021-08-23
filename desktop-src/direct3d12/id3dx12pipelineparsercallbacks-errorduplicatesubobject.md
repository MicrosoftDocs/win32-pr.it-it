---
title: Metodo ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject (D3DX12.h)
description: Chiama il callback di errore del sottooggetto duplicato di un oggetto che implementa questa interfaccia.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Metodo ErrorDuplicateSubobject
- Metodo ErrorDuplicateSubobject, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo ErrorDuplicateSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33724b1fdfec4951ce2efb31d4916ce210dc2b73858a5ef250c14a8744646bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045469"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a>Metodo ID3DX12PipelineParserCallbacks::ErrorDuplicateSubobject

Chiama il callback di errore del sottooggetto duplicato di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo duplicato* 
</dt> <dd>

Tipo: **[ **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**

Tipo di oggetto secondario duplicato.

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

[**TIPO DI OGGETTO SECONDARIO STATO PIPELINE D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

