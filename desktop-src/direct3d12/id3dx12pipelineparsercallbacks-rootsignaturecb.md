---
title: Metodo ID3DX12PipelineParserCallbacks RootSignatureCb (D3DX12. h)
description: Chiama il callback del sottooggetto della firma radice di un oggetto che implementa questa interfaccia.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Metodo RootSignatureCb
- Metodo RootSignatureCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo RootSignatureCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322155"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: RootSignatureCb

Chiama il callback del sottooggetto della firma radice di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RootSignature* 
</dt> <dd>

Tipo: **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***

Dettagli del sottooggetto della firma radice analizzato da un flusso di stato della pipeline.

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

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

