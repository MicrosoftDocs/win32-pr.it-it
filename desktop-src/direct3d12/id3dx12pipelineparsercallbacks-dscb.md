---
title: Metodo ID3DX12PipelineParserCallbacks DSCb (D3DX12. h)
description: Chiama il callback del sottooggetto del Domain shader di un oggetto che implementa questa interfaccia.
ms.assetid: F4877211-4122-4418-9323-3F68B0BB3363
keywords:
- Metodo DSCb
- Metodo DSCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo DSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf5f68ca6e6e4891fa391a142d45a1496a42ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323115"
---
# <a name="id3dx12pipelineparsercallbacksdscb-method"></a>ID3DX12PipelineParserCallbacks::D Metodo SCb

Chiama il callback del sottooggetto del Domain shader di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void DSCb(
  [ref] const D3D12_SHADER_BYTECODE &DS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Servizi di *dominio Active Directory* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ shader \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Dettagli del sottooggetto Domain shader analizzato da un flusso di stato della pipeline.

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

[**\_BYTECODE shader D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





