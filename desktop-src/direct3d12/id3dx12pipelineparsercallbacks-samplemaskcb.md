---
title: Metodo ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12.h)
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
ms.openlocfilehash: 64acc7e969f52e78250cde9bc4c693ce3eae06ae3edd08e7f18c65dc0ff6fa8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069591"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>Metodo ID3DX12PipelineParserCallbacks::SampleMaskCb

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

*Maschera di esempio* 
</dt> <dd>

Tipo: **UINT**

Dettagli del sottooggetto maschera di esempio analizzato da un flusso di stato della pipeline.

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
</dt> </dl>

 

 





