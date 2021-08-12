---
title: Metodo ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12.h)
description: Chiama il callback depth stencil oggetto secondario D3D12 \_ DEPTH STENCIL DESC1 di un oggetto \_ \_ che implementa questa interfaccia.
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
ms.openlocfilehash: 97deca53ffc4de474896b89993f84cebf359acd9045956243c5ece4e215e31cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528969"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a>Metodo ID3DX12PipelineParserCallbacks::D epthStencilState1Cb

Chiama il callback depth stencil oggetto secondario [**D3D12 \_ DEPTH \_ STENCIL \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) di un oggetto che implementa questa interfaccia.

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

Tipo: **const [**D3D12 \_ DEPTH STENCIL \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**

Dettagli del sottooggetto depth stencil stato della pipeline analizzato da un flusso di stato della pipeline.

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

[**D3D12 \_ DEPTH \_ STENCIL \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





