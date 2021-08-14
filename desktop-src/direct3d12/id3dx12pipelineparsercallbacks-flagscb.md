---
title: Metodo FlagsCb ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Chiama il callback del sottooggetto flags di un oggetto che implementa questa interfaccia.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Metodo FlagsCb
- Metodo FlagsCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo FlagsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d14e8b507ae04a5f35b2786ca4ba7ab6ec19bb449492aa2c40f32510cd3ecb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528783"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a>Metodo ID3DX12PipelineParserCallbacks::FlagsCb

Chiama il callback del sottooggetto flags di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* 
</dt> <dd>

Tipo: **[ **FLAG DI STATO \_ DELLA PIPELINE \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Dettagli del sottooggetto flags analizzato da un flusso di stato della pipeline.

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

[**FLAG DI STATO DELLA PIPELINE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





