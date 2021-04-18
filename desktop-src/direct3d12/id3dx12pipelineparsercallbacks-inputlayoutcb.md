---
title: Metodo ID3DX12PipelineParserCallbacks InputLayoutCb (D3DX12. h)
description: Chiama il callback del sottooggetto layout di input di un oggetto che implementa questa interfaccia.
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
ms.openlocfilehash: 2bc28276ef893247577cf41de8f4aba5582c101d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323098"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: InputLayoutCb

Chiama il callback del sottooggetto layout di input di un oggetto che implementa questa interfaccia.

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

Tipo: **const [**D3D12 \_ input \_ layout \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**

Dettagli del sottooggetto layout di input analizzato da un flusso di stato della pipeline.

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

[**\_ \_ Descrizione layout input \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





