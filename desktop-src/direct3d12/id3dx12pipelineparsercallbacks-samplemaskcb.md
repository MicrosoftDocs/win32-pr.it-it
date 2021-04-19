---
title: Metodo ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12. h)
description: Chiama il callback del sottooggetto maschera di esempio di un oggetto che implementa questa interfaccia.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Metodo SampleMaskCb
- Metodo SampleMaskCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo SampleMaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322150"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>Metodo ID3DX12PipelineParserCallbacks:: SampleMaskCb

Chiama il callback del sottooggetto maschera di esempio di un oggetto che implementa questa interfaccia.

## <a name="syntax"></a>Sintassi


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SampleMask* 
</dt> <dd>

Tipo: **uint**

Dettagli del sottooggetto maschera di esempio analizzato da un flusso di stato della pipeline.

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
</dt> </dl>

 

 





