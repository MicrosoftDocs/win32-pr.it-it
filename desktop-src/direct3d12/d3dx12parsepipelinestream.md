---
title: Funzione D3DX12ParsePipelineStream (D3dx12. h)
description: Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di sottooggetto analizzata.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream (funzione)
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
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322172"
---
# <a name="d3dx12parsepipelinestream-function"></a>D3DX12ParsePipelineStream (funzione)

Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di sottooggetto analizzata.

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

Tipo: **const [**D3D12 \_ pipeline \_ state \_ Stream \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

Descrizione del flusso di stato della pipeline da analizzare.

</dd> <dt>

*pCallbacks* 
</dt> <dd>

Tipo: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Struttura che specifica i callback da chiamare per ogni tipo di sottooggetto e callback aggiuntivi da chiamare in caso di errore di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questo metodo restituisce un errore HRESULT Success (**S \_ OK** o **E \_ INVALIDARG** se viene rilevato un tipo di sottooggetto sconosciuto, se la descrizione del flusso è vuota, null o contiene oggetti SubObject duplicati, inclusi oggetti SubObject derivati), oppure se *pCallbacks* è null. In ogni caso in cui \_ viene restituito E INVALIDARG, viene prima chiamato un callback corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





