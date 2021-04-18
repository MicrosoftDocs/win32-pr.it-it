---
title: Metodo ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12. h)
description: Chiama lo stato depth stencil (D3D12 \_ Depth \_ stencil \_ DESC1) callback di un oggetto che implementa questa interfaccia.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- Metodo DepthStencilState1Cb
- Metodo DepthStencilState1Cb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo DepthStencilState1Cb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322159"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a>ID3DX12PipelineParserCallbacks::D Metodo epthStencilState1Cb

Chiama lo stato depth stencil ([**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) callback di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DepthStencilState* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**

Dettagli del sottooggetto depth stencil stato analizzato da un flusso di stato della pipeline.

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

[**\_Stencil profondità \_ D3D12 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





