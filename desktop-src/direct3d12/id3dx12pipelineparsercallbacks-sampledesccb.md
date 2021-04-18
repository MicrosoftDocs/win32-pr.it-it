---
title: Metodo ID3DX12PipelineParserCallbacks SampleDescCb (D3DX12. h)
description: Chiama il callback di esempio della descrizione del sottooggetto di un oggetto che implementa questa interfaccia.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Metodo SampleDescCb
- Metodo SampleDescCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo SampleDescCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322151"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: SampleDescCb

Chiama il callback di esempio della descrizione del sottooggetto di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SampleDesc* \[ Ref\]
</dt> <dd>

Tipo: **const [**DXGI \_ Sample \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**

Dettagli del sottooggetto Descrizione di esempio analizzato da un flusso di stato della pipeline.

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

[**DXGI di \_ esempio \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

