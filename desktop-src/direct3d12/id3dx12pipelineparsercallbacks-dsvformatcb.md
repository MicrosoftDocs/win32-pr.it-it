---
title: Metodo ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) (DSV)
description: Chiama il callback del sottooggetto del formato del valore depth stencil di un oggetto che implementa questa interfaccia.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
keywords:
- Metodo DepthStencilStateCb
- Metodo DepthStencilStateCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334359"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a>Metodo ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) per depth stencil valore

Chiama il callback del sottooggetto del formato del valore depth stencil di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DepthStencilState* 
</dt> <dd>

Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Dettagli del depth stencil oggetto del formato del valore analizzato da un flusso di stato della pipeline.

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

[**\_formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

