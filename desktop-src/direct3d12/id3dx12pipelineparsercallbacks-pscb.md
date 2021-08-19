---
title: Metodo PSCb ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Chiama il pixel shader di sottooggetto di un oggetto che implementa questa interfaccia.
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- Metodo PSCb
- Metodo PSCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo PSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c15b09598218259d5cdeedfb3453aaf2a4f669242ddb76e676093e81e0dd9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894571"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a>Metodo ID3DX12PipelineParserCallbacks::P SCb

Chiama il pixel shader di sottooggetto di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PS* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Dettagli del sottooggetto pixel shader analizzato da un flusso di stato della pipeline.

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

[**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





