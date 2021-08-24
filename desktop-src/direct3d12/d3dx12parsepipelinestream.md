---
title: Funzione D3DX12ParsePipelineStream (D3dx12.h)
description: Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di oggetto secondario analizzata.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- Funzione D3DX12ParsePipelineStream
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbdd472d118a5ec9d49c5f105ee6b8e8ef2e3ea540f6f1954bad17273e9e030f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608561"
---
# <a name="d3dx12parsepipelinestream-function"></a>Funzione D3DX12ParsePipelineStream

Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di oggetto secondario analizzata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Desc* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ PIPELINE STATE STREAM \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

Descrizione del flusso di stato della pipeline da analizzare.

</dd> <dt>

*pCallbacks* 
</dt> <dd>

Tipo: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Struttura che specifica i callback da chiamare per ogni tipo di oggetto secondario e callback aggiuntivi da chiamare in caso di errore di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questo metodo restituisce un errore HRESULT **(errore S \_ OK** o **E \_ INVALIDARG** se viene rilevato un tipo di oggetto secondario sconosciuto, se la descrizione del flusso è vuota, Null o contiene sottooggetti duplicati (inclusi i sottooggetti derivati) o *se pCallbacks* è Null. In ogni caso in cui viene restituito E \_ INVALIDARG, viene prima chiamato un callback corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





