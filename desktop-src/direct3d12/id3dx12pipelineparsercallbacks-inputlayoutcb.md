---
title: Metodo InputLayoutCb ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Chiama il callback del sottooggetto di layout di input di un oggetto che implementa questa interfaccia.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Metodo InputLayoutCb
- Metodo InputLayoutCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo InputLayoutCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f7012686c85b38e94f8f3d2400cf406d614fc83ff0ba25e746ac0433b2e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528773"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a>Metodo ID3DX12PipelineParserCallbacks::InputLayoutCb

Chiama il callback del sottooggetto di layout di input di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InputLayout* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ INPUT LAYOUT \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**

Dettagli del sottooggetto di layout di input analizzato da un flusso di stato della pipeline.

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

[**D3D12 \_ INPUT \_ LAYOUT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





