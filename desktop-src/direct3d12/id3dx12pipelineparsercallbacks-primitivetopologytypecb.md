---
title: Metodo ID3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb (D3DX12. h)
description: Chiama il callback del sottooggetto del tipo di topologia primitivo di un oggetto che implementa questa interfaccia.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Metodo PrimitiveTopologyTypeCb
- Metodo PrimitiveTopologyTypeCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo PrimitiveTopologyTypeCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323096"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a>ID3DX12PipelineParserCallbacks::P metodo rimitiveTopologyTypeCb

Chiama il callback del sottooggetto del tipo di topologia primitivo di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PrimitiveTopologyType* 
</dt> <dd>

Tipo: **[ **\_ \_ \_ tipo di topologia primitiva D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

Dettagli del sottooggetto del tipo di topologia primitivo analizzato da un flusso di stato della pipeline.

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

[**\_Tipo di \_ topologia PRIMItiva D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





