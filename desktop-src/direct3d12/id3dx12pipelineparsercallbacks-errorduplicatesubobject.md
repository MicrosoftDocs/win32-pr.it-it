---
title: Metodo ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject (D3DX12. h)
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
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323111"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a>Metodo ID3DX12PipelineParserCallbacks:: ErrorDuplicateSubobject

Chiama il callback di errore del sottooggetto duplicato di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DuplicateType* 
</dt> <dd>

Tipo: **[ **\_ \_ \_ \_ tipo di sottooggetto stato della pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**

Tipo di sottooggetto duplicato.

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

[**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

